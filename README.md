# Kubernetes
<img width="600" alt="Screenshot 2567-08-22 at 19 28 18" src="https://github.com/user-attachments/assets/d323f789-2362-4f98-8bc2-7a2a3931f148">


# Virtualiztion 
<img width="600" alt="Screenshot 2567-08-22 at 19 33 10" src="https://github.com/user-attachments/assets/b8663f37-f5c4-4e87-be14-84044e9b4937">
<img width="600" alt="Screenshot 2567-08-22 at 18 44 15" src="https://github.com/user-attachments/assets/560db0f5-85f5-43b3-a0ea-0ad17b705581">


# Result
<img width="600" alt="Screenshot 2567-08-22 at 18 45 34" src="https://github.com/user-attachments/assets/a3e47388-ea18-4248-aec0-5bba98913b12">
<img width="300" alt="Screenshot 2567-08-22 at 22 09 37" src="https://github.com/user-attachments/assets/0588b98c-833e-4f93-b55c-c987f46c4152">
<img width="600" alt="Screenshot 2567-08-22 at 18 45 50" src="https://github.com/user-attachments/assets/41764df7-f559-428d-a2cf-8238a7ccd410">
<img width="900" alt="Screenshot 2567-08-22 at 19 17 22" src="https://github.com/user-attachments/assets/8fbcd3e7-63ff-4fe2-af92-797f2da075a9">

# Set up CMD
📌pull graphite from helm to configure

https://artifacthub.io/packages/helm/kiwigrid/graphite

helm pull kiwigrid/graphite --untar --untardir .

📌 build and push to dockerhub manually
docker build -t dckerbeniii/app-send-metric:latest .

docker login

docker push dckerbeniii/app-send-metric:latest

📌start mini cluster

minikube start --driver docker --cpus=2 --memory=2200 --disk-size=20g

helm install my-graphite . -f values.yaml

kubectl apply -f deployment-app-send-metrics.yml



