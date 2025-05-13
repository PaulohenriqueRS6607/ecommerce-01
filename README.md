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




<div style="background-color: #f0ffff; padding: 20px; border-radius: 10px; margin: 20px 0;">
  <h2 style="color: #2c3e50;">🎨 Exemplos de Requisições</h2>
  
  <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h3 style="color: #2c3e50;">Criar Usuário</h3>
    <pre style="color: #34495e;">
{
    "nome": "amanda ferreira",
    "email": "amanda@email.com",
    "telefone": "40028922",
    "senha": "112233445566"
}</pre>
  </div>

  <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h3 style="color: #2c3e50;">Criar Produto</h3>
    <pre style="color: #34495e;">
{
    "nome": "nintendo switch 2",
    "descricao": "Console da mais recente geração",
    "preco": 4.499,90,
    "imagemUrl": "https://exemplo.com/switch2.jpg"
}</pre>
  </div>

  <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h3 style="color: #2c3e50;">Criar Pedido</h3>
    <pre style="color: #34495e;">
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
}</pre>
  </div>
</div>


<div style="background-color: #e6f7ff; padding: 20px; border-radius: 10px; margin: 20px 0;"> <h2 style="color: #2c3e50;">💾 Banco de Dados - MySQL</h2> <p style="color: #34495e;">O banco de dados utilizado contém várias tabelas para gerenciar os dados da livraria e seus processos. A seguir estão as tabelas e seus respectivos campos:</p> <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;"> <h3 style="color: #2c3e50;">Tabela: tb_categoria</h3> <pre style="color: #34495e;"> id INT AUTO_INCREMENT PRIMARY KEY
nome
VARCHAR(255)

descricao
TEXT</pre>

</div> <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;"> <h3 style="color: #2c3e50;">Tabela: tb_item_pedido</h3> <pre style="color: #34495e;"> id INT AUTO_INCREMENT PRIMARY KEY
pedido_id
INT

produto_id
INT

quantidade
INT

preco_unitario
DECIMAL(10, 2)

total
DECIMAL(10, 2)</pre>

</div> <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;"> <h3 style="color: #2c3e50;">Tabela: tb_pagamento</h3> <pre style="color: #34495e;"> id INT AUTO_INCREMENT PRIMARY KEY
pedido_id
INT

data_pagamento
DATETIME

valor_pago
DECIMAL(10, 2)

metodo_pagamento
VARCHAR(100)

status_pagamento
VARCHAR(50)</pre>

</div> <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;"> <h3 style="color: #2c3e50;">Tabela: tb_pedido</h3> <pre style="color: #34495e;"> id INT AUTO_INCREMENT PRIMARY KEY
usuario_id
INT

data_pedido
DATETIME

status_pedido
VARCHAR(100)

total
DECIMAL(10, 2)</pre>

</div> <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;"> <h3 style="color: #2c3e50;">Tabela: tb_produto</h3> <pre style="color: #34495e;"> id INT AUTO_INCREMENT PRIMARY KEY
titulo
VARCHAR(255)

descricao
TEXT

preco
DECIMAL(10, 2)

quantidade_estoque
INT

categoria_id
INT</pre>

</div> <div style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; margin: 10px 0;"> <h3 style="color: #2c3e50;">Tabela: tb_usuario</h3> <pre style="color: #34495e;"> id INT AUTO_INCREMENT PRIMARY KEY
nome
VARCHAR(255)

email
VARCHAR(255)

senha
VARCHAR(255)

endereco
VARCHAR(255)

telefone
VARCHAR(20)</pre>

</div> </div>
