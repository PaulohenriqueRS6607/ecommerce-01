🛍️ E-commerce

📋 Sobre o Projeto
E-commerce desenvolvida com Spring Boot para gerenciamento de produtos, pedidos e usuários.

🚀 Tecnologias Utilizadas
Java 21
Spring Boot 3.1.0
Spring Data JPA
MySQL 8.0
Maven

🛠️ Funcionalidades
✅ Cadastro de usuários
🛒 Gerenciamento de produtos
📦 Controle de pedidos
🔐 Autenticação de usuários
📝 Endpoints

👨‍👦‍👦 Usuários
POST http://localhost:8080/usuario/salvar - Criar usuário
GET http://localhost:8080/usuarios - Listar usuários
GET http://localhost:8080/usuarios/{id} - Buscar usuário por ID
PUT http://localhost:8080/usuarios/{id} - Atualizar usuário
DELETE http://localhost:8080/usuarios/{id} - Deletar usuário

🛒 Produtos
POST http://localhost:8080/produtos - Criar produto
GET http://localhost:8080/produtos - Listar produtos
GET http://localhost:8080/produtos/{id} - Buscar produto por ID
PUT http://localhost:8080/produtos/{id} - Atualizar produto
DELETE http://localhost:8080/produtos/{id} - Deletar produto

📦 Pedidos
POST http://localhost:8080/pedidos - Criar pedido
GET http://localhost:8080/pedidos - Listar pedidos
GET http://localhost:8080/pedidos/{id} - Buscar pedido por ID
PUT http://localhost:8080/pedidos/{id} - Atualizar pedido
DELETE http://localhost:8080/pedidos/{id} - Deletar pedido
GET http://localhost:8080/pedidos/cliente/{clienteId} - Listar pedidos do cliente
GET http://localhost:8080/pedidos/{id}/itens - Listar itens do pedido

💸 Pagamento
POST http://localhost:8080/pagamentos/pedido/{id} - Fazer o pagamento, não precisa de corpo
    
🎨 Exemplos de Requisições
Criar Usuário
{
    "nome": "amanda ferreira",
    "email": "amanda@email.com",
    "telefone": "40028922",
    "senha": "112233445566"
}

Criar Produto
{
    "nome": "nintendo switch 2",
    "descricao": "Console da mais recente geração",
    "preco": 4.499,90,
    "imagemUrl": "https://exemplo.com/switch2.jpg"
}

Criar Pedido
{
    "cliente": {
        "id": 1
    },
    "items": [
        {
            "produtoId": 1,
            "quantidade": 2,
            "preco": 4.499,90
        }
    ]
}
