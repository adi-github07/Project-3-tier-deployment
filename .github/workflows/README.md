GITHUB_ACTIONS:

This pipeline uses Ubuntu runners to automate testing, security scanning, Docker builds, and Kubernetes manifest updates for Node.js microservices

1. Checkout of repo sets up node.js.Runs syntax validation on all .js 
2. Gitleaks scan:scans the code for exposed secret like tokens,password,api keys
3. Trivy scan for vulnerabilty check
4. Docker build and push using github sha for unique versioning 
5. Image vulnerabilty scan using trivy image scan for OS and library  vulnerabilities
6. Kubernetes auto update of manifest:updating the docker image using latest image tag using yq to update the images
7. Commits and pushes of the latest docker images with the latest git commit sha tag




