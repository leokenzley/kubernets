# kubernets
kubernets-jupyter-notbook-application - estudo minikube
##Executando o projeto
### cria o namespace jupyter
```
$ kubectl apply -f /jupyter/jupyter-ns.yml
```
### seta o namespace padrão jupyter
```
$ kubectl config set-context --current --namespace=jupyter
```
### executa o deployment
```
$ kubectl apply -f /jupyter/jupyter-dp.yml
```
### mapeia a porta 8888 do container para acesso externo na porta 8080
```
$ kubectl port-forward jupyter-dp-7db5579d8d-tvmck 8080:8888
```
### Abra algum navegador e acesse localhost:8080, deverá aparecer a aplicação jupyter
![img.png](img.png)