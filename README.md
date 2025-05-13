🛍️ E-commerce
Uma aplicação de e-commerce desenvolvida com Spring Boot para gerenciamento de produtos, pedidos e usuários.

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



Método
Endpoint
Descrição



POST
http://localhost:8080/usuario/salvar
Criar usuário


GET
http://localhost:8080/usuario
Listar usuários


GET
http://localhost:8080/usuario/{id}
Buscar usuário por ID


PUT
http://localhost:8080/usuario/{id}
Atualizar usuário


DELETE
http://localhost:8080/usuario/{id}
Deletar usuário


🛒 Produtos



Método
Endpoint
Descrição



POST
http://localhost:8080/produtos
Criar produto


GET
http://localhost:8080/produtos
Listar produtos


GET
http://localhost:8080/produtos/{id}
Buscar produto por ID


PUT
http://localhost:8080/produtos/{id}
Atualizar produto


DELETE
http://localhost:8080/produtos/{id}
Deletar produto


📦 Pedidos



Método
Endpoint
Descrição



POST
http://localhost:8080/pedidos
Criar pedido


GET
http://localhost:8080/pedidos
Listar pedidos


GET
http://localhost:8080/pedidos/{id}
Buscar pedido por ID


PUT
http://localhost:8080/pedidos/{id}
Atualizar pedido


DELETE
http://localhost:8080/pedidos/{id}
Deletar pedido


GET
http://localhost:8080/pedidos/cliente/{clienteId}
Listar pedidos do cliente


GET
http://localhost:8080/pedidos/{id}/itens
Listar itens do pedido


💸 Pagamento



Método
Endpoint
Descrição



POST
http://localhost:8080/pagamentos/pedido/{id}
Fazer o pagamento, não precisa de corpo



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
spring.datasource.password=sua-senha
spring.jpa.hibernate.ddl-auto=update




Compilar e Executar
mvn clean install
mvn spring-boot:run


Acessar a API

A aplicação estará disponível em http://localhost:8080.




📚 Documentação
Para documentação detalhada da API, teste os endpoints usando ferramentas como Postman ou cURL.

🤝 Contribuição
Contribuições são bem-vindas! Siga os passos abaixo:

Faça um fork do repositório.
Crie uma nova branch (git checkout -b feature/sua-funcionalidade).
Commit suas alterações (git commit -m 'Adiciona sua funcionalidade').
Envie para a branch (git push origin feature/sua-funcionalidade).
Abra um Pull Request.


📄 Licença
Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.

📬 Contato
Para dúvidas ou feedback, abra uma issue no GitHub.
