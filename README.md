<h3 align="center">
  [GoStack7] | Projeto desenvolvido ao longo do curso
</h3>

---

## ⚙ Tecnologias utilizadas

- NodeJS
- express
- postgres, redis e mongodb
- mongoose
- sequelize
- youch
- yup
- multer
- cors
- date-fns
- express-async-errors
- express-handlebars
- nodemailer
- nodemailer-express-handlerbars
- jsonwebtoken
- bcrypt
- nodemon

---

## 💻 Instruções para execução

- Caso esteja utilizando docker, poderá criar e inicializar sua base de dados com os comandos abaixo:
```bash
  # criando container com imagem do banco postgres
  docker run --name postgres -e POSTGRES_PASSWORD=postgres -d postgres

  # criando container com imagem do banco mongodb
  docker run --name mongo -d mongo

  # criando container com imagem do banco redis
  docker run --name redis -d redis

  # inicializando os bancos de dados
  docker start postgres mongo redis
```

- Faça o download do projeto:
```bash
  # clonando o repositório
  git clone https://github.com/AugustoMarcelo/gobarber-backend.git

  # acessando a pasta
  cd gobarber-backend

  # fazendo download das dependências
  yarn
```

- Usando o arquivo `.env.example` como modelo, crie um arquivo `.env` na raiz do projeto e preencha com os dados requisitados.

- Para criar as tabelas, execute o seguinte comando:
```bash
  # criando as tabelas no banco de dados
  yarn sequelize db:migrate

  # criando um usuário administrador: email: admin@gobarber.com e senha: 123456
  yarn sequelize db:seed:all
```

- Com o banco de dados rodando e as tabelas criadas, inicialize a aplicação e o sistema de filas para envio de e-mails:
```bash
  # inicializando servidor
  yarn dev

  # inicializando fila de e-mails
  yarn queue
```
