Desenvolvimento Mobile

📝 Descrição do Projeto/Atividade

Desenvolvimento de um aplicativo de previsão do tempo utilizando React Native e TypeScript, integrado a uma API para consultar informações climáticas em tempo real. O aplicativo permite pesquisar cidades e exibir dados como temperatura, clima e umidade.

🧠 Reflexão de Aprendizado

1. O que aprendi?

Aprendi a desenvolver aplicativos móveis utilizando React Native e TypeScript, criando componentes reutilizáveis e organizando melhor o código. Também aprendi a utilizar Hooks como useState e useEffect para gerenciar estados e executar ações automáticas, além de consumir APIs para buscar dados externos. Desenvolvi conhecimentos sobre estilização de telas, tratamento de erros e atualização dinâmica das informações exibidas ao usuário.

2. Para que serve (Por que aprendi)?

Aprender desenvolvimento mobile é importante porque grande parte dos usuários utiliza smartphones no dia a dia. Essa competência permite criar aplicativos para empresas e usuários finais, facilitando processos, aumentando a produtividade e oferecendo serviços digitais de forma prática e acessível. O mercado de trabalho busca cada vez mais profissionais capazes de desenvolver aplicações móveis modernas e eficientes.

🛠️ Tecnologias e Ferramentas Utilizadas

- React Native / Expo
- TypeScript
- Fetch API
- React Hooks (useState e useEffect)

💻 Demonstração e Como Rodar

Código Relevante Comentado

const fetchWeatherData = async (city: string) => {
  try {
    setLoading(true); // Inicia o carregamento

    const response = await fetch(
      `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=SUA_API_KEY`
    );

    const data = await response.json(); // Converte a resposta para JSON

    setWeather(data); // Atualiza os dados do clima
  } catch (err) {
    setError('Não foi possível carregar os dados de clima.');
  } finally {
    setLoading(false); // Finaliza o carregamento
  }
};

Instruções para Executar

1. Instale as dependências:

npm install

2. Inicialize o servidor do Expo:

npx expo start

3. Utilize o aplicativo Expo Go no celular ou um emulador Android/iOS para visualizar a aplicação.
