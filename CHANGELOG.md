# 📜 CHANGELOG

Todas as mudanças relevantes do projeto serão registradas aqui.

## [3.9.3] - Em desenvolvimento

### ✨ Adicionado
- Botão \*\*Pronúncia técnica: Ligada/Desligada\*\*.
- Variável `pronunciaTecnicaAtiva` para controlar o estado do recurso.
- Função `alternarPronunciaTecnica()` para ativar ou desativar a adaptação de termos técnicos.
- Função `substituirTermoTecnico()` para substituir termos específicos antes da fala.
- Função `aplicarPronunciaTecnica()` para aplicar o dicionário técnico ao texto lido.
- Dicionário inicial de pronúncia para termos comuns de informática.
- Log do estado da pronúncia técnica no início da leitura.

### 🔧 Melhorado
- Leitura de textos técnicos com termos em inglês.
- Compreensão auditiva de conteúdos mistos em português e informática.
- Controle do usuário sobre a adaptação fonética dos termos.
- Experiência de estudo com textos sobre programação, web, banco de dados, Git e Docker.
- Preservação do texto visual original durante a leitura.

### 🧠 Lógica
- O texto visual permanece inalterado na caixa de leitura.
- A adaptação técnica é aplicada apenas no texto enviado ao `SpeechSynthesis`.
- Antes da criação do `SpeechSynthesisUtterance`, o sistema gera `textoParaFala`.
- Quando a pronúncia técnica está ligada, termos técnicos são substituídos por versões fonéticas.
- Quando a pronúncia técnica está desligada, o texto é enviado para fala sem adaptações.
- A lógica de leitura, pausa, retomada e clique por frase foi preservada.

### 🗣️ Pronúncia técnica
- Adicionadas substituições para termos como `frontend`, `backend`, `framework`, `deploy`, `debug`, `commit`, `push`, `pull`, `merge`, `branch`, `endpoint`, `script`, `server`, `client`, `browser`, `dashboard`, `database`, `query`, `array`, `string`, `boolean`, `JSON`, `REST`, `API`, `HTTP`, `HTML`, `CSS`, `JavaScript`, `PHP`, `SQL`, `MySQL`, `MariaDB`, `Git`, `GitHub` e `Docker`.
- O recurso foi criado para reduzir pronúncias estranhas geradas por vozes em português ao ler termos técnicos em inglês.
- O botão permite comparação direta entre leitura original e leitura adaptada.

### 🎨 Interface
- Adicionado botão \*\*Pronúncia técnica: Ligada\*\* junto aos controles principais.
- O botão usa estado visual ligado/desligado com as classes já existentes.
- O texto do botão alterna entre \*\*Pronúncia técnica: Ligada\*\* e \*\*Pronúncia técnica: Desligada\*\*.
- Mantido o layout visual da V3.9.2.
- Mantidos os botões de leitura, Markdown, acompanhamento e clique para ler.

### 🧪 Diagnóstico
- Adicionado registro de status ao ligar ou desligar a pronúncia técnica.
- Adicionado log indicando se a pronúncia técnica está ligada ou desligada ao iniciar leitura.
- Mantidos os logs de leitura por clique.
- Mantidos os logs de leitura, pausa, continuação, erro e conclusão.

### ⚠️ Tratamento
- A adaptação fonética não altera o texto exibido ao usuário.
- O recurso pode ser desligado quando a leitura original for preferível.
- Preserva o modo edição como padrão inicial.
- Preserva o controle manual de clique para ler.
- Preserva os ajustes visuais da V3.9.1.
- Preserva a limpeza de Markdown adicionada na V3.8.

---

## [3.9.2] - Em desenvolvimento

### ✨ Adicionado
- Botão \*\*Clique para ler: Ligado/Desligado\*\*.
- Variável `cliqueParaLerAtivo` para controlar o estado do recurso.
- Função `alternarCliqueParaLer()` para ativar ou desativar a leitura por clique.
- Feedback visual do botão conforme o estado do recurso.
- Mensagens de status para indicar modo edição ou modo clique ativo.
- Título auxiliar na caixa de texto indicando o modo atual.

