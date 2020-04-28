<h3 align="center">
  [GoStack7] | Projeto desenvolvido ao longo do curso
</h3>

---

## 📑 Sobre

**GoBarber** é uma aplicação que permite fornecedores de serviços (nesse caso, barbeiros) gerenciar sua agenda de atendimentos. A aplicação está dividida entre back end, front end e o mobile. O front end representa a visão do prestador de serviço, mostrando os horários em abertos, notificações sobre agendamentos, perfil do usuário e possibilidade de criar uma conta. O mobile permite que os usuários (clientes) possam agendar um serviço, selecionando o prestador e o horário disponível. Abaixo, seguem os links para as outras versões.

<h4 align="center">
  <a href="https://github.com/AugustoMarcelo/gobarber-frontend">Front end</a> | <a href="https://github.com/AugustoMarcelo/gobarber-mobile">Mobile</a>
</h4>

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
