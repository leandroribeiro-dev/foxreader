\# 📜 CHANGELOG

## [3.5] - 2026-05-01

### 🔧 Melhorado
- Scroll baseado em posição relativa da caixa (~30%), mais fluido e previsível
- Reset completo da leitura (scroll, índice e texto)
- Melhor consistência ao iniciar nova leitura

### 🧠 Lógica
- Controle interno de estado da leitura (leitura iniciada / pausa solicitada)
- Melhor tratamento de retomada (resume)
- Detecção de perda de estado de pausa

### 🧪 Diagnóstico
- Log da velocidade aplicada no início da leitura
- Logs mais descritivos no fluxo de execução

### ⚠️ Tratamento
- Feedback mais claro quando não é possível retomar leitura
- Tratamento mais robusto de falhas de voz e interrupções

---

## [3.4] - 2026-04-30

### ✨ Adicionado
- Controle de acompanhamento visual (ligar/desligar)
- Botão “Acompanhar” com estado dinâmico

### 🔧 Melhorado
- Scroll mais estável com posição fixa de leitura
- Melhor controle da posição da frase na tela
- Ajuste fino na rolagem (menos oscilações)

### 🧪 Diagnóstico
- Registro detalhado do estado do SpeechSynthesis
- Log de transições (start, pause, resume, end)
- Monitoramento de speaking / paused / pending

### ⚠️ Tratamento
- Tentativa automática de retomada ao falhar resume
- Feedback mais claro quando voz não suporta pausa

---
## [3.3] - 2026-04-30

### 🔧 Melhorado
- Scroll interno mais suave e controlado
- Redução de reposicionamento desnecessário
- Atualização de frase apenas quando muda

### 🧪 Diagnóstico
- Log mais limpo (menos ruído de boundary)
- Registro detalhado de erros por voz

### ⚠️ Tratamento
- Mensagens específicas para falha de voz
- Melhor feedback ao usuário

---


Todas as mudanças relevantes do projeto serão registradas aqui.


## [3.2] - 2026-04-30

### ✨ Adicionado

- Sistema de log interno
- Botão para mostrar/ocultar log
- Botão para baixar log em `.txt`

### 🔧 Melhorado

- Layout travado na tela
- Header compacto
- Remoção do quadro “Lendo agora”
- Scroll restrito à caixa de texto
- Marcador amarelo mantido diretamente no texto
- Melhor acompanhamento da frase durante a leitura

### 🧪 Diagnóstico

- Registro de eventos de leitura
- Registro de carregamento de vozes
- Registro de erros da SpeechSynthesis
- Registro de ações como pausar, continuar, parar e limpar texto

---

\## \[3.1] - Em desenvolvimento



\### ✨ Adicionado

\- Carregamento de arquivos `.txt` e `.md`

\- Cabeçalho fixo durante a leitura

\- Rodapé informativo da aplicação

\- Área de texto com rolagem interna



\### 🔧 Melhorado

\- Layout ajustado para melhor aproveitamento da tela

\- Scroll da frase marcada dentro da própria caixa de texto

\- Tratamento do campo de velocidade com vírgula ou ponto

\- Mensagem ao tentar continuar leitura sem pausa ativa



\---



\## \[3.0] - Em desenvolvimento



\### ✨ Adicionado

\- Destaque visual da frase sendo lida em tempo real

\- Exibição dinâmica do trecho atual em “Lendo agora”

\- Função de normalização de texto para melhor leitura

\- Botão para alternar entre vozes principais e todas as vozes

\- Scroll automático acompanhando a leitura



\### 🔧 Melhorado

\- Organização do layout e experiência do usuário (UI)

\- Lógica de leitura por frases

\- Controle e seleção de vozes

\- Tratamento de texto antes da leitura



\---



\## \[2.2] - 2026-04-29



\### 🚀 Adicionado

\- Checkbox para exibir vozes Online/Natural

\- Identificação visual do tipo de voz (\[Local] / \[Online/Natural])

\- Botão "Limpar texto"

\- Placeholder dinâmico na área de texto



\### 🧠 Melhorado

\- Controle manual da lista de vozes

\- Feedback mais claro no status (voz local vs online)

\- Refinamento na seleção de vozes em português



\### 🎨 Interface

\- Melhor organização dos controles

\- Ajuste na experiência de entrada de texto



\---



\## \[2.2] - Em desenvolvimento



\### 🚧 Em andamento

\- Estrutura inicial da nova versão

\- Preparação para melhorias e ajustes



\---



\## \[2.0] - 2026-04-29



\### 🚀 Adicionado

\- Interface completa com controles de leitura

\- Seleção dinâmica de vozes

\- Controle de velocidade (range)

\- Botões de controle (Ler, Pausar, Continuar, Parar)

\- Teste de voz

\- Recarregamento de vozes



\### 🧠 Melhorado

\- Filtro automático de vozes em português

\- Priorização de vozes locais (offline)

\- Exclusão de vozes instáveis (Online/Natural)

\- Fallback inteligente para vozes disponíveis



\### 🎨 Interface

\- Layout centralizado e limpo

\- Área de texto editável

\- Status dinâmico de leitura

\- Avisos orientativos ao usuário



\---



\## \[1.0] - Inicial



\### 🚀 Adicionado

\- Estrutura básica HTML

\- Leitura simples via SpeechSynthesis

