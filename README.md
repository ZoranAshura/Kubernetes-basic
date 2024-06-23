## Part 1. Ready-made manifest

#### 1. Run a Kubernetes environment with 4GB memory
![1.2](./images/part_1/1.2.png)

#### 2. Apply the manifest from the /src/example directory to the created Kubernetes environment
![1.3](./images/part_1/1.3.png)
![1.4](./images/part_1/1.4.png)

> The project from docker hub doesn't work on my system cause I have arm architecture not amd
![1.5](./images/part_1/1.5.png)
#### 2.1. So let's create my custom simple manifest
![1.6](./images/part_1/1.6.png)
![1.7](./images/part_1/1.7.png)
> ./src/example/nginx.yml

#### 3. Run the standard Kubernetes control panel with the minikube dashboard
![1.8](./images/part_1/1.8.png)
![1.9](./images/part_1/1.9.png)

#### 4. Create tunnels to access the deployed services with the command minikube services
#### 5. Check if the deployed application works by opening the application page in the browser (nginx service)
![1.10](./images/part_1/1.10.png)

## Part 2. Your own manifest

#### 1. Write your own yml-files of manifests for the application from the first project (/src/services) implementing the following:
- Configuration map with the values of database hosts and services.
- Secrets with the password and login to the database.
- Pods and services for all application modules: postgres, rabbitmq and 7 application services. Use a single replica for all services.
> Check the ./src/k8s-configs directory

#### 2. Run the application by sequentially applying manifests with the command kubectl apply -f <manifest>.yaml.
![2.1](./images/part_2/2.1.png)

#### 3. Check the status of created objects (secrets, configuration map, pods and services) in the cluster using kubectl get <object_type> <object_name> and kubectl describe <object_type> <object_name>. 
![2.2](./images/part_2/2.2.png)
![2.3](./images/part_2/2.3.png)

#### 4. Check for correct secret values by applying, for example, the command: kubectl get secret my-secret -o jsonpath='{.data.password}' | base64 --decode to decode the secret.
> I have the same password and login for postgres database 
![2.4](./images/part_2/2.4.png)

#### 5. Check the logs of the application running in the cluster with the command kubectl logs <container_name>
![2.5](./images/part_2/2.5.png)
> ETC...

#### 6. Create tunnels to access the gateway service and session service.
![2.6](./images/part_2/2.6.png)
![2.7](./images/part_2/2.7.png)

#### 7. Run postman functional tests and make sure that the application works.
![2.8](./images/part_2/2.8.png)

#### 8. Run the standard Kubernetes control panel with the command minikube dashboard. Include the following information in the report as screenshots from the dashboard: the current state of the cluster nodes, a list of running Pods, and other metrics such as CPU and memory utilization, Pod logs, configurations on the Pod and secrets.
![2.9](./images/part_2/2.9.png)
![2.9](./images/part_2/2.10.png)
![2.9](./images/part_2/2.11.png)
![2.9](./images/part_2/2.12.png)
> ETC... 

#### 9. Rebuild the application with the following deployment strategies:
- recreate
![2.9](./images/part_2/2.13.png)
![2.9](./images/part_2/2.14.png)
![2.9](./images/part_2/2.15.png)
> Less than a minute 
- rolling
![2.9](./images/part_2/2.16.png)
![2.9](./images/part_2/2.17.png)
![2.9](./images/part_2/2.18.png)


