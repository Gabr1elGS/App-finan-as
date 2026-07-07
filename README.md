# 💰 Controle Financeiro

Aplicativo de controle financeiro pessoal 100% offline. Gerencie seus gastos, salário e dividendos direto do celular, sem precisar de internet ou banco de dados.

---

## 📱 Screenshots

| Tela de Boas-vindas | Dashboard | Gastos |
|:---:|:---:|:---:|
| Crie seu perfil com nome e avatar | Resumo completo do mês | Adicione e gerencie contas |

| Receitas | Comparar Meses | Perfil |
|:---:|:---:|:---:|
| Salário e dividendos | Análise mês a mês | Backup e configurações |

---

## ✨ Funcionalidades

### 👤 Perfil do Usuário
- Cadastro com nome e avatar personalizado (20 opções de emoji)
- Edição de perfil a qualquer momento
- Detecção automática de dados de versões anteriores

### 💸 Gestão de Gastos
- Cadastro de categorias ilimitadas (Alimentação, Moradia, Transporte, etc.)
- Adicionar contas com nome, valor e categoria
- ☑️ Marcar contas como **pagas** (checkbox)
- ✏️ Editar qualquer gasto já lançado
- 🔄 Marcar gastos como **recorrentes** (fixos todo mês)
- 🗑️ Excluir gastos

### 💵 Gestão de Receitas
- Cadastro de **Salário** e **Dividendos** separados
- ☑️ Marcar como **recebido** (checkbox)
- ✏️ Editar receitas
- 🔄 Marcar receitas como **recorrentes**
- Resumo de valores recebidos vs pendentes

### 📅 Controle por Mês
- Seletor de mês com **calendário visual**
- Navegação por setas ◀ ▶ ou toque no mês para abrir o calendário
- Seleção livre de qualquer mês e ano
- Indicador de meses que possuem dados (bolinha verde)
- Botão rápido "Ir para mês atual"

### 🔄 Gastos e Receitas Recorrentes
- Marque itens fixos como recorrentes (aluguel, streaming, salário, etc.)
- Ao mudar de mês, o app oferece um botão para **copiar todos os recorrentes** do mês anterior com um toque
- Evita redigitar os mesmos lançamentos todo mês

### 📊 Dashboard (Resumo)
- Saldo do mês (receitas - gastos) com indicador visual verde/vermelho
- Cards de Salário e Dividendos
- Contas pagas vs pendentes com contadores
- 🏆 **Ranking de categorias** com barras de progresso (🥇🥈🥉)
- Últimas contas do mês

### 📅 Comparativo Mensal
- Visão lado a lado de todos os meses
- Gastos, salário e dividendos de cada mês
- Barra proporcional de gastos
- 🏆 Categoria com maior gasto em cada mês
- Saldo mensal (positivo/negativo)

### 📦 Backup e Restauração
- 📤 **Exportar** todos os dados em arquivo JSON
- 📥 **Importar** dados de um backup anterior
- O backup inclui: perfil, categorias, gastos, receitas e contadores
- Instruções de como atualizar o app sem perder dados

---

## 🛡️ Privacidade

- **100% Offline** — nenhum dado é enviado para a internet
- Todos os dados ficam salvos no **localStorage** do navegador (memória do celular)
- Sem banco de dados, sem servidor, sem rastreamento
- Seus dados são somente seus

---

## 🚀 Como Instalar

### Opção 1: Netlify (Recomendado — Grátis)

1. Baixe o arquivo `app-pronto.zip`
2. Acesse [app.netlify.com/drop](https://app.netlify.com/drop)
3. Crie uma conta grátis
4. Faça upload do arquivo ZIP
5. Pronto! Seu link permanente será gerado

### Opção 2: Qualquer hospedagem estática

O app é um site estático (HTML/CSS/JS). Pode ser hospedado em:
- Netlify
- Vercel
- GitHub Pages
- Cloudflare Pages
- Qualquer servidor web

### 📱 Instalar no Android

1. Abra o link do seu app no **Chrome**
2. Toque nos **3 pontinhos** (⋮)
3. Toque em **"Adicionar à tela inicial"**
4. O app aparece como ícone no celular!

---

## 🔄 Como Atualizar

1. No app atual: vá em **👤 Perfil** → toque **📤 Exportar**
2. Baixe o novo ZIP
3. No Netlify: vá no seu site → aba **Deploys** → arraste o novo ZIP
4. Abra o app atualizado → **👤 Perfil** → **📥 Importar**
5. Selecione o arquivo de backup
6. Pronto! ✅

> **Dica:** Se atualizar no mesmo site do Netlify, os dados podem ser mantidos automaticamente. O backup é uma garantia extra.

---

## 🏗️ Tecnologias

| Tecnologia | Uso |
|---|---|
| **Next.js 16** | Framework React |
| **React 19** | Interface do usuário |
| **TypeScript** | Tipagem segura |
| **Tailwind CSS 4** | Estilização |
| **localStorage** | Armazenamento de dados |
| **PWA** | Funciona como app nativo |

---

## 📂 Estrutura do Projeto

```
src/
├── app/
│   ├── page.tsx          # App principal (todas as telas)
│   ├── layout.tsx        # Layout base
│   └── globals.css       # Estilos globais e animações
├── lib/
│   └── supabase.ts       # Placeholder (não utilizado)
public/
├── manifest.json         # Configuração PWA
├── download.html         # Página de download
└── README.md             # Este arquivo
```

---

## 📋 Histórico de Versões

### v4.0 — Perfil e Backup
- 👤 Cadastro de perfil com nome e avatar
- 📤📥 Exportar e importar dados (backup completo)
- ✅ Detecção automática de dados de versões anteriores
- 🗑️ Opção de apagar todos os dados

### v3.0 — Edição e Recorrentes
- ✏️ Editar gastos e receitas já lançados
- 🔄 Marcar itens como recorrentes
- 📋 Copiar recorrentes do mês anterior com um toque

### v2.0 — Dividendos e Checkbox
- ☑️ Marcar dividendos e salário como recebidos
- 📊 Resumo de recebidos vs pendentes

### v1.0 — Lançamento
- 📅 Separação por mês com calendário visual
- 🏆 Ranking de categorias
- 📅 Comparativo mensal
- 💸 Gastos com categorias
- 💵 Salário e dividendos
- ☑️ Marcar contas como pagas

---

## 📄 Licença

Este projeto é de uso pessoal e livre. Use, modifique e distribua como quiser.

---

<p align="center">
  Feito com ❤️ para quem quer controlar suas finanças
</p>
