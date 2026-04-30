# 🦊 FoxReader

Leitor de texto em voz (Text-to-Speech) baseado em HTML + JavaScript, utilizando a API nativa do navegador (SpeechSynthesis).

## 📌 Versão

Atualizar versão → **V3.3**

---

## 🚀 Funcionalidades

- Leitura de texto em voz (TTS)
- Seleção de vozes disponíveis no sistema
- Filtro automático para vozes em português
- Preferência por vozes locais (offline)
- Controle de velocidade de leitura
- Botões de controle:
  - ▶ Ler
  - ⏸ Pausar
  - ▶ Continuar
  - ⛔ Parar
- Teste de voz
- Recarregar vozes
- Área editável para inserção de texto
- Opção para exibir vozes Online/Natural
- Identificação visual de tipo de voz ([Local] / [Online/Natural])
- Botão para limpar texto
- Placeholder dinâmico na área de texto
- Exibição do trecho atual sendo lido
- Scroll automático durante a leitura
- Normalização de texto
- Alternância entre vozes principais e todas as vozes
- Carregamento de arquivos `.txt` e `.md`
- Cabeçalho fixo durante o uso
- Área de leitura com altura ajustada à tela
- Rodapé informativo da aplicação
- Melhor suporte a valores de velocidade com vírgula ou ponto
- Layout estável com altura travada na tela
- Scroll interno apenas na área de leitura
- Remoção do quadro separado “Lendo agora”
- Destaque da frase atual diretamente no texto
- Sistema de log interno
- Botão para mostrar/ocultar log
- Botão para baixar log em `.txt`
- Scroll mais inteligente na leitura
- Redução de atualizações desnecessárias
- Melhor tratamento de erros de voz

---

## 🧠 Inteligência aplicada

- Filtragem automática de vozes `pt-BR`
- Exclusão de vozes instáveis (`Online`, `Natural`)
- Fallback inteligente:
  - Voz local em português → prioridade
  - Voz em português → alternativa
  - Todas as vozes → último recurso
- Classificação de vozes:
  - [Local] → mais estáveis
  - [Online/Natural] → melhor qualidade, porém instáveis
- Controle manual para exibir ou ocultar vozes online

---

## ⚠️ Observações

- O funcionamento depende das vozes instaladas no sistema operacional
- Navegadores podem ter comportamentos diferentes
- Algumas vozes online podem falhar

---

## ▶️ Como usar

1. Abra o arquivo `FoxReader.html` no navegador
2. Aguarde o carregamento das vozes
3. Escolha uma voz
3.1 (Opcional) Marque "Mostrar vozes Online/Natural" para ampliar as opções
4. Cole ou digite o texto
5. Clique em **Ler texto**

---

## 🛠️ Tecnologias

- HTML5
- CSS3
- JavaScript
- Web Speech API (SpeechSynthesis)

---

## 📂 Estrutura
/
├── FoxReader.html
├── README.md
├── CHANGELOG.md
└── legacy/


---

## 📈 Próximos passos (ideias)

- Destaque de texto em tempo real
- Interface dark mode
- Controle de pitch
- Exportação de áudio

---

## 👤 Autor

Leandro Ribeiro