### 🔧 Melhorado
- Fluxo de edição dentro da caixa de texto.
- Controle do recurso de leitura por clique.
- Prevenção de leitura acidental durante edição do texto.
- Clareza da interface sobre quando o clique inicia leitura.
- Subtítulo da aplicação, orientando que o clique precisa ser ativado.

### 🧠 Lógica
- O clique para leitura passou a ficar desligado por padrão.
- O evento de clique na caixa de texto agora verifica `cliqueParaLerAtivo` antes de iniciar a leitura.
- Quando o recurso está desligado, o clique apenas permite edição normal do texto.
- Quando o recurso está ligado, o clique inicia a leitura a partir da frase selecionada.
- A leitura por clique continua reutilizando a lógica de retomada por frase.

### 🎨 Interface
- Adicionado botão específico para controlar o modo \*\*Clique para ler\*\*.
- O botão usa estado visual ligado/desligado com as classes já existentes.
- O texto do botão alterna entre \*\*Clique para ler: Ligado\*\* e \*\*Clique para ler: Desligado\*\*.
- Mantido o layout visual da V3.9.1.

### 🧪 Diagnóstico
- Adicionado registro de status ao ligar ou desligar o modo de clique.
- Mantidos os logs de leitura por clique adicionados na V3.9.
- Mantidos os logs de leitura, pausa, continuação, erro e conclusão.

### ⚠️ Tratamento
- Evita acionamento acidental da leitura enquanto o usuário edita o conteúdo.
- Preserva o modo edição como padrão inicial.
- Mantém a leitura por clique disponível quando ativada manualmente.
- Preserva os ajustes visuais da V3.9.1.
- Preserva a limpeza de Markdown adicionada na V3.8.

---

## [3.9.1] - Em desenvolvimento

### 🎨 Interface
- Ajustado o espaçamento interno da caixa de texto.
- Adicionado espaço extra no lado direito para reduzir conflito visual com a barra de rolagem.
- Adicionado `line-height: 1.7` diretamente na caixa de leitura.
- Adicionado `word-break: break-word` para evitar estouro de palavras longas.
- Adicionada cor de seleção personalizada com `.box::selection`.

### 🔧 Melhorado
- Conforto visual durante leitura de textos longos.
- Distância entre texto, borda e barra de rolagem.
- Quebra de linhas em conteúdos com palavras extensas ou termos técnicos.
- Aparência da seleção de texto dentro da área editável.

### 🧠 Lógica
- Nenhuma alteração funcional na lógica de leitura.
- Mantida a leitura por clique adicionada na V3.9.
- Mantida a limpeza de Markdown adicionada na V3.8.
- Mantida a rolagem automática removida.

### ⚠️ Tratamento
- Redução do risco de texto colado ou visualmente sobreposto à borda da caixa.
- Melhor comportamento visual em textos técnicos com palavras longas.
- Preservação da estrutura de leitura e retomada já existente.

---

[3.9] - Em desenvolvimento

### ✨ Adicionado
- Estilo `.frase-item` para transformar frases em elementos clicáveis.
- Função `prepararFrasesParaClique()` para preparar o texto antes da leitura por clique.
- Função `obterIndiceFraseDoClique()` para identificar a frase selecionada pelo usuário.
- Função `localizarFrasePorCaracterNoTextoCompleto()` para localizar a frase pela posição do cursor.
- Função `iniciarLeituraPeloClique()` para iniciar a leitura a partir da frase clicada.
- Evento de clique na caixa de texto para acionar a leitura a partir de um ponto específico.

### 🔧 Melhorado
- Fluxo de leitura em textos longos, permitindo retomar a partir de uma frase intermediária.
- Experiência de estudo, reduzindo a necessidade de reiniciar a leitura desde o começo.
- Texto visual passou a ser renderizado com frases individualizadas quando o acompanhamento está ativo.
- Subtítulo da interface atualizado para informar o uso do clique em frases.

