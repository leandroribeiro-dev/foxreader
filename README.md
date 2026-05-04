\# 🦊 FoxReader



Leitor de texto em voz (Text-to-Speech) baseado em HTML + JavaScript, utilizando a API nativa do navegador (`SpeechSynthesis`).



\---



\## 📌 Versão



\*\*V3.9.2\*\*



\---



\## 🚀 Funcionalidades



\### 🔊 Leitura

\- Leitura de texto em voz (TTS)

\- Controle de velocidade de leitura

\- Pausar, continuar e parar leitura

\- Retomada manual quando o navegador falha ao continuar a leitura

\- Controle refinado da retomada por frase

\- Início da leitura a partir de uma frase específica por clique no texto



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

\- Modo de edição preservado por padrão



\### 👁️ Leitura visual

\- Destaque da frase atual

\- Frases renderizadas como itens clicáveis

\- Acompanhamento visual com marcação amarela

\- Acompanhamento visual ligável/desligável

\- Rolagem automática removida para evitar avanço visual acelerado

\- Controle manual da barra de rolagem pelo usuário

\- Reposicionamento automático do texto ao iniciar, normalizar ou carregar arquivo

\- Espaçamento interno da caixa de texto ajustado

\- Melhor quebra de palavras longas

\- Seleção visual com fundo azul claro



\### 🖱️ Clique para ler

\- Botão \*\*Clique para ler: Ligado/Desligado\*\*

\- Recurso desligado por padrão

\- Quando desligado, a caixa de texto fica livre para edição

\- Quando ligado, clicar em uma frase inicia a leitura daquele ponto

\- Feedback visual do estado do botão

\- Mensagem de status indicando se o modo de clique está ativo ou inativo



\### 📊 Diagnóstico

\- Sistema de log interno

\- Exibição do log na interface

\- Exportação do log em `.txt`

\- Registro de estados internos da síntese de voz

\- Logs de retomada, pausa, continuação e avanço da frase atual

\- Log específico para início da leitura por clique

\- Log de ativação e desativação do modo \*\*Clique para ler\*\*



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

\- Detecção da posição/frase clicada para iniciar a leitura a partir de um ponto específico

\- Controle manual do modo de leitura por clique para evitar acionamentos acidentais



\---



\## 🧹 Limpeza de Markdown



A versão \*\*V3.9.2\*\* mantém o tratamento básico para arquivos Markdown iniciado na V3.8.



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



\## 🖱️ Leitura a partir de uma frase



A versão \*\*V3.9.2\*\* mantém a possibilidade de iniciar a leitura a partir de uma frase específica, mas agora esse recurso precisa ser ativado manualmente.



Funcionamento básico:



1\. O recurso \*\*Clique para ler\*\* inicia desligado.

2\. O usuário pode editar o texto normalmente.

3\. Ao ativar \*\*Clique para ler\*\*, o clique em uma frase passa a iniciar a leitura daquele ponto.

4\. O texto é dividido internamente em frases.

5\. Cada frase pode ser identificada pelo sistema.

6\. A leitura é iniciada a partir da frase selecionada.

7\. O destaque visual acompanha a frase atual, sem forçar a rolagem automática.



Esse ajuste evita que a leitura seja iniciada acidentalmente durante edições no texto.



\---



\## 🎨 Ajuste visual herdado da V3.9.1



A versão \*\*V3.9.2\*\* mantém os ajustes visuais da V3.9.1:



\- `padding` interno da caixa de texto

\- espaço extra à direita para evitar conflito com a barra de rolagem

\- `line-height` para melhorar a leitura

\- `word-break` para evitar estouro de palavras longas

\- cor de seleção do texto



\---



\## ⚠️ Observações



\- O funcionamento depende das vozes instaladas no sistema operacional.

\- Navegadores podem apresentar comportamentos diferentes.

\- Algumas vozes online podem falhar ou não suportar pausa/retomada corretamente.

\- A retomada manual pode repetir parte da frase atual para evitar perda de conteúdo.

\- A marcação visual foi ajustada para priorizar estabilidade em vez de avanço agressivo.

\- A rolagem automática continua removida; o usuário controla a posição do texto manualmente.

\- Blocos de código Markdown são simplificados para melhorar a leitura em voz alta.

\- O modo \*\*Clique para ler\*\* fica desligado por padrão para preservar a edição do texto.

\- A V3.9.2 é uma versão funcional de controle do recurso de leitura por clique.



\---



\## ▶️ Como usar



1\. Abra o arquivo `FoxReader.html` no navegador.

2\. Aguarde o carregamento das vozes.

3\. Escolha uma voz.

4\. Opcionalmente, clique em \*\*Mostrar todas\*\* para ampliar as opções.

5\. Cole, digite ou carregue um texto.

6\. Ao carregar arquivo `.md`, a limpeza básica de Markdown será aplicada automaticamente.

7\. Para texto colado manualmente, use \*\*Limpar Markdown\*\* se necessário.

8\. Clique em \*\*Ler texto\*\* para iniciar do começo.

9\. Para iniciar por uma frase específica, ative \*\*Clique para ler\*\*.

10\. Clique diretamente em uma frase para iniciar a leitura daquele ponto.

11\. Desative \*\*Clique para ler\*\* quando quiser editar o texto sem iniciar leitura acidentalmente.

12\. Use \*\*Pausar\*\*, \*\*Continuar\*\* ou \*\*Parar\*\* conforme necessário.

13\. Use \*\*Acompanhar\*\* para ligar ou desligar o destaque visual da leitura.

14\. Use \*\*Mostrar log\*\* para acompanhar diagnósticos internos.



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

\- Controle opcional de rolagem a cada grupo de frases

\- Dicionário técnico de pronúncia para termos de informática



\---



\## 👤 Autor



Leandro Ribeiro





