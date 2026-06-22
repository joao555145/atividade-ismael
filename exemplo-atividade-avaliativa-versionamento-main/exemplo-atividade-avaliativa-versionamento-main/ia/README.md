Inteligência Artificial (IA)

📝 Descrição do Projeto/Atividade

Desenvolvimento de um sistema simples de análise de sentimentos utilizando a API do Google Gemini em Python. O programa recebe um texto enviado pelo usuário e identifica se o sentimento é positivo, negativo ou neutro, utilizando inteligência artificial para interpretar a linguagem natural.

🧠 Reflexão de Aprendizado

1. O que aprendi?

Aprendi os conceitos básicos de Inteligência Artificial e de Modelos de Linguagem (LLMs), entendendo como eles podem interpretar textos e gerar respostas. Também aprendi a utilizar APIs de IA, criar prompts eficientes (Prompt Engineering) e processar as respostas geradas pelo modelo. Além disso, desenvolvi conhecimentos sobre automação de tarefas e integração de IA em aplicações reais.

2. Para que serve (Por que aprendi)?

Aprender Inteligência Artificial é importante porque ela está cada vez mais presente no mercado de trabalho. A IA pode automatizar tarefas complexas, analisar grandes quantidades de dados, gerar textos, classificar informações e auxiliar na tomada de decisões. Empresas utilizam essa tecnologia em chatbots, assistentes virtuais, análise de sentimentos, atendimento ao cliente e diversas outras aplicações, aumentando a eficiência e reduzindo custos.

🛠️ Tecnologias e Ferramentas Utilizadas

- Python
- Google Gemini API
- Biblioteca google-generativeai
- python-dotenv
- Engenharia de Prompts (Prompt Engineering)

💻 Demonstração e Como Rodar

Código Relevante Comentado

import google.generativeai as genai
import os

# Configura a chave da API
genai.configure(api_key=os.environ["GEMINI_API_KEY"])

# Define o modelo que será utilizado
model = genai.GenerativeModel('gemini-1.5-flash')

# Função para analisar o sentimento do texto
def analisar_sentimento(texto_cliente):
    prompt = f"""
    Analise o sentimento do seguinte texto.
    Responda apenas com:
    POSITIVO, NEGATIVO ou NEUTRO.

    Texto: {texto_cliente}
    """

    response = model.generate_content(prompt)

    return response.text.strip()

Instruções para Executar

1. Certifique-se de ter o Python instalado em seu computador.

2. Instale as dependências:

pip install google-generativeai python-dotenv

3. Crie um arquivo ".env" e adicione:

GEMINI_API_KEY=sua_chave_aqui

4. Execute o programa:

python app.py