### 🧠 Lógica
- O texto é dividido em frases antes da identificação do clique.
- Cada frase renderizada recebe o atributo `data-indice-frase`.
- O clique em uma frase permite reconstruir a leitura a partir daquele índice.
- Quando o clique ocorre fora de uma frase marcada, o sistema tenta localizar a frase pela posição do cursor.
- A leitura por clique reutiliza a lógica de retomada já existente.

### 🎨 Interface
- Frases receberam cursor visual de clique.
- Frases passaram a ter destaque visual ao passar o mouse.
- O destaque amarelo da frase atual foi mantido.
- A rolagem automática continua removida.
- O layout visual da V3.8 foi preservado.

### 🧪 Diagnóstico
- Adicionado log para registrar a frase escolhida por clique.
- Adicionado log quando não for possível identificar a frase clicada.
- Mantidos os logs de leitura, pausa, continuação, erro e conclusão.
- Mantido o registro da frase atual durante o acompanhamento visual.

### ⚠️ Tratamento
- Validação de texto vazio antes de preparar frases para clique.
- Validação do índice da frase clicada antes de iniciar a leitura.
- Tratamento alternativo quando o clique não ocorre diretamente sobre uma frase renderizada.
- Preservação da limpeza de Markdown adicionada na V3.8.
- Preservação da leitura sem rolagem automática.

---

## [3.8] - Em desenvolvimento

### ✨ Adicionado

- Função `limparMarkdown()` para remover ou simplificar sintaxe Markdown antes da leitura.
- Função `limparMarkdownDoBox()` para aplicar limpeza Markdown manualmente no texto exibido.
- Botão \*\*Limpar Markdown\*\* na interface.
- Limpeza automática de arquivos `.md` durante o carregamento.


### 🔧 Melhorado

- Leitura de arquivos Markdown, evitando que símbolos como `#`, `\*`, crases e pipes sejam pronunciados.
- Fluxo de carregamento de arquivos `.md`, agora com tratamento específico.
- Experiência de estudo com textos vindos de anotações, apostilas e arquivos Markdown.
- Controle visual da leitura, mantendo o destaque da frase atual sem forçar a rolagem automática.


### 🧠 Lógica

- Arquivos `.md` passam por pré-processamento antes de serem exibidos na caixa de texto.
- Textos colados manualmente podem ser tratados pelo botão \*\*Limpar Markdown\*\*.
- O destaque amarelo da frase atual foi mantido.
- A rolagem automática do marcador foi removida.
- O usuário passa a controlar manualmente a posição da barra de rolagem.


### 🎨 Interface

- Adicionado botão \*\*Limpar Markdown\*\* junto aos controles principais.
- Mantido o layout visual da V3.7.
- Mantido o espaçamento interno ampliado da caixa de texto.
- Alterado `scroll-behavior` da caixa de texto para `auto`.


### 🧪 Diagnóstico

- Mantidos os logs de leitura, pausa, continuação, erro e conclusão.
- Mantido o registro da frase atual durante o acompanhamento visual.
- Adicionado feedback de status ao carregar e limpar arquivos Markdown.


### ⚠️ Tratamento

- Títulos Markdown com `#` são convertidos em texto comum.
- Marcações de negrito e itálico são removidas mantendo o conteúdo.
- Links Markdown são convertidos para o texto visível.
- Imagens Markdown são simplificadas pelo texto alternativo.
- Citações, listas, linhas horizontais e separadores de tabela são limpos ou simplificados.
- Blocos de código Markdown são simplificados como “bloco de código”.

---

## [3.7] - Em desenvolvimento


### ✨ Adicionado

- Controle de índice base da leitura com `indiceBaseLeitura`.
- Controle temporal do avanço visual com `ultimoAvancoVisual`.
- Intervalo mínimo entre avanços visuais com `intervaloMinimoAvancoVisual`.
- Função `localizarFrasePorCaracterNoTrecho()` para localizar frases considerando retomadas parciais.
- Função `podeAtualizarMarcador()` para evitar atualizações visuais excessivas.
- Função `limitarAvancoVisual()` para impedir saltos bruscos entre frases.


### 🔧 Melhorado

