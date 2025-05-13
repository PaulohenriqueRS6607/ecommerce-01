🛍️ E-commerce Spring Boot
A robust e-commerce application built with Spring Boot for managing products, orders, and users. This project provides a RESTful API with secure authentication and comprehensive CRUD operations.

📋 Project Overview
This is a backend e-commerce system developed to handle user management, product catalog, order processing, and payment operations. It leverages modern Java technologies and follows best practices for scalability and maintainability.

🚀 Technologies Used


Java 21: Modern Java version for enhanced performance and features.
Spring Boot 3.1.0: Framework for building production-ready applications.
Spring Data JPA: Simplifies database interactions with ORM.
MySQL 8.0: Relational database for persistent storage.
Maven: Dependency management and build automation.


🛠️ Features

✅ User Management: Register, list, update, and delete users.
🛒 Product Management: Create, list, update, and delete products.
📦 Order Management: Place, list, update, and delete orders, including client-specific order retrieval.
🔐 Authentication: Secure user authentication for protected endpoints.
💸 Payment Processing: Process payments for orders.


📝 API Endpoints
👨‍👦‍👦 Users



Method
Endpoint
Description



POST
/usuario/salvar
Create a new user


GET
/usuarios
List all users


GET
/usuarios/{id}
Get user by ID


PUT
/usuarios/{id}
Update user


DELETE
/usuarios/{id}
Delete user


🛒 Products



Method
Endpoint
Description



POST
/produtos
Create a new product


GET
/produtos
List all products


GET
/produtos/{id}
Get product by ID


PUT
/produtos/{id}
Update product


DELETE
/produtos/{id}
Delete product


📦 Orders



Method
Endpoint
Description



POST
/pedidos
Create a new order


GET
/pedidos
List all orders


GET
/pedidos/{id}
Get order by ID


PUT
/pedidos/{id}
Update order


DELETE
/pedidos/{id}
Delete order


GET
/pedidos/cliente/{clienteId}
List orders by client


GET
/pedidos/{id}/itens
List items in an order


💸 Payments



Method
Endpoint
Description



POST
/pagamentos/pedido/{id}
Process payment for order



🎨 Example Requests
Create User
{
    "nome": "Amanda Ferreira",
    "email": "amanda@email.com",
    "telefone": "40028922",
    "senha": "112233445566"
}

Create Product
{
    "nome": "Nintendo Switch 2",
    "descricao": "Console da mais recente geração",
    "preco": 4499.90,
    "imagemUrl": "https://exemplo.com/switch2.jpg"
}

Create Order
{
    "cliente": {
        "id": 1
    },
    "items": [
        {
            "produtoId": 1,
            "quantidade": 2,
            "preco": 4499.90
        }
    ]
}


🛠️ Setup Instructions
Prerequisites

Java 21
MySQL 8.0
Maven

Steps

Clone the Repository
git clone https://github.com/your-username/ecommerce-spring-boot.git
cd ecommerce-spring-boot


Configure MySQL

Create a MySQL database named ecommerce.
Update application.properties with your database credentials:spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=your-username
spring.datasource.password=your-password
spring.jpa.hibernate.ddl-auto=update




Build and Run
mvn clean install
mvn spring-boot:run


Access the API

The application runs on http://localhost:8080.




📚 Documentation
For detailed API documentation, refer to the Postman Collection or test the endpoints directly using tools like Postman or cURL.

🤝 Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m 'Add your feature').
Push to the branch (git push origin feature/your-feature).
Open a Pull Request.


📄 License
This project is licensed under the MIT License. See the LICENSE file for details.

📬 Contact
For questions or feedback, feel free to reach out via email or open an issue on GitHub.
