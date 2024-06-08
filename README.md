# Golang Ecommerce Microservice

## Services
- User
- Authentication
- Email
- Product
- Order
- Inventory

## Technologies
- Golang
- Gin
- Fiber
- MySQL
- Redis
- Nats.io
- gRPC

## Roadmap

### Phase 1: Build Locally
1. **Setup Project Structure**
   - [ ] Create a mono-repo or multiple repositories for each service.
   - [ ] Define a common structure for services (controllers, models, routes, configs)[ ] .

2. **Implement User Service**
   - [ ] Set up Gin or Fiber.
   - [ ] Implement user CRUD operations.
   - [ ] Connect to MySQL database.

3. **Implement Authentication Service**
   - [ ] JWT authentication.
   - [ ] Integrate with User Service for login/registration.
   - [ ] Password hashing (bcrypt).

4. **Implement Email Service**
   - [ ] Set up Nats.io for message queuing.
   - [ ] Create email sending logic.
   - [ ] Design basic email templates.

5. **Implement Product Service**
   - [ ] Product catalog management.
   - [ ] Integration with MySQL for product data.
   - [ ] Implement search and filter functionality.

6. **Implement Order Service**
   - [ ] Order creation and management.
   - [ ] Integrate with User and Product Services.
   - [ ] Basic order status tracking.

7. **Implement Inventory Service**
   - [ ] Inventory tracking and updates.
   - [ ] Connect with Product and Order Services.
   - [ ] Implement stock level adjustments.

### Phase 2: CI/CD Setup & Containerization
1. **CI/CD Setup**
   - [ ] Integrate with GitHub Actions, GitLab CI, or another CI/CD tool.
   - [ ] Automate testing and deployment pipelines.
   - [ ] Ensure all services have corresponding tests.

2. **Containerization**
   - [ ] Create Dockerfiles for each service.
   - [ ] Set up Docker Compose for local development.
   - [ ] Ensure services can communicate within Docker network.

3. **Configuration Management**
   - [ ] Centralize configuration using tools like Consul or Vault.
   - [ ] [ ] Secure sensitive information (DB credentials, API keys).

### Phase 3: Deployment to EKS
1. **Kubernetes Configuration**
   - [ ] Create Kubernetes manifests for each service.
   - [ ] Set up Helm charts for easier management.
   - [ ] Configure namespaces, services, deployments, and secrets.

2. **EKS Deployment**
   - [ ] Set up AWS EKS cluster.
   - [ ] Use tools like eksctl for cluster management.
   - [ ] Deploy services to EKS and ensure they are running correctly.

3. **Monitoring and Logging**
   - [ ] Integrate monitoring tools like Prometheus and Grafana.
   - [ ] [ ] Set up centralized logging using Elasticsearch, Fluentd, and Kibana (EFK stack).

4. **Scaling and Resilience**
   - [ ] Implement auto-scaling policies.
   - [ ] Ensure high availability and fault tolerance.
   - [ ] Set up proper health checks and readiness probes.

## Example Directory Structure
Here is an example directory structure for the project:
```
ecommerce-microservices/
├── user-service/
│   ├── controllers/
│   │   └── user_controller.go
│   ├── models/
│   │   └── user.go
│   ├── routes/
│   │   └── user_routes.go
│   ├── main.go
│   ├── Dockerfile
│   └── ...
├── auth-service/
│   ├── controllers/
│   │   └── auth_controller.go
│   ├── models/
│   │   └── auth.go
│   ├── routes/
│   │   └── auth_routes.go
│   ├── main.go
│   ├── Dockerfile
│   └── ...
├── email-service/
│   ├── controllers/
│   │   └── email_controller.go
│   ├── templates/
│   │   └── welcome_email.html
│   ├── main.go
│   ├── Dockerfile
│   └── ...
├── product-service/
│   ├── controllers/
│   │   └── product_controller.go
│   ├── models/
│   │   └── product.go
│   ├── routes/
│   │   └── product_routes.go
│   ├── main.go
│   ├── Dockerfile
│   └── ...
├── order-service/
│   ├── controllers/
│   │   └── order_controller.go
│   ├── models/
│   │   └── order.go
│   ├── routes/
│   │   └── order_routes.go
│   ├── main.go
│   ├── Dockerfile
│   └── ...
├── inventory-service/
│   ├── controllers/
│   │   └── inventory_controller.go
│   ├── models/
│   │   └── inventory.go
│   ├── routes/
│   │   └── inventory_routes.go
│   ├── main.go
│   ├── Dockerfile
│   └── ...
└── docker-compose.yml
```

This structure helps in keeping each service modular and independent, facilitating easier development and deployment.

### Conclusion
This roadmap provides a structured approach to building, containerizing, and deploying a Golang-based eCommerce microservice architecture. By following these phases, you can ensure that each service is developed correctly, tested, and deployed efficiently, leading to a robust and scalable application.
