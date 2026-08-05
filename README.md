# 💰 Controle Financeiro v5.0

Aplicativo de controle financeiro pessoal 100% offline. Gerencie seus gastos, salário e dividendos direto do celular, sem precisar de internet ou banco de dados.

---

## 📱 Screenshots

| Tela de Boas-vindas               | Dashboard              | Gastos                     |
| --------------------------------- | ---------------------- | -------------------------- |
| Crie seu perfil com nome e avatar | Resumo completo do mês | Adicione e gerencie contas |

| Receitas             | Comparar Meses    | Perfil                 |
| -------------------- | ----------------- | ---------------------- |
| Salário e dividendos | Análise mês a mês | Backup e configurações |

---

## ✨ Novidades da v5.0

### 📈 Dividendos com Múltiplos Meses
- Ao adicionar um dividendo, escolha **quantos meses** ele vai pagar
- O sistema cria automaticamente entradas para cada mês
- Edite ou apague individualmente ou todos de uma vez

### ½ Pagamento Parcial (Dividendos)
- Dividendos podem ser marcados como **pagamento parcial**
- Pagamentos parciais ficam destacados em **amarelo**
- Toggle para alternar entre pagamento total/parcial

### 🔤 Ordenação Alfabética
- Gastos e Receitas organizados em **ordem alfabética**
- Categorias também em ordem alfabética

### 📊 Gráficos na Aba Comparar
- Cada mês possui um **gráfico de barras** mostrando:
  - 🔴 Gastos
  - 🟢 Salário
  - 🟡 Dividendos

### 🎮 Novo Ícone do App
- Ícone inspirado na moeda **Mora** do Genshin Impact

---

## ✨ Funcionalidades

### 👤 Perfil do Usuário
* Cadastro com nome e avatar personalizado (20 opções de emoji)
* Edição de perfil a qualquer momento

### 💸 Gestão de Gastos
* Cadastro de categorias ilimitadas
* Adicionar contas com nome, valor e categoria
* ☑️ Marcar contas como **pagas**
* ✏️ Editar qualquer gasto
* 🔄 Marcar gastos como **recorrentes**
* 🗑️ Excluir gastos

### 💵 Gestão de Receitas
* Cadastro de **Salário** e **Dividendos** separados
* ☑️ Marcar como **recebido**
* ✏️ Editar receitas
* 🔄 Marcar receitas como **recorrentes**
* 📅 Dividendos com múltiplos meses
* ½ Marcar dividendo como pagamento parcial

### 📅 Controle por Mês
* Seletor de mês com **calendário visual**
* Navegação por setas ◀ ▶
* Indicador de meses com dados (bolinha verde)
* Botão rápido "Ir para mês atual"

### 🔄 Gastos e Receitas Recorrentes
* Marque itens fixos como recorrentes
* Copie todos os recorrentes do mês anterior com um toque

### 📊 Dashboard (Resumo)
* Saldo do mês com indicador visual
* Cards de Salário e Dividendos
* Contas pagas vs pendentes
* 🏆 Ranking de categorias
* Últimas contas do mês

### 📅 Comparativo Mensal
* Visão de todos os meses com gráficos
* Gastos, salário e dividendos de cada mês
* 🏆 Categoria com maior gasto
* Saldo mensal

### 📦 Backup e Restauração
* 📤 Exportar dados em JSON
* 📥 Importar dados de backup

---

## 🛡️ Privacidade

* **100% Offline** — nenhum dado é enviado para a internet
* Dados salvos no **localStorage** do navegador
* Sem banco de dados, sem servidor, sem rastreamento
* Seus dados são somente seus

---

## 🚀 Como Instalar no Netlify

### Opção 1: Deploy via GitHub (Recomendado)

1. Faça fork deste repositório ou faça upload dos arquivos para seu GitHub
2. Acesse [app.netlify.com](https://app.netlify.com)
3. Clique em "Add new site" → "Import an existing project"
4. Conecte seu GitHub e selecione o repositório
5. As configurações de build serão detectadas automaticamente
6. Clique em "Deploy site"
7. Pronto! Seu site estará no ar em minutos

### Opção 2: Deploy manual (ZIP)

1. Execute `npm run build` para gerar a pasta `out/`
2. Acesse [app.netlify.com/drop](https://app.netlify.com/drop)
3. Arraste a pasta `out/` para fazer o deploy
4. Pronto!

### 📱 Instalar no Android

1. Abra o link do seu app no **Chrome**
2. Toque nos **3 pontinhos** (⋮)
3. Toque em **"Adicionar à tela inicial"**
4. O app aparece como ícone no celular!

---

## 🔄 Como Atualizar

1. No app atual: vá em **👤 Perfil** → toque **📤 Exportar**
2. Faça o deploy da nova versão
3. Abra o app atualizado → **👤 Perfil** → **📥 Importar**
4. Selecione o arquivo de backup
5. Pronto! ✅

---

## 🏗️ Tecnologias

| Tecnologia         | Uso                      |
| ------------------ | ------------------------ |
| **Next.js 16**     | Framework React          |
| **React 19**       | Interface do usuário     |
| **TypeScript**     | Tipagem segura           |
| **Tailwind CSS 4** | Estilização              |
| **Recharts**       | Gráficos                 |
| **localStorage**   | Armazenamento de dados   |
| **PWA**            | Funciona como app nativo |

---

## 📂 Estrutura do Projeto

```
src/
├── app/
│   ├── page.tsx          # Página principal
│   ├── layout.tsx        # Layout base
│   └── globals.css       # Estilos globais
├── components/
│   ├── FinanceApp.tsx    # App principal
│   ├── Dashboard.tsx     # Tela de resumo
│   ├── ExpensesTab.tsx   # Aba de gastos
│   ├── RevenueTab.tsx    # Aba de receitas
│   ├── CompareTab.tsx    # Aba de comparação
│   ├── ProfileTab.tsx    # Aba de perfil
│   ├── MonthChart.tsx    # Gráficos
│   ├── MonthSelector.tsx # Seletor de mês
│   └── WelcomeScreen.tsx # Tela de boas-vindas
├── lib/
│   ├── types.ts          # Tipos TypeScript
│   ├── storage.ts        # Funções de localStorage
│   └── utils.ts          # Utilitários
public/
├── manifest.json         # Configuração PWA
├── icon-192.png          # Ícone 192x192
└── icon-512.png          # Ícone 512x512
```

---

## 📋 Desenvolvimento Local

```bash
# Instalar dependências
npm install

# Rodar em desenvolvimento
npm run dev

# Build para produção
npm run build

# A pasta 'out/' será gerada com os arquivos estáticos
```

---

## 📄 Licença

Este projeto é de uso pessoal e livre. Use, modifique e distribua como quiser.

---

Feito com ❤️ para quem quer controlar suas finanças
