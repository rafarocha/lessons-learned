# Commands
### Deployments

#### 
```
kubectl get deployments         # Listar deployments ativos em namespace atual ou não especificado aaa sfdsgsgsdgsdg 
```

#### Obter detalhes sobre um deployment
```kubectl describe deployments/demo```

kubectl get pods --selector app=demo -- verifica se o pod está executando
kubectl delete pods --selector app=demo -- encerrar o pod
kubectl delete all --selector app=demo -- desativa o deployment e faz limpeza geral
kubectl apply -f k8s/deployment.yaml -- submete o arquivo manifesto YAML ao cluster
kubectl port-fowrward service/demo 9999:8888 -- criando um service. para a partir de um manifesto 
kubectl delete all -f k8s/ -- fazendo a limpeza de todos os recursos na pasta de maifestos
kubectl get nodes -- ver os nós presentes em cluster
kubectl get all -- ver recursos de todos os tipos
kubectl describe deployments/demo-dev-6c96484c48-69vss -- obter detalhes de um Pod individual

kubectl apply -f helm-auth.yaml -- autorizar o acesso ao seu cluster, arquivo helm 
helm init --service-account tiller -- inicializar o Helm para que acesse o cluster
helm version -- conferir se o helm está pronto e funcionando, em 1st talvez uns 5 mins
helm install --name demo ./k8s/demo -- criar recurso deployment, que inicia um Pod e Service
helm list -- verificar quais releases estã executando em qualquer instante
helm status NOME_RELEASE -- status exato de uma release específica
