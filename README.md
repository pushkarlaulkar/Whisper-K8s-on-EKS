Instructions to deploy YoPass on AWS EKS Auto Mode
  1. Deploy EKS cluster through Auto Mode through AWS Console. Add the ` CoreDNS `, ` VPC CNI `, ` Kube Proxy ` add ons.
  2. Create a namespace. ` kubectl create ns yopass `
  3. Deploy the `memcached` & `yopass` deployment & service using the `kubectl` command
  4. ` kubectl -n yopass apply -f yopass-dep.yml -f yopass-svc.yml -f memcached-dep.yml -f memcached-svc.yml `
  5. Deploy `Ingress`, `Ingress Class` & `Ingress Params` which will create a ALB listening on port 443. We will need to provide the arn of the certificate in the `Ingress` object.
  6. Run the command ` kubectl -n yopass -f ingress-all.yml `