- Ajuste do espaçamento interno da caixa de texto.
- Reposicionamento inicial do texto usando `requestAnimationFrame()`.
- Controle visual da frase atual durante a leitura.
- Comportamento da retomada manual após pausa.
- Sincronia entre leitura, frase marcada e rolagem interna.
- Estabilidade do acompanhamento visual em textos longos.


### 🧠 Lógica

- A leitura passou a controlar melhor o ponto de retomada por frase.
- A marcação visual agora evita retrocessos e avanços repetidos.
- O marcador não avança mais para frases anteriores à frase atual.
- O avanço visual passou a ser limitado a uma frase por atualização.
- A retomada manual passou a usar uma base de índice para localizar corretamente o trecho em leitura.



### 🧪 Diagnóstico

- Registro da frase atual com base no índice real da leitura.
- Logs de retomada manual mantidos para análise do comportamento da voz.
- Melhor rastreamento do fluxo entre `onstart`, `onboundary`, `onerror` e `onend`.


### 🎨 Interface

- Removido o botão \*\*Testar voz\*\*.
- Caixa de texto recebeu maior espaçamento vertical interno.
- Interface ficou mais focada nas ações principais de leitura.


### ⚠️ Tratamento

- Prevenção contra índice de frase inválido na renderização.
- Reset de `indiceBaseLeitura` ao finalizar, parar, limpar, normalizar ou carregar novo arquivo.
- Redução de saltos visuais causados por múltiplos eventos `boundary`.
- Priorização da estabilidade visual em vez de atualização agressiva da marcação.

--- 

## Resumo técnico


A versão **V3.7** refinou o acompanhamento visual da leitura.

O foco principal foi controlar melhor o avanço da frase marcada, especialmente durante pausas, retomadas e eventos rápidos gerados pela `SpeechSynthesis`.

Esta versão representa uma etapa intermediária de estabilização da leitura visual, ainda dentro do ciclo evolutivo da série V3.x.

---

## [3.6] - Em desenvolvimento

### 🔧 Melhorado
- Reposicionamento mais confiável da caixa de texto ao iniciar leitura.
- Retorno automático ao topo após normalizar texto.
- Retorno automático ao topo após carregar arquivos `.txt` ou `.md`.
- Melhor organização interna do fluxo de leitura.

### 🧠 Lógica
- Criação da função `irParaInicioDoTexto()` para centralizar o reposicionamento visual.
- Criação da função `prepararLeitura()` para centralizar leitura normal e retomada.
- Criação da função `montarTextoAPartirDaFrase()` para reconstruir o texto a partir de uma frase específica.
- Criação da função `retomarManual()` para fallback quando o `resume()` nativo falha.
- Transformação da função `falar()` em chamada simplificada para `prepararLeitura()`.

### 🧪 Diagnóstico
- Log específico para reposicionamento do box de texto.
- Log de retomada manual com índice da frase atual.
- Melhor rastreamento do comportamento de pausa/continuação.

### ⚠️ Tratamento
- Quando `speechSynthesis.resume()` falha, o sistema tenta retomar manualmente.
- Quando o navegador perde o estado de pausa, o sistema tenta recuperar o fluxo.
- A retomada manual usa a frase atual para evitar perda de conteúdo.

---

## [3.5] - 2026-05-01

### 🔧 Melhorado
- Scroll baseado em posição relativa da caixa (~30%), mais fluido e previsível.
- Reset completo da leitura (scroll, índice e texto).
- Melhor consistência ao iniciar nova leitura.

### 🧠 Lógica
- Controle interno de estado da leitura (leitura iniciada / pausa solicitada).
- Melhor tratamento de retomada (`resume`).
- Detecção de perda de estado de pausa.

### 🧪 Diagnóstico
- Log da velocidade aplicada no início da leitura.
- Logs mais descritivos no fluxo de execução.

### ⚠️ Tratamento
- Feedback mais claro quando não é possível retomar leitura.
- Tratamento mais robusto de falhas de voz e interrupções.

---

## [3.4] - 2026-04-30

### ✨ Adicionado
- Controle de acompanhamento visual (ligar/desligar).
- Botão “Acompanhar” com estado dinâmico.

