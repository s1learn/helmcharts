Updated Directory Structure and Files
Here's the full directory structure for the main-application Helm chart, including the sub-charts for general-job, web-frontend, and web-backend, along with the CronJob configuration, with the container port changed to 8080.

'''
main-application/
  Chart.yaml
general-job/
  Chart.yaml
  templates/
    pvc.yaml
    cronjob.yaml
web-frontend/
  Chart.yaml
  templates/
    deployment.yaml
web-backend/
  Chart.yaml
  templates/
    deployment.yaml


Steps to Deploy
Navigate to the main-application directory:

'''
cd path/to/main-application
Update dependencies:

'''
helm dependency update
This command will fetch and update the dependencies specified in the Chart.yaml file of the main application.

Deploy the main application:

'''
helm install main-application .
This command installs the main application along with its dependencies (sub-charts) into your Kubernetes cluster.

