*** Recommended to perform below commands as a ROOT user ***
----------------------------------------------------------------------------------------------


echo "Install Helm Chart Using Script"

curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3

chmod 700 get_helm.sh

./get_helm.sh

helm version

=================================================

To have new look of helm folder structure install "tree"

sudo apt install tree

=================================================

helm create helloworld
(Create a helm chart)

Helm install <release-name> .
(Create a release just like to run helm with release name and execute in current helm directory)

Helm list -a 
(To see the helm release along with associated chart)

Kubectl get svc
(To see the services created by helm chart)

Kubectl get deployment 
(To see the deployments created by helm chart)

=================================================

Helm Lint:

helm lint helmlint/
(To check syntax errors)

=================================================

Helm Template:

Helm template .
(Gives details of all files)
(It also checks for validation of the values provided)

=================================================

Helm dry-run:

Helm install myrelease --dry-run --debug .
(Check validation from prod deploy)4

=================================================

Helm Delete:

Helm delete <release-name>

=================================================

Helm Upgrade:

 helm upgrade <release-name>  .
(Should be in PWD)

=================================================


Helm Variables:

Add variables in values.yaml
Now add that in any files with below syntax

{{ .Values.service.type }}

=================================================

Helm Rollback:

First perform Upgrade
Now perform  Rollback

Helm rollback <release-name> <revision-number>



