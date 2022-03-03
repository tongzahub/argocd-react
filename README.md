# config Kubernetes
```
aws eks --region ap-southeast-1 update-kubeconfig --name arthit-devops-labs
```

# register gitLabs  or github

# crate ReactJS  APP 
```
npx create-react-app  app
```

# create dockerHub Repro 


# Build Docker and Test  Image 
```
docker build -t tongzahub/argocd-react .
docker run -p 9090:3000 tongzahub/argocd-react 
```

# push images to DockerHub 
```
docker push tongzahub/argocd-react:latest

```

# Install Argo CD 
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

# get password argo cd admin 
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```

# kube port-forward
```
kubectl port-forward service/argocd-react  9999:8888
```