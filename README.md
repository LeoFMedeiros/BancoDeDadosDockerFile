# PostgreSQL com Docker: Guia Rápido

Passos para configurar e executar um banco de dados PostgreSQL usando Docker.

## 1. Clonar o Repositório

```bash
git clone https://github.com/LeoFMedeiros/BancoDeDadosDockerFile.git
cd BancoDeDadosDockerFile
```

## 2. Configurar Variáveis de Ambiente

Crie um arquivo chamado `.env` na raiz do projeto com o seguinte conteúdo. **Edite os valores** `seu_usuario`, `sua_senha_segura` e `seu_banco_de_dados`.

```env
# Configurações do PostgreSQL
POSTGRES_USER=seu_usuario
POSTGRES_PASSWORD=sua_senha_segura
POSTGRES_DB=seu_banco_de_dados
POSTGRES_PORT=5432
```


```bash
# Comando rápido para adicionar ao .gitignore
echo ".env" >> .gitignore
```

## 3. Executar com Docker Compose

Certifique-se de que o Docker e o Docker Compose estão instalados e execute:

```bash
docker-compose up -d
```

O comando `-d` executa em segundo plano.

## 4. Acessar o Banco

- **Host:** `localhost`
- **Porta:** `5432` (ou a definida em `POSTGRES_PORT`)
- **Usuário:** O valor de `POSTGRES_USER` no `.env`
- **Senha:** O valor de `POSTGRES_PASSWORD` no `.env`
- **Banco:** O valor de `POSTGRES_DB` no `.env`

## 5. Parar o Container

```bash
docker-compose down
``` 