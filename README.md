# 🚖 Uber-Application  

**Uber-Application** is a Spring Boot-based ride-hailing service that mimics Uber's core functionalities, including ride booking, driver management, fare calculation, and real-time tracking. It follows a **microservices architecture** for scalability and efficiency.  

## 📂 Repository Structure  

```
📦 Uber-Application  
 ┣ 📂 src                    # Application source code  
 ┣ 📜 pom.xml                # Maven dependencies  
 ┣ 📜 mvnw / mvnw.cmd        # Maven wrapper  
 ┣ 📜 README.md              # Project documentation  
```

## ✨ Features  

✔️ **User & Driver Authentication** – Secure login & registration  
✔️ **Ride Booking** – Users can request rides, drivers can accept  
✔️ **Real-time Ride Tracking** – Track ride progress via APIs  
✔️ **Fare Estimation** – Dynamic pricing based on distance & time  
✔️ **Rating & Feedback** – Users & drivers can rate each other  
✔️ **Microservices Architecture** – Modular and scalable  

## 🛠️ Tech Stack  

| Technology  | Description |  
|-------------|------------|  
| **Java 17+**  | Core backend language |  
| **Spring Boot** | Backend framework |  
| **Spring Cloud** | Microservices implementation |  
| **Spring Security + JWT** | Authentication & authorization |  
| **PostgreSQL / MySQL** | Database for ride & user details |  
| **Kafka / RabbitMQ** | Event-driven architecture |  
| **Docker & Kubernetes** | Containerization & orchestration |  

## 🔧 Prerequisites  

- **Java 17+**  
- **Maven**  
- **PostgreSQL or MySQL**  
- **Docker (Optional, for containerized deployment)**  

## 🚀 Installation & Setup  

### 1️⃣ Clone the Repository  

```bash
git clone https://github.com/Hugs-4-Bugs/Uber-Application.git  
cd Uber-Application
```

### 2️⃣ Configure Database  

Update `application.properties` with your database details:  

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/uber_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### 3️⃣ Build and Run  

```bash
mvn clean install  
mvn spring-boot:run  
```

## 📡 API Endpoints  

### 🔹 **User & Driver Authentication**  
| Method | Endpoint | Description |  
|--------|---------|-------------|  
| `POST` | `/api/auth/register` | Register a new user/driver |  
| `POST` | `/api/auth/login` | Login with JWT authentication |  

### 🔹 **Ride Management**  
| Method | Endpoint | Description |  
|--------|---------|-------------|  
| `POST` | `/api/rides/request` | Request a new ride |  
| `POST` | `/api/rides/accept/{rideId}` | Driver accepts a ride |  
| `GET` | `/api/rides/{rideId}` | Get ride details |  

### 🔹 **Fare & Payments**  
| Method | Endpoint | Description |  
|--------|---------|-------------|  
| `GET` | `/api/fare/calculate?distance=X&time=Y` | Estimate fare |  
| `POST` | `/api/payments/charge` | Process ride payment |  

## 📌 Future Enhancements  

- Implement **Geo-Location API** for accurate tracking  
- Add **Payment Gateway Integration** (Stripe, Razorpay)  
- Introduce **AI-based Surge Pricing**  
- Deploy on **AWS with Kubernetes & CI/CD**  

## 🤝 Contribution  

Contributions are welcome! Submit issues or create pull requests.  

## 📜 License  

This project is licensed under the **MIT License**.  

---
