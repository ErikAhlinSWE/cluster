hämta yml fil från cluster lenode - kubeconfig.yaml
skapar ett namespace i clustret -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\01-namespace.yaml
skapar PVC (persistent volume clame) -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\10-pvc.yaml   
skapar mysql -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\20-mysql.yaml   
skapar deploy -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\30-ya123site.yaml   
skapar DNS -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\50-ingress.yaml   
