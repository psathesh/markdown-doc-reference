# Minikube

For full documentation visit [minikube](https://minikube.sigs.k8s.io/docs/){:target="_blank"}.

## Installation

	$ brew install minikube
	$ minikube version
	
	$ minikube start --driver=docker
	
	
	$ minikube delete
	$ minikube start --vm-driver virtualbox
	$ minikube addons enable ingress
	
	$ minikube dashboard
	
	$ minikube status
	
	$ minikube stop
	