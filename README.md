# 🦊 FoxReader

Leitor de texto em voz (Text-to-Speech) baseado em HTML + JavaScript, utilizando a API nativa do navegador (SpeechSynthesis).

---

## 📌 Versão

**V3.5**

---

## 🚀 Funcionalidades

### 🔊 Leitura
- Leitura de texto em voz (TTS)
- Controle de velocidade de leitura
- Pausar, continuar e parar leitura
- Teste rápido de voz

### 🎧 Vozes
- Seleção de vozes disponíveis no sistema
- Filtro automático para vozes em português
- Preferência por vozes locais (offline)
- Alternância entre vozes principais e todas
- Identificação: `[Local]` / `[Online/Natural]`

### 📝 Entrada de texto
- Área editável para digitação/colagem
- Carregamento de arquivos `.txt` e `.md`
- Normalização automática de texto
- Limpeza rápida do conteúdo

### 👁️ Leitura visual
- Destaque da frase atual
- Scroll automático durante leitura
- Acompanhamento visual (ligar/desligar)

### 📊 Diagnóstico
- Sistema de log interno
- Exibição do log na interface
- Exportação do log em `.txt`

---

## 🧠 Inteligência aplicada

- Filtragem automática de vozes `pt-BR`
- Fallback inteligente:
  - Voz local → prioridade
  - Voz em português → alternativa
  - Outras vozes → último recurso
- Classificação de vozes:
  - `[Local]` → mais estáveis
  - `[Online/Natural]` → melhor qualidade, porém menos confiáveis

---

## ⚠️ Observações

- Depende das vozes instaladas no sistema operacional
- Navegadores podem apresentar comportamentos diferentes
- Algumas vozes online podem falhar ou não suportar pausa/retomada

---

## ▶️ Como usar

1. Abra o arquivo `FoxReader.html` no navegador  
2. Aguarde o carregamento das vozes  
3. Escolha uma voz  
4. (Opcional) Clique em **Mostrar todas** para ampliar as opções  
5. Cole, digite ou carregue um texto  
6. Clique em **Ler texto**

---

## 🛠️ Tecnologias

- HTML5  
- CSS3  
- JavaScript  
- Web Speech API (SpeechSynthesis)

---

## 📂 Estrutura

```txt
/
├── FoxReader.html
├── README.md
├── CHANGELOG.md
└── legacy/
```

## 📈 Próximos passos (ideias)
- Interface dark mode
- Controle de pitch
- Exportação de áudio
- Persistência de configurações (voz/velocidade)

## 👤 Autor

Leandro Ribeiro

