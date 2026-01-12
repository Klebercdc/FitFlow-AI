# FitFlow AI - App de Treino com Chat Inteligente

## 🏋️ Sobre

FitFlow AI é um aplicativo moderno de rastreamento de treinos que integra a tecnologia de IA NVIDIA Nemotron para fornecer sugestões personalizadas de exercícios e orientações de fitness em tempo real.

**Recursos principais:**
- 📱 Interface responsiva para registro de exercícios
- 🤖 Chat AI com NVIDIA Nemotron para recomendações de treino
- 📊 Histórico de treinos com armazenamento local
- 🔒 Dados verificados de fontes oficiais de fitness
- ⚡ Deploy automático em Vercel

## 🚀 Quick Start - Deploy em Vercel

### Pré-requisitos
1. Conta em [Vercel](https://vercel.com)
2. Chave API NVIDIA Nemotron (obtida em [build.nvidia.com](https://build.nvidia.com))
3. Conta GitHub

### Passos para Deploy

1. **Fork/Clone este repositório**
   ```bash
   git clone https://github.com/Klebercdc/FitFlow-AI.git
   cd FitFlow-AI
   ```

2. **Fazer deploy em Vercel**
   - Acesse [vercel.com/new](https://vercel.com/new)
   - Conecte seu repositório GitHub
   - Selecione `FitFlow-AI`
   - Adicione as variáveis de ambiente:
     - `NVIDIA_API_KEY`: Sua chave API NVIDIA
   - Clique em "Deploy"

3. **Acessar a aplicação**
   - Seu app estará disponível em `https://<seu-projeto>.vercel.app`

## 🔑 Configuração da Chave NVIDIA

### Obtendo a Chave API

1. Acesse [build.nvidia.com](https://build.nvidia.com)
2. Faça login ou crie uma conta
3. Vá para "API Keys" nas configurações
4. Clique em "Create New Key"
5. Copie a chave gerada

### Adicionando ao Vercel

1. Acesse seu projeto em [vercel.com](https://vercel.com)
2. Vá para "Settings" → "Environment Variables"
3. Adicione:
   - **Name:** `NVIDIA_API_KEY`
   - **Value:** Sua chave API
4. Clique "Save" e redeploy o projeto

## 📚 Estrutura do Projeto

```
FitFlow-AI/
├── index.html          # Interface frontend
├── api/
│   └── chat.js        # Handler da API NVIDIA
├── package.json       # Dependências do projeto
├── vercel.json        # Configuração Vercel
└── README.md          # Este arquivo
```

## 💡 Como Funciona

### Frontend (index.html)
- Interface com dois painéis: Rastreador de Treinos + Chat AI
- Armazena dados localmente usando localStorage
- Comunicação com o backend via fetch API

### Backend (api/chat.js)
- Serverless function rodando em Vercel
- Recebe mensagens do usuário
- Consulta NVIDIA Nemotron com prompts baseados em dados oficiais
- Retorna respostas em português

## 🎯 Fontes de Dados Confiáveis

A IA foi configurada para:
- Consultar orientações oficiais de fitness e nutrição
- Basear-se em dados verificados de organizações como:
  - American College of Sports Medicine (ACSM)
  - Organização Mundial da Saúde (OMS)
  - Instituições de pesquisa de fitness reconhecidas
- Evitar informações especulativas ou não verificadas
- Sempre citar fontes quando possível

## 🛠️ Desenvolvimento Local

### Instalação

```bash
npm install
```

### Rodando localmente

```bash
npm run dev
```

Acesse `http://localhost:3000` no seu navegador.

## 📝 Variáveis de Ambiente

Crie um arquivo `.env.local` para desenvolvimento:

```env
NVIDIA_API_KEY=sua_chave_aqui
```

## 🔒 Segurança

- A chave API NVIDIA nunca é exposta ao cliente
- Todas as requisições são processadas no backend
- O aplicativo não armazena dados sensíveis
- localStorage é usado apenas para histórico de treinos local

## 🚨 Troubleshooting

### Erro: "NVIDIA API key not configured"
- Verifique se a variável `NVIDIA_API_KEY` foi adicionada em Vercel
- Redeploy o projeto após adicionar a chave

### Chat não respondendo
- Verifique a chave API em [build.nvidia.com](https://build.nvidia.com)
- Certifique-se de que a chave está ativa
- Verifique os logs em Vercel: Projeto → Deployments → Logs

## 📱 Suporte a Dispositivos

- ✅ Desktop (Chrome, Firefox, Safari, Edge)
- ✅ Tablet (iPad, Android tablets)
- ✅ Mobile (iPhone, Android phones)

## 🤝 Contribuindo

Sinta-se livre para fazer fork, melhorar e abrir pull requests!

## 📄 Licença

MIT - Veja LICENSE para detalhes

## 👨‍💻 Autor

**Kleber** - [GitHub](https://github.com/Klebercdc)

---

**Desenvolvido com ❤️ e NVIDIA AI**
