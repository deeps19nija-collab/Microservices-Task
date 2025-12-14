# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```

---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```
2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!

--------------------------------------------------------------------------------------------------------------
## Create the docker file in respective services folders like user-service -> Dockerfile , order-service -> dockerfile etc.   
## and Build the docker images, tag it and push to docker hub 

**termianal command history**  
cd .\Microservices\  
  16 cd .\user-service\  
  17 clear  
  18 docker login  
  19 docker build -t deepsjain271/user-service  
  20 docker build -t deepsjain271/user-service .  
  21 clear  
  22 cd ..  
  23 cd prod  
  24 cd .\product-service\  
  25 cles  
  26 clear  
  27 docker build -t deepsjain271/product-service .  
  28 cd ..  
  29 cd .\order-service\  
  30 clear  
  31 docker build -t deepsjain271/order-service .  
  32 cd ..  
  33 cd .\gateway-service\  
  34 docker build -t deepsjain271/gateway-service .  
  35 docker build -t deepsjain271/gateway-service .  
  36 cls  
  
  <img width="1286" height="611" alt="image" src="https://github.com/user-attachments/assets/957d56e0-3e15-47e0-a082-44ff9fecaba6" />  
  
  **commands **  
  45 docker images  
  46 docker push deepsjain271/user-service:latest  
  47 docker push deepsjain271/product-service:latest  
  48 docker push deepsjain271/order-service:latest  
  49 docker push deepsjain271/gateway-service:latest  

  <img width="1428" height="603" alt="image" src="https://github.com/user-attachments/assets/e1c4d3c7-fa05-4139-a4bd-f33bad75bdc5" />  


  ## Minikube config  
  <img width="1311" height="477" alt="image" src="https://github.com/user-attachments/assets/578539c7-0ba5-4429-8395-d8995b2a825c" />  

  ## Screenshot Inter-Service Communication  
 **Gateway communicates with services using Kubernetes DNS:**  
    http://user-service:3000  
    http://product-service:3001  
    http://order-service:3002  

    
  <img width="593" height="355" alt="image" src="https://github.com/user-attachments/assets/1a7ac820-ee46-454e-9d25-346330f940bb" />
  
  <img width="751" height="336" alt="image" src="https://github.com/user-attachments/assets/a326b605-b152-4f9a-894b-a880f3ac2da5" />
  
  <img width="941" height="367" alt="image" src="https://github.com/user-attachments/assets/8c733b6c-4cda-4363-8071-cf2f562406d7" />
  
  <img width="696" height="353" alt="image" src="https://github.com/user-attachments/assets/961828d7-497c-42a7-80b6-24112bf14d37" />

 **For , order-service there is no data initially, You can add the data through gateway endpoint http://localhost:3003/api/orders as below**  

  <img width="986" height="787" alt="image" src="https://github.com/user-attachments/assets/d166faff-1bee-40e5-b188-4714018cf04c" />  
  
   **Now, again hit the url for order-service you will get the ouptut**  

 <img width="1015" height="373" alt="image" src="https://github.com/user-attachments/assets/249943f9-00c8-4337-965c-0d58af54c8a7" />  

 **************************************************************************************************************************************************






  


  


  




