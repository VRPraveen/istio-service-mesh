#steps to install minikube 

wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
# From the above command download the binaries of minikube.On to your local-system

sudo cp minikube-linux-amd64 /usr/local/bin/minikube
# copy the binaries, onto bin folder

sudo chmod +x /usr/local/bin/minikube
# changing mod onto executable file for the minikube executable file.

minikube version
# Check for the minikube version example:minikube version: v1.27.0

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
# In this above command we are fetching kubenetes-command-linetool (kubectl)

chmod +x kubectl
# changing mod onto executable file for the kubectl executable file.

sudo mv kubectl /usr/local/bin/
# moving the kubectl onto bin folder

kubectl version 
# Check the ionstalled version of kubernetes-command line tool.

minikube start --driver=docker
# Start the minikube by setting docker as a driver

minikube status
# Check for the status of the minikube

minikube dashboard
# To view the kubenetes dashboard 

#steps to install istio on minikube

istioctl install --set profile=default
# On the above command Installing istio-command-line-tool and setting the profile onto default 

kubectl get pod -n istio-system 
# On the above command istiod and istio-ingress gateway pod is up and running

#Run the following yaml files 
metrics: folder contains prometheus, grafana and jaeger
kiali-istio: This folder contains kiali yaml to view the GUI for the istio-service mesh
apps: This folder contains the application.yaml's. istio-gateway yaml's, virtual service yaml with request routing logic to the deployed application.
grafana-dashboard: This folder contains cluster monitoring dashboard which can imported as a json in grafana.





