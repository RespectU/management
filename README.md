# management
aws ecr get-login-password --region ap-northeast-2 | docker login --username AWS -p $(aws ecr get-login-password --region ap-northeast-2) 271153858532.dkr.ecr.ap-northeast-2.amazonaws.com/



curl https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get | bash

kubectl --namespace kube-system create sa tiller

kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller

helm init --service-account tiller

kubectl patch deploy --namespace kube-system tiller-deploy -p '{"spec":{"template":{"spec":{"serviceAccount":"tiller"}}}}'

helm repo add incubator http://storage.googleapis.com/kubernetes-charts-incubator
helm repo update
helm install --name my-kafka --namespace kafka incubator/kafka  

kubectl get po -n kafka 



AWS_ACCOUNT_ID
271153858532

KUBE_URL
https://1909A15692175E5B4C379C70779A535F.sk1.ap-northeast-2.eks.amazonaws.com

KUBE_TOKEN
