# Elysium API

A **Elysium API** é uma API RESTful desenvolvida para [descrição do seu projeto], oferecendo funcionalidades como [listar as funcionalidades principais, como CRUD, autenticação, etc.]. Ela foi construída utilizando **[Tecnologias utilizadas, como Node.js, TypeScript, Fastify, MongoDB, etc.]** e visa proporcionar uma maneira eficiente e escalável de facilidade para uso.

## Funcionalidades

- **Autenticação**: Suporte a login e criação de contas de usuários.
- **CRUD**: Operações para criar, ler, atualizar e excluir dados.
- **[Outras funcionalidades específicas do seu projeto]**.

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript no servidor.
- **TypeScript**: Superset do JavaScript para um código mais robusto.
- **Express**: Framework para criar APIs em Node.js.
- **[Outras tecnologias que você usou, como banco de dados, ORM, etc.]**

## Instalação

Para rodar o projeto localmente, siga os passos abaixo:

### 1. Clone o repositório

```bash
git clone https://github.com/SeuUsuario/Elysium-API.git
cd Elysium-API
```

### 2. Depois vá para o arquivo ".env" e mude oque for necessário!

```yaml
mongodb://<usuário>:<senha>@<host>:<porta>/<nome_do_banco>?<O resto será gerado a partir daqui>

-- Mas mude oque for necessário.
```

### 3. Se necessário, crie novas rotas no arquivo "routes.ts"

```typescript
export async function routes(
  fastify: FastifyInstance,
  options: FastifyPluginOptions
) {
  fastify.get(
    "/nome_da_rota",
    async (request: FastifyRequest, reply: FastifyReply) => {
      return { Hello: "World!" };
    }
  );
}
```

### 4. Modifique o código como desejar!

Essa API é open-source, disponível para qualquer um que queira usá-la!

Espero que curtam!
