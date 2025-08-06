1. Link for Deploy Three-Tier DevSecOps Kubernetes Project on AWS EKS with ArgoCD, Prometheus, Grafana, Jenkins is: https://codewithmuh.medium.com/deploy-three-tier-devsecops-kubernetes-project-on-aws-eks-with-argocd-prometheus-grafana-jenkins-0484cbee7ba1
2. Link for Containerizing and Deploying a Three-Tier Application on AWS EKS with Kubernetes is: https://medium.com/@silas.cloudspace/containerizing-and-deploying-a-three-tier-application-on-aws-eks-with-kubernetes-bd9b0eaf2648

Note: I have done POC using the second Link and deployed frontend and backend applications except database. so frontend was working fine, but because of no data base, backend application was not able to connect with database and getting logs as below:


k -n poc-api logs pod/backend-67cfd6fc6b-bsvq2 <-

listening on Port 3500
Error connecting to the database: Error: connect ECONNREFUSED 127.0.0.1:3306
    at TCPConnectWrap.afterConnect [as oncomplete] (net.js:1159:16) {
  errno: -111,
  code: 'ECONNREFUSED',
  syscall: 'connect',
  address: '127.0.0.1',
  port: 3306,
  fatal: true
}
