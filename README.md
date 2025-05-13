🛍️ E-commerce Spring Boot
Uma aplicação de e-commerce robusta desenvolvida com Spring Boot para gerenciamento de produtos, pedidos e usuários. Este projeto oferece uma API RESTful com autenticação segura e operações CRUD completas.

📋 Sobre o Projeto
Este é um sistema de e-commerce backend projetado para gerenciar usuários, catálogo de produtos, processamento de pedidos e operações de pagamento. Utiliza tecnologias modernas de Java e segue boas práticas para escalabilidade e manutenção.

🚀 Tecnologias Utilizadas


Java 21: Versão moderna do Java para melhor desempenho e funcionalidades.
Spring Boot 3.1.0: Framework para construção de aplicações prontas para produção.
Spring Data JPA: Simplifica interações com banco de dados usando ORM.
MySQL 8.0: Banco de dados relacional para armazenamento persistente.
Maven: Gerenciamento de dependências e automação de build.


🛠️ Funcionalidades

✅ Gerenciamento de Usuários: Cadastro, listagem, atualização e exclusão de usuários.
🛒 Gerenciamento de Produtos: Criação, listagem, atualização e exclusão de produtos.
📦 Gerenciamento de Pedidos: Criação, listagem, atualização e exclusão de pedidos, incluindo recuperação de pedidos por cliente.
🔐 Autenticação: Autenticação segura de usuários para endpoints protegidos.
💸 Processamento de Pagamentos: Processamento de pagamentos para pedidos.


📝 Endpoints da API
👨‍👦‍👦 Usuários



Método
Endpoint
Descrição



POST
/usuario/salvar
Criar um novo usuário


GET
/usuarios
Listar todos os usuários


GET
/usuarios/{id}
Buscar usuário por ID


PUT
/usuarios/{id}
Atualizar usuário


DELETE
/usuarios/{id}
Excluir usuário


🛒 Produtos



Método
Endpoint
Descrição



POST
/produtos
Criar um novo produto


GET
/produtos
Listar todos os produtos


GET
/produtos/{id}
Buscar produto por ID


PUT
/produtos/{id}
Atualizar produto


DELETE
/produtos/{id}
Excluir produto


📦 Pedidos



Método
Endpoint
Descrição



POST
/pedidos
Criar um novo pedido


GET
/pedidos
Listar todos os pedidos


GET
/pedidos/{id}
Buscar pedido por ID


PUT
/pedidos/{id}
Atualizar pedido


DELETE
/pedidos/{id}
Excluir pedido


GET
/pedidos/cliente/{clienteId}
Listar pedidos por cliente


GET
/pedidos/{id}/itens
Listar itens de um pedido


💸 Pagamentos



Método
Endpoint
Descrição



POST
/pagamentos/pedido/{id}
Processar pagamento do pedido



🎨 Exemplos de Requisições
Criar Usuário
{
    "nome": "Amanda Ferreira",
    "email": "amanda@email.com",
    "telefone": "40028922",
    "senha": "112233445566"
}

Criar Produto
{
    "nome": "Nintendo Switch 2",
    "descricao": "Console da mais recente geração",
    "preco": 4499.90,
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
            "preco": 4499.90
        }
    ]
}


🛠️ Instruções de Configuração
Pré-requisitos

Java 21
MySQL 8.0
Maven

Passos

Clonar o Repositório
git clone https://github.com/seu-usuario/ecommerce-spring-boot.git
cd ecommerce-spring-boot


Configurar o MySQL

Crie um banco de dados MySQL chamado ecommerce.
Atualize o arquivo application.properties com suas credenciais do banco:spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=seu-usuario
spring.datasource.password=sua-
spring.jpa.hibernate.ddl-auto=update



