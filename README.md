<h1>Descrição do Projeto</h1>

<p>Este projeto é uma API RESTful desenvolvida em Java utilizando o framework Spring, incluindo Spring Boot, Spring JWT e H2 Database. Ele foi criado utilizando o Spring Initializr para facilitar a configuração inicial.</p>

<p>A principal funcionalidade da API é permitir o registro e o login de novos usuários, fornecendo autenticação JWT para garantir a segurança dos endpoints.</p>

<h2>Funcionalidades</h2>

<ul>
  <li><strong>Registro de Usuário</strong>: Os usuários podem se registrar na API fornecendo um nome, um endereço de e-mail e uma senha. A API verifica se o e-mail já está em uso e, em seguida, registra o novo usuário no sistema.</li>
  
  <li><strong>Login de Usuário</strong>: Os usuários podem fazer login na API fornecendo seu endereço de e-mail e senha. Se as credenciais estiverem corretas, a API gera um token JWT para autenticação subsequente.</li>
</ul>

<h2>Testando a API</h2>

<p>Para testar a API, siga estas instruções:</p>

<ol>
  <li><strong>Clonando o Projeto</strong>: Clone este repositório em sua máquina local usando o seguinte comando:<br>
    <code>git clone https://github.com/Edmilson95/login-auth-api.git</code></li>
  
  <li><strong>Registro de Usuário</strong>: Faça uma solicitação POST para o endpoint <code>/register</code> com o seguinte JSON no corpo da solicitação:<br>
    {
    "name": "Edmilson",
    "email": "edmilson@gmail.com",
    "password": "123456789"
    }
    A API retornará um código 200 OK e um token JWT para autenticação.</li>
  
  <li><strong>Login de Usuário</strong>: Faça uma solicitação POST para o endpoint <code>/login</code> com o seguinte JSON no corpo da solicitação:<br>
    {
    "email": "edmilson@gmail.com",
    "password": "123456789"
    }
    Se as credenciais estiverem corretas, a API retornará um código 200 OK e um token JWT também.</li>
    
    Testando a Autenticação: Após o login bem-sucedido, faça uma solicitação GET para o endpoint <code>/user</code> com o token JWT gerado no corpo da requisição, utilizando o prefixo Bearer. Certifique-se de incluir o token no seguinte formato:<br>
    {
    "Authorization": "Bearer seu-token-jwt"
    }
    Se tudo estiver configurado corretamente, a resposta será "Suuuuuuuuuucesso!" com um código de status 200 OK.</li>   
</ol>

<h2>Ambiente de Desenvolvimento</h2>

<p>Este projeto foi desenvolvido e testado localmente usando o Java 17.</p>