### 🔧 Melhorado
- Scroll mais estável com posição fixa de leitura.
- Melhor controle da posição da frase na tela.
- Ajuste fino na rolagem (menos oscilações).

### 🧪 Diagnóstico
- Registro detalhado do estado do `SpeechSynthesis`.
- Log de transições (`start`, `pause`, `resume`, `end`).
- Monitoramento de `speaking`, `paused` e `pending`.

### ⚠️ Tratamento
- Tentativa automática de retomada ao falhar `resume`.
- Feedback mais claro quando a voz não suporta pausa.

---

## [3.3] - 2026-04-30

### 🔧 Melhorado
- Scroll interno mais suave e controlado.
- Redução de reposicionamento desnecessário.
- Atualização de frase apenas quando muda.

### 🧪 Diagnóstico
- Log mais limpo, com menos ruído de `boundary`.
- Registro detalhado de erros por voz.

### ⚠️ Tratamento
- Mensagens específicas para falha de voz.
- Melhor feedback ao usuário.

---

## [3.2] - 2026-04-30

### ✨ Adicionado
- Sistema de log interno.
- Botão para mostrar/ocultar log.
- Botão para baixar log em `.txt`.

### 🔧 Melhorado
- Layout travado na tela.
- Header compacto.
- Remoção do quadro “Lendo agora”.
- Scroll restrito à caixa de texto.
- Marcador amarelo mantido diretamente no texto.
- Melhor acompanhamento da frase durante a leitura.

### 🧪 Diagnóstico
- Registro de eventos de leitura.
- Registro de carregamento de vozes.
- Registro de erros da `SpeechSynthesis`.
- Registro de ações como pausar, continuar, parar e limpar texto.

---

## [3.1] - Em desenvolvimento

### ✨ Adicionado
- Carregamento de arquivos `.txt` e `.md`.
- Cabeçalho fixo durante a leitura.
- Rodapé informativo da aplicação.
- Área de texto com rolagem interna.

### 🔧 Melhorado
- Layout ajustado para melhor aproveitamento da tela.
- Scroll da frase marcada dentro da própria caixa de texto.
- Tratamento do campo de velocidade com vírgula ou ponto.
- Mensagem ao tentar continuar leitura sem pausa ativa.

---

## [3.0] - Em desenvolvimento

### ✨ Adicionado
- Destaque visual da frase sendo lida em tempo real.
- Exibição dinâmica do trecho atual em “Lendo agora”.
- Função de normalização de texto para melhor leitura.
- Botão para alternar entre vozes principais e todas as vozes.
- Scroll automático acompanhando a leitura.

### 🔧 Melhorado
- Organização do layout e experiência do usuário (UI).
- Lógica de leitura por frases.
- Controle e seleção de vozes.
- Tratamento de texto antes da leitura.

---

## [2.2] - 2026-04-29

### 🚀 Adicionado
- Checkbox para exibir vozes Online/Natural.
- Identificação visual do tipo de voz (`[Local]` / `[Online/Natural]`).
- Botão "Limpar texto".
- Placeholder dinâmico na área de texto.

### 🧠 Melhorado
- Controle manual da lista de vozes.
- Feedback mais claro no status (voz local vs online).
- Refinamento na seleção de vozes em português.

### 🎨 Interface
- Melhor organização dos controles.
- Ajuste na experiência de entrada de texto.

---

## [2.0] - 2026-04-29

### 🚀 Adicionado
- Interface completa com controles de leitura.
- Seleção dinâmica de vozes.
- Controle de velocidade.
- Botões de controle (Ler, Pausar, Continuar, Parar).
- Teste de voz.
- Recarregamento de vozes.

### 🧠 Melhorado
- Filtro automático de vozes em português.
- Priorização de vozes locais (offline).
- Exclusão de vozes instáveis (`Online` / `Natural`).
- Fallback inteligente para vozes disponíveis.

### 🎨 Interface
- Layout centralizado e limpo.
- Área de texto editável.
- Status dinâmico de leitura.
- Avisos orientativos ao usuário.

---

## [1.0] - Inicial

### 🚀 Adicionado
- Estrutura básica HTML.
- Leitura simples via `SpeechSynthesis`.
