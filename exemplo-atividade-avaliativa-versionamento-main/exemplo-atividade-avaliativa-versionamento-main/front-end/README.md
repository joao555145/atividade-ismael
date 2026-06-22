Desenvolvimento Front-end

📝 Descrição do Projeto/Atividade

Criação de um site responsivo para gerenciamento de finanças pessoais, permitindo registrar receitas e despesas, visualizar o saldo disponível e acompanhar as movimentações de forma simples e organizada. O projeto foi desenvolvido com HTML, CSS e JavaScript.

🧠 Reflexão de Aprendizado

1. O que aprendi?

Aprendi a estruturar páginas utilizando HTML5 de forma semântica, criar layouts modernos e responsivos com CSS3 utilizando Flexbox e Grid, além de adicionar interatividade com JavaScript. Também aprendi a manipular o DOM, criar funções para atualizar informações na tela e organizar melhor o código para facilitar a manutenção e evolução do projeto.

2. Para que serve (Por que aprendi)?

Aprender Front-end é essencial porque é a parte do sistema com a qual o usuário interage diretamente. Interfaces bonitas, acessíveis e responsivas melhoram a experiência do usuário, aumentam a facilidade de uso e tornam o produto mais atrativo. No mercado de trabalho, empresas valorizam profissionais capazes de criar aplicações modernas que funcionem bem em computadores e dispositivos móveis.

🛠️ Tecnologias e Ferramentas Utilizadas

- HTML5
- CSS3
- JavaScript (ES6+)
- Flexbox
- CSS Grid

💻 Demonstração e Como Rodar

Código Relevante Comentado

const updateUI = (transactions) => {
  const listElement = document.getElementById('transaction-list');

  // Limpa a lista anterior
  listElement.innerHTML = '';

  // Percorre todas as transações
  transactions.forEach(transaction => {
    const item = document.createElement('li');

    // Define a classe conforme o tipo
    item.classList.add(
      transaction.type === 'income'
      ? 'income-item'
      : 'expense-item'
    );

    // Exibe nome e valor
    item.innerHTML =
      `${transaction.name}
      <span>R$ ${transaction.amount.toFixed(2)}</span>`;

    listElement.appendChild(item);
  });
};

Instruções para Executar

Se for um projeto HTML, CSS e JavaScript:

1. Abra o arquivo "index.html" em seu navegador.

2. Ou utilize a extensão Live Server no VS Code para executar localmente.

Se utilizar Node.js ou Vite:

npm install
npm run dev

Acesse o endereço fornecido no terminal, como:

http://localhost:5173
