Multi-Ingress is a chart built for deploying multiple nginx ingress controllers for kubernetes clusters on AWS. 

FOR DEVELOPERS: To point your deployed application to use this ingress controller, you MUST add an annotation to your ingress resource in the following format: 
`kubernetes.io/ingress.class = nginx-<the identifier you set>`
