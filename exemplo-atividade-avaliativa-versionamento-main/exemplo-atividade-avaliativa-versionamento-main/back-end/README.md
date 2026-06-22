Desenvolvimento Back-end

📝 Descrição do Projeto/Atividade

Desenvolvimento de uma API RESTful para cadastro e autenticação de usuários, permitindo realizar operações de criação, consulta, atualização e exclusão de registros. O sistema foi desenvolvido utilizando Node.js, Express e TypeScript, com integração a banco de dados e recursos de segurança para proteção das informações.

🧠 Reflexão de Aprendizado

1. O que aprendi?

Aprendi os conceitos fundamentais do desenvolvimento Back-end, como criação de rotas HTTP (GET, POST, PUT e DELETE), tratamento de requisições e respostas do servidor, utilização de middlewares e integração com banco de dados. Também aprendi sobre autenticação de usuários, criptografia de senhas e organização da lógica de negócio para tornar a aplicação mais segura e eficiente.

2. Para que serve (Por que aprendi)?

O Back-end é responsável por toda a lógica de funcionamento de um sistema, sendo a parte que processa dados, aplica regras de negócio e se comunica com o banco de dados. Aprender essa área é essencial porque garante a segurança das informações, a integridade dos dados e o funcionamento correto das aplicações. Atualmente, APIs são amplamente utilizadas para conectar aplicativos, sites e serviços, tornando essa competência muito importante no mercado de tecnologia.

🛠️ Tecnologias e Ferramentas Utilizadas

- Node.js
- Express
- TypeScript
- JWT (JSON Web Token)
- bcryptjs
- SQLite

💻 Demonstração e Como Rodar

Código Relevante Comentado

app.post('/login', async (req, res) => {

  const { email, password } = req.body;

  const user = await database.findUserByEmail(email);

  // Verifica se o usuário existe e se a senha está correta
  if (!user || !(await bcrypt.compare(password, user.passwordHash))) {

    return res.status(401).json({
      error: 'Credenciais inválidas'
    });

  }

  // Gera um token de autenticação
  const token = jwt.sign(
    { userId: user.id },
    SECRET_KEY,
    { expiresIn: '1h' }
  );

  // Retorna o token para o cliente
  return res.json({ token });

});

Instruções para Executar

1. Instale as dependências:

npm install

2. Configure as variáveis de ambiente no arquivo ".env", se necessário.

3. Inicie o servidor:

npm start

Ou execute em modo de desenvolvimento:

npm run dev

4. Utilize ferramentas como Postman, Insomnia ou Thunder Client para testar as rotas da API.
