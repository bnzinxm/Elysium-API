<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elysium API - Documentação</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        header {
            background-color: #6c5ce7;
            color: #fff;
            padding: 2rem 1rem;
            text-align: center;
        }

        header h1 {
            font-size: 2.5rem;
            margin: 0;
        }

        header p {
            font-size: 1.2rem;
        }

        section {
            padding: 2rem 1rem;
            margin: 1rem;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        h2 {
            color: #6c5ce7;
            font-size: 1.8rem;
            margin-bottom: 1rem;
        }

        h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        p {
            font-size: 1rem;
            margin-bottom: 1rem;
        }

        code {
            background-color: #f5f5f5;
            padding: 0.2rem 0.5rem;
            border-radius: 5px;
            font-size: 1rem;
        }

        pre {
            background-color: #2d3436;
            color: #dfe6e9;
            padding: 1rem;
            border-radius: 8px;
            overflow-x: auto;
            font-size: 1rem;
            margin-top: 1rem;
        }

        a {
            color: #6c5ce7;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        footer {
            background-color: #2d3436;
            color: #fff;
            padding: 1rem;
            text-align: center;
            position: absolute;
            bottom: 0;
            width: 100%;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        ul li {
            margin-bottom: 0.5rem;
        }
    </style>

</head>
<body>
    <header>
        <h1>Elysium API</h1>
        <p>Documentação oficial da API para integração com a plataforma Elysium.</p>
    </header>

    <section>
        <h2>Introdução</h2>
        <p>A Elysium API fornece acesso a diversos serviços de nossa plataforma, permitindo que você integre funcionalidades de maneira fácil e eficiente. A API foi projetada para ser simples, rápida e segura, com uma documentação clara para facilitar a implementação em seu projeto.</p>
    </section>

    <section>
        <h2>Recursos</h2>
        <p>A Elysium API oferece diversos endpoints para interação com nossa plataforma. Alguns dos recursos disponíveis incluem:</p>
        <ul>
            <li><strong>Autenticação de Usuários</strong> - Gerencie tokens de autenticação e usuários.</li>
            <li><strong>Dados de Performance</strong> - Obtenha dados detalhados sobre a performance da plataforma.</li>
            <li><strong>Gerenciamento de Conteúdo</strong> - Crie, edite e exclua conteúdos diretamente através da API.</li>
            <li><strong>Integração com Terceiros</strong> - Conecte-se com serviços externos facilmente.</li>
        </ul>
    </section>

    <section>
        <h2>Autenticação</h2>
        <p>Para utilizar a Elysium API, é necessário um token de autenticação. Você pode obter um token ao se registrar no sistema e gerar um token no painel de administração.</p>
        <h3>Exemplo de como obter um token:</h3>
        <pre>

curl -X POST https://api.elysium.com/v1/auth/login \
 -H "Content-Type: application/json" \
 -d '{"username": "seu_usuario", "password": "sua_senha"}'
</pre>
<p>O retorno será um token de acesso:</p>
<pre>
{
"token": "your_access_token_here"
}
</pre>
<p>Este token deverá ser incluído nas requisições como um cabeçalho `Authorization`.</p>
</section>

    <section>
        <h2>Exemplo de Endpoints</h2>
        <h3>1. Endpoint de Usuários</h3>
        <p>Este endpoint permite que você obtenha informações sobre um usuário específico.</p>
        <pre>

GET /v1/users/{user_id}
Authorization: Bearer your_access_token_here
</pre>
<p>Exemplo de resposta:</p>
<pre>
{
"id": 123,
"username": "usuario_teste",
"email": "usuario@exemplo.com",
"created_at": "2024-01-01T12:00:00Z"
}
</pre>

        <h3>2. Endpoint de Performance</h3>
        <p>Este endpoint permite acessar dados de performance da plataforma.</p>
        <pre>

GET /v1/performance
Authorization: Bearer your_access_token_here
</pre>
<p>Exemplo de resposta:</p>
<pre>
{
"cpu_usage": "75%",
"memory_usage": "60%",
"requests": 1234
}
</pre>
</section>

    <section>
        <h2>Documentação Completa</h2>
        <p>Para mais detalhes sobre a API, consulte a documentação completa em nosso portal oficial:</p>
        <a href="https://api.elysium.com/docs" target="_blank">Documentação Oficial da Elysium API</a>
    </section>

    <footer>
        <p>&copy; 2024 Elysium. Todos os direitos reservados.</p>
    </footer>

</body>
</html>
