\# 🦊 FoxReader



Leitor de texto em voz (Text-to-Speech) baseado em HTML + JavaScript, utilizando a API nativa do navegador (`SpeechSynthesis`).



\---



\## 📌 Versão



\*\*V3.8\*\*



\---



\## 🚀 Funcionalidades



\### 🔊 Leitura

\- Leitura de texto em voz (TTS)

\- Controle de velocidade de leitura

\- Pausar, continuar e parar leitura

\- Retomada manual quando o navegador falha ao continuar a leitura

\- Controle refinado da retomada por frase



\### 🎧 Vozes

\- Seleção de vozes disponíveis no sistema

\- Filtro automático para vozes em português

\- Preferência por vozes locais (offline)

\- Alternância entre vozes principais e todas

\- Identificação: `\[Local]` / `\[Online/Natural]`



\### 📝 Entrada de texto

\- Área editável para digitação/colagem

\- Carregamento de arquivos `.txt` e `.md`

\- Limpeza automática de Markdown ao carregar arquivos `.md`

\- Botão manual \*\*Limpar Markdown\*\*

\- Normalização automática de texto

\- Limpeza rápida do conteúdo



\### 👁️ Leitura visual

\- Destaque da frase atual

\- Acompanhamento visual com marcação amarela

\- Acompanhamento visual ligável/desligável

\- Rolagem automática removida para evitar avanço visual acelerado

\- Controle manual da barra de rolagem pelo usuário

\- Reposicionamento automático do texto ao iniciar, normalizar ou carregar arquivo



\### 📊 Diagnóstico

\- Sistema de log interno

\- Exibição do log na interface

\- Exportação do log em `.txt`

\- Registro de estados internos da síntese de voz

\- Logs de retomada, pausa, continuação e avanço da frase atual



\---



\## 🧠 Inteligência aplicada



\- Filtragem automática de vozes `pt-BR`

\- Fallback inteligente:

&#x20; - Voz local → prioridade

&#x20; - Voz em português → alternativa

&#x20; - Outras vozes → último recurso

\- Classificação de vozes:

&#x20; - `\[Local]` → mais estáveis

&#x20; - `\[Online/Natural]` → melhor qualidade, porém menos confiáveis

\- Tratamento complementar para falhas de pausa/retomada

\- Controle de índice base para retomada manual

\- Controle temporal do avanço visual para reduzir marcações aceleradas

\- Limitação de avanço visual para evitar saltos bruscos entre frases

\- Limpeza básica de sintaxe Markdown para melhorar a leitura em voz alta



\---



\## 🧹 Limpeza de Markdown



A versão \*\*V3.8\*\* adiciona tratamento básico para arquivos Markdown.



Ao carregar um arquivo `.md`, o FoxReader remove ou simplifica elementos como:



\- títulos com `#`

\- negrito com `\*\*texto\*\*`

\- itálico com `\*texto\*`

\- código inline com crases

\- links no formato `\[texto](url)`

\- imagens no formato `!\[alt](url)`

\- citações com `>`

\- listas com `-`, `\*`, `+` ou numeração

\- linhas horizontais

\- separadores de tabela com `|`



O objetivo é evitar que o leitor de voz pronuncie símbolos de formatação durante o estudo.



\---



\## ⚠️ Observações



\- O funcionamento depende das vozes instaladas no sistema operacional.

\- Navegadores podem apresentar comportamentos diferentes.

\- Algumas vozes online podem falhar ou não suportar pausa/retomada corretamente.

\- A retomada manual pode repetir parte da frase atual para evitar perda de conteúdo.

\- A marcação visual foi ajustada para priorizar estabilidade em vez de avanço agressivo.

\- Na V3.8, a rolagem automática foi removida; o usuário controla a posição do texto manualmente.

\- Blocos de código Markdown são simplificados para melhorar a leitura em voz alta.



\---



\## ▶️ Como usar



1\. Abra o arquivo `FoxReader.html` no navegador.

2\. Aguarde o carregamento das vozes.

3\. Escolha uma voz.

4\. Opcionalmente, clique em \*\*Mostrar todas\*\* para ampliar as opções.

5\. Cole, digite ou carregue um texto.

6\. Ao carregar arquivo `.md`, a limpeza básica de Markdown será aplicada automaticamente.

7\. Para texto colado manualmente, use \*\*Limpar Markdown\*\* se necessário.

8\. Clique em \*\*Ler texto\*\*.

9\. Use \*\*Pausar\*\*, \*\*Continuar\*\* ou \*\*Parar\*\* conforme necessário.

10\. Use \*\*Acompanhar\*\* para ligar ou desligar o destaque visual da leitura.

11\. Use \*\*Mostrar log\*\* para acompanhar diagnósticos internos.



\---



\## 🛠️ Tecnologias



\- HTML5

\- CSS3

\- JavaScript

\- Web Speech API (`SpeechSynthesis`)



\---



\## 📂 Estrutura



```txt

/

├── FoxReader.html

├── README.md

├── CHANGELOG.md

└── legacy/

```



\---



\## 📈 Próximos passos (ideias)



\- Interface dark mode

\- Controle de pitch

\- Exportação de áudio

\- Persistência de configurações (voz/velocidade)

\- Separação futura de HTML, CSS e JavaScript

\- Melhorias adicionais no sistema de retomada por frase

\- Refinamento do comportamento entre diferentes navegadores e vozes

\- Ajuste mais inteligente para leitura de blocos de código Markdown



\---



\## 👤 Autor



Leandro Ribeiro 

