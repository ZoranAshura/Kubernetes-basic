## Part 1. Ready-made manifest

#### 1. Run a Kubernetes environment with 4GB memory
![1.1](./images/part_1/1.1.png)
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