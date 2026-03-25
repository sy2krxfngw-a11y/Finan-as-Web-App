# Meu Controle Financeiro - Web App

Versão web do aplicativo de controle de gastos, desenvolvida com React, Vite e Tailwind CSS.

## 🚀 Como Executar

### Pré-requisitos
- Node.js (v14+)
- npm ou pnpm

### Instalação

1. **Instale as dependências:**
```bash
npm install
# ou
pnpm install
```

2. **Inicie o servidor de desenvolvimento:**
```bash
npm run dev
# ou
pnpm dev
```

3. **Abra no navegador:**
```
http://localhost:3000
```

## 📁 Estrutura do Projeto

```
finance-app-web/
├── src/
│   ├── components/          # Componentes reutilizáveis
│   │   ├── CircularProgress.jsx
│   │   └── ProgressBar.jsx
│   ├── pages/              # Páginas da aplicação
│   │   ├── Home.jsx
│   │   ├── AddExpense.jsx
│   │   ├── EditCategory.jsx
│   │   └── Settings.jsx
│   ├── hooks/              # Hooks customizados
│   │   └── useFinanceData.js
│   ├── App.jsx             # Componente principal
│   ├── main.jsx            # Entrada da aplicação
│   └── index.css           # Estilos globais
├── index.html              # HTML principal
├── vite.config.js          # Configuração Vite
├── tailwind.config.js      # Configuração Tailwind
└── package.json            # Dependências
```

## 🎯 Funcionalidades

✅ **Painel Principal**
- Gráfico circular mostrando percentual de consumo
- Barra de progresso visual
- Resumo de gastos, limite e restante
- Listagem de categorias com status

✅ **Adicionar Gasto**
- Seleção de categoria
- Entrada de valor
- Descrição opcional
- Seletor de data

✅ **Editar Categorias**
- Mudar nome da categoria
- Escolher cor (10 opções)
- Ajustar limite mensal

✅ **Configurações**
- Definir salário mensal
- Configurar limite total
- Ajustar limite de alerta

## 💾 Armazenamento de Dados

Os dados são salvos automaticamente no **localStorage** do navegador:
- Categorias
- Despesas
- Configurações

**Nota:** Os dados são locais ao navegador. Se você limpar o cache, os dados serão perdidos.

## 🎨 Personalização

### Cores
Edite `tailwind.config.js` para mudar as cores:
```javascript
colors: {
  primary: '#FF8C00',      // Laranja
  success: '#4CAF50',      // Verde
  error: '#F44336',        // Vermelho
  warning: '#FFA500',      // Amarelo
}
```

### Porta
Edite `vite.config.js` para mudar a porta:
```javascript
server: {
  port: 3000,  // Mude para outra porta
}
```

## 📦 Build para Produção

Para criar uma versão otimizada:
```bash
npm run build
# ou
pnpm build
```

Os arquivos compilados estarão em `dist/`.

## 🚀 Deploy

### Vercel
```bash
npm install -g vercel
vercel
```

### Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod --dir dist
```

### GitHub Pages
1. Adicione ao `vite.config.js`:
```javascript
base: '/finance-app-web/',
```
2. Execute: `npm run build`
3. Faça push da pasta `dist/` para o branch `gh-pages`

## 🐛 Troubleshooting

### Porta 3000 já está em uso
Mude a porta em `vite.config.js` ou execute:
```bash
lsof -i :3000
kill -9 <PID>
```

### Dados não aparecem
1. Abra o DevTools (F12)
2. Vá em `Application > Local Storage`
3. Verifique se há dados salvos

### Estilos não carregam
```bash
npm install
npm run dev
```

## 📚 Tecnologias

- **React 18** - Biblioteca UI
- **Vite** - Build tool
- **Tailwind CSS** - Framework CSS
- **Lucide React** - Ícones
- **localStorage** - Armazenamento local

## 📄 Licença

Projeto pessoal - Livre para usar e modificar.

## 🤝 Contribuições

Sinta-se livre para fazer fork e enviar pull requests!

---

**Desenvolvido com ❤️ para controlar seus gastos**
