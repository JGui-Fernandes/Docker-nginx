# 🚀 Docker + Kubernetes — joao-fernandes/docker-nginx

Projeto de exemplo usando **Docker** e **Kubernetes** com o **NGINX**.

---
## ⚙️ Ferramentas usadas
- [Docker](https://www.docker.com/get-started/)
- [Kubectl](https://kubernetes.io/pt-br/docs/tasks/tools/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)

---

## Baixando o projeto

### Clonando o repositório
```bash
git clone https://github.com/JGui-Fernandes/Docker-nginx.git
```
### Acessando a pasta
```bash
cd Docker-nginx
```

---

## 🐳 Docker

### Build da imagem
```bash
docker build -t joao-fernandes/docker-nginx:1.0 .
```

### Rodando a imagem (opcional)
```bash
docker run -d --name docker-nginx -p 8080:80 joao-fernandes/docker-nginx:1.0
```

### Acessar servidor em execução (opcional)
[Acesse localhost](http://localhost:8080/)

---

## ☸️ Kubernetes

### Subindo deploy e service
```bash
kubectl apply -f ./k8/deploy.yaml
kubectl apply -f ./k8/service.yaml
```

### Confirmar que os pods, deploy e service estão rodando (opcional)
```bash
kubectl get all
```

### Acessar o localhost
[Acesse localhost](http://localhost:30080/)

### Limpando cluster
```bash
kubectl delete -f ./k8/deploy.yaml -f ./k8/service.yaml
```
