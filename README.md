Instructions to deploy YoPass on AWS EKS Auto Mode
  1. Deploy EKS Auto Mode through AWS Console.
  2. Create a namespace. ` kubectl create ns yopass `
  3. Deploy the `memcached` & `yopass` deployment & service using the `kubectl` command :- ` kubectl -n yopass apply -f yopass-dep.yml -f yopass-svc.yml `
