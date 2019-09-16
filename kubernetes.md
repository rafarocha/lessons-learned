## Review Books 
### Cloud Native DevOps with Kubernetes
#### Commands
```shell
# Deployments
kubectl get deployments                 # Listar deployments ativos em namespace atual 
kubectl describe deployments/demo       # Obter detalhes sobre um deployment
kubectl get pods --selector app=demo    # Verifica se o pod está executando
kubectl delete pods --selector app=demo # Encerrar o pod 
kubectl delete all --selector app=demo  # Desativa o deployment e faz limpeza geral
kubectl apply -f k8s/deployment.yaml    # Submete o arquivo manifesto YAML ao cluster

# Services
kubectl port-fowrward service/demo 9999:8888 # Criando um service a partir de um manifesto 
kubectl delete all -f k8s/  # Fazendo a limpeza de todos os recursos na pasta de manifestos

# Pods
kubectl get nodes # Ver os nós presentes em cluster
kubectl get all # Ver recursos de todos os tipos
kubectl describe deployments/demo-dev-6c96484c48-69vss # Obter detalhes de um Pod individual

# Helm
kubectl apply -f helm-auth.yaml # Autorizar o acesso ao seu cluster, arquivo helm 
helm init --service-account tiller # Inicializar o Helm para que acesse o cluster
helm version # Conferir se o helm está pronto e funcionando, em 1st talvez uns 5 mins
helm install --name demo ./k8s/demo # Criar recurso deployment, que inicia um Pod e Service
helm list # Verificar quais releases estã executando em qualquer instante
helm status NOME_RELEASE # Status exato de uma release específica
```
