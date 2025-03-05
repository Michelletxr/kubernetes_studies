# Kubernetes - Comandos Essenciais

## 📌 Gerenciamento do Cluster
```sh
kubectl cluster-info         # Ver informações do cluster
kubectl version              # Ver versão do Kubernetes e do kubectl
kubectl get nodes            # Listar os nós do cluster
kubectl describe node <nome> # Exibir detalhes de um nó específico
```

## 📌 Gerenciamento de Pods
```sh
kubectl get pods                     # Listar todos os Pods
kubectl get pods -o wide              # Listar Pods com detalhes adicionais
kubectl describe pod <meu-pod>        # Ver detalhes de um Pod específico
kubectl logs <meu-pod>                # Ver logs de um Pod
kubectl logs -f <meu-pod>             # Ver logs em tempo real
kubectl delete pod <meu-pod>          # Remover um Pod
kubectl exec -it <meu-pod> -- /bin/sh # Entrar no shell de um Pod
```

## 📌 Criando e Gerenciando Deployments
```sh
kubectl create deployment meu-deploy --image=nginx       # Criar um Deployment
kubectl get deployments                                  # Listar os Deployments
kubectl describe deployment meu-deploy                   # Ver detalhes de um Deployment
kubectl scale deployment meu-deploy --replicas=3         # Escalar réplicas de um Deployment
kubectl rollout restart deployment meu-deploy            # Reiniciar um Deployment
kubectl delete deployment meu-deploy                     # Remover um Deployment
```

## 📌 Trabalhando com Services
```sh
kubectl expose pod meu-pod --type=NodePort --port=8080  # Criar um Service NodePort
kubectl get services                                    # Listar os Services
kubectl describe service meu-pod                        # Ver detalhes de um Service
kubectl delete service meu-pod                          # Remover um Service
```

## 📌 Gerenciando Namespaces
```sh
kubectl get namespaces                  # Listar todos os Namespaces
kubectl create namespace meu-namespace   # Criar um Namespace
kubectl delete namespace meu-namespace   # Remover um Namespace
```

## 📌 Trabalhando com Arquivos YAML
```sh
kubectl apply -f meu-arquivo.yaml  # Aplicar um arquivo YAML
kubectl delete -f meu-arquivo.yaml # Remover recursos do arquivo YAML
kubectl get all                    # Listar todos os recursos no namespace atual
```

## 📌 Diagnóstico e Debugging
```sh
kubectl get events                            # Ver eventos do cluster
kubectl get pods --all-namespaces             # Listar Pods em todos os Namespaces
kubectl logs <meu-pod>                        # Ver logs de um Pod
kubectl logs -f <meu-pod>                     # Acompanhar logs em tempo real
kubectl exec -it <meu-pod> -- /bin/sh         # Acessar o shell do contêiner
kubectl top pod                               # Ver uso de CPU e memória dos Pods
kubectl top node                              # Ver uso de CPU e memória dos Nodes
```

## 🚀 Resumo
Esses comandos cobrem os principais usos do Kubernetes! 🔥  

