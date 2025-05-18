# Sistema de Criação de Jogos "Escolha sua Aventura" com Agentes

Este projeto utiliza múltiplos agentes com modelos de linguagem para gerar um jogo interativo no estilo "Escolha sua Aventura" baseado em um tema e nome de personagem fornecidos pelo usuário.

## Como Funciona

O sistema opera em uma cadeia de quatro agentes, cada um com uma função específica:

1.  **Agente Redator:** Cria a história inicial, com começo, meio e fim, e múltiplos finais possíveis, baseando-se no tema e nome do personagem principal.
2.  **Agente Conversor:** Transforma a história linear em um roteiro estruturado para um jogo "Escolha sua Aventura", dividindo-a em cenas com opções de escolha e caminhos ramificados.
3.  **Agente Revisor:** Revisa o roteiro adaptado, aprimorando o tone, a emoção e a coerência lógica da narrativa interativa.
4.  **Agente Gerador de Código:** Converte o roteiro revisado em código Python funcional para um jogo jogável via terminal.

## Tecnologias Utilizadas

*   **Google Gemini:** Utilizado como modelo de linguagem para os agentes.
*   **Google ADK (Agent Development Kit):** Framework utilizado para criar e gerenciar os agentes.
*   **Python:** Linguagem de programação principal do projeto.
*   **Bibliotecas Python:** `IPython`, `google.genai`, `google.adk`, `datetime`, `textwrap`, `requests`, `warnings`, `time`, `sys`.

## Como Usar (em Google Colab)

1.  **Configure a API Key:** Certifique-se de ter sua chave de API do Google Gemini configurada no Google Colab usando `userdata.get('GOOGLE_API_KEY')`.
2.  **Instale as Dependências:** O notebook instala as bibliotecas necessárias (`google-genai` e `google-adk`).
3.  **Execute as Células:** Execute todas as células do notebook em sequência.
4.  **Forneça as Entradas:** Quando solicitado, digite o tema do jogo e o nome do personagem principal.
5.  **Veja os Resultados:** O notebook exibirá os resultados de cada agente, culminando no código Python final do jogo.
6.  **Jogue o Jogo Gerado:** Copie o código Python gerado pelo Agente 4 e cole-o em um novo arquivo `.py` ou em uma nova célula de código no Colab para rodar o jogo.

## Estrutura do Código

O código é modular, com funções definidas para cada agente (`agente_redator`, `agente_conversor`, `agente_revisor`, `agente_gerador`). Uma função auxiliar (`call_agent`) é utilizada para interagir com os agentes via `Runner`. Outra função (`to_markdown`) é usada para formatar a saída no Colab. A execução principal do script guia o usuário através do processo de criação do jogo.
