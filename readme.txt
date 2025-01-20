hämta yml fil från cluster lenode - kubeconfig.yaml
skapar ett namespace i clustret -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\01-namespace.yaml
skapar PVC (persistent volume clame) -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\10-pvc.yaml   
skapar mysql -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\20-mysql.yaml   
skapar deploy -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\30-ya123site.yaml
skapar deploy -> kubectl --kubeconfig=kubeconfig.yaml --namespace=keel apply -f .\31-cloudstartpythonapi.yaml   
skapar deploy -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\40-extrasite.yaml
skapar DNS -> kubectl --kubeconfig=.\kubeconfig.yaml apply -f .\50-ingress.yaml   
skapar Redis -> kubectl --kubeconfig=kubeconfig.yaml --namespace=yatest apply -f .\60-redis.yaml
skapar Keel -> kubectl --kubeconfig=kubeconfig.yaml --namespace=keel apply -f .\70-keel.yaml
skapar DNS Keel -> kubectl --kubeconfig=kubeconfig.yaml --namespace=keel apply -f .\71-keelingress.yaml

se alla pods för yatest -> kubectl --kubeconfig=kubeconfig.yaml --namespace=yatest get pods --namespace yatest 
uppdaterar pods ->         kubectl --kubeconfig=.\kubeconfig.yaml rollout restart -n yatest deployment yagolangsite      