# Helm

For full documentation visit [helm.sh](https://helm.sh/){:target="_blank"}.

## Installation


	$ brew install helm
	$ helm repo add stable https://kubernetes-charts.storage.googleapis.com/
	$ helm repo add incubator https://kubernetes-charts-incubator.storage.googleapis.com/
	$ helm repo update
	
	$ helm search repo stable
	$ helm search repo nginx
	
	$ helm ls
	
	$ helm dependency update /Users/upurusa/Downloads/caasp-services-master/contrib/helm-charts/portus
	
	
	$ helm install bagi incubator/portus
	
	$ helm install --name bagi incubator/portus
	
	
	
	$ helm install bagi /Users/upurusa/Downloads/caasp-services-master/contrib/helm-charts/portus
	$ helm install bagi -f ./portus/values.yaml ./portus
	$ helm upgrade bagi -f ./portus/values.yaml ./portus
	$ helm uninstall bagi
	$ helm delete bagi

	$ helm --debug upgrade --install bagi -f ./portus/values.yaml ./portus

	$ helm get manifest bagi


	$ helm install my-mariadb -f ./mariadb/values.yaml ./mariadb



[BACK to TOC](./../README.md)

----------