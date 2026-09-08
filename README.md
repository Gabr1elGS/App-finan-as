# 💰 Controle Financeiro v9.0

Aplicativo de controle financeiro pessoal **100% offline**. Gerencie gastos, receitas, dividendos e veículos direto do celular, sem internet e sem banco de dados.

---

## ✨ Novidades da v9.0 — Vencimento de Dividendos

### 🔔 Data de vencimento
* Ao cadastrar um **Dividendo**, informe a **data de vencimento** (opcional)
* Em dividendos parcelados, o vencimento **avança automaticamente** a cada mês
  * Ex: `15/01`, `15/02`, `15/03`...
  * Datas inválidas são ajustadas (31/01 → 28/02)

### 📢 Sistema de notificações
* **Alerta no app** — painel destacado no Resumo e na aba Receitas
* **Notificação no celular** — aviso do sistema operacional quando vencer (1x por dia)
* **Badge numérico** no ícone da aba Receitas com a quantidade de pendências
* Botão **✓** para marcar como recebido direto do alerta

### 🎨 Sinalização por cores

| Situação | Cor | Indicação |
| -------- | --- | --------- |
| Atrasado | 🔴 Vermelho | `Atrasado X dias` |
| Vence hoje | 🟠 Âmbar (pulsante) | `Vence hoje` |
| Próximos 3 dias | 🔵 Azul | `Vence em X dias` |
| Futuro | ⚪ Cinza | Apenas a data |
| Recebido | ⚪ Cinza | Alerta removido |

---

## 📋 Histórico de Versões

| Versão | Novidades |
| ------ | --------- |
| **v9.0** | 🔔 Vencimento de dividendos + notificações |
| **v8.0** | ⛽ Abastecimento com forma de pagamento integrada aos Gastos |
| **v7.0** | 🚗 Aba Veículos: abastecimentos, km/mês e manutenção |
| **v6.0** | 🐛 Correção de fuso horário e recorrência • parcelas • foto de perfil |
| **v5.0** | 📊 Gráficos no comparativo • dividendos multi-mês • ícone Mora |
| **v4.0** | 👤 Perfil e backup |
| **v3.0** | ✏️ Edição e recorrentes |
| **v2.0** | ☑️ Dividendos e checkbox |
| **v1.0** | 🚀 Lançamento |

---

## ✨ Funcionalidades

### 👤 Perfil
* Nome + avatar emoji (24 opções) **ou foto da galeria**
* Foto comprimida para 256px, salva apenas no dispositivo

### 💸 Gastos
* Categorias ilimitadas com **sugestões rápidas**
* ☑️ Marcar como pago • ✏️ Editar • 🗑️ Excluir
* 🔄 Recorrentes (copia do mês anterior com um toque)
* 💳 **Parcelamento** com contador `1/12`, `2/12`...

### 💵 Receitas
* **Salário** e **Dividendos** separados
* 📅 Dividendos com múltiplas parcelas e contador de andamento
* ½ Marcar pagamento **parcial** (destaque amarelo)
* 🔔 **Data de vencimento com notificação** *(novo na v9.0)*

### 🚗 Veículos
* Cadastro de **Carro** 🚗 e **Moto** 🏍️
* **Abastecimentos**: valor, odômetro, litros, gasolina/álcool, data
* **Cálculo automático**: km percorridos, litros, média km/L e preço/litro
* **Manutenções**: serviço, valor e data
* 💵 **Dinheiro** → lançado também em Gastos
* 💳 **Cartão** → registrado somente em Veículos

### 📊 Dashboard
* Saldo do mês com indicador visual
* Cards de Salário e Dividendos
* 🏆 Ranking de categorias
* Barra de progresso de contas pagas

### 📈 Comparativo
* Gráfico de barras por mês (Gastos, Salário, Dividendos)
* Categoria com maior gasto e saldo mensal

### 📦 Backup
* 📤 Exportar / 📥 Importar em JSON
* Importação compatível com formatos de versões anteriores

---

## 🔔 Como ativar as notificações

1. Abra o app e cadastre um dividendo com data de vencimento
2. Toque em **"Ativar"** no aviso que aparece
3. Confirme a permissão no navegador

> **Dica:** para receber avisos com o app fechado, instale-o na tela inicial (PWA). As notificações são disparadas quando o app é aberto e o vencimento está próximo.

---

## 🛡️ Privacidade

* **100% Offline** — nenhum dado sai do dispositivo
* Armazenamento em **localStorage**
* Sem servidor, sem rastreamento, sem conta

---

## 🚀 Deploy no Netlify

### Via GitHub (recomendado)
1. Faça fork/upload deste repositório
2. Em [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import an existing project**
3. Selecione o repositório e clique em **Deploy**

### Deploy manual
1. Baixe o ZIP da release
2. Arraste em [app.netlify.com/drop](https://app.netlify.com/drop)

### 📱 Instalar no celular
**Android (Chrome):** ⋮ → *Instalar aplicativo*
**iPhone (Safari):** Compartilhar → *Adicionar à Tela de Início*

---

## 🔄 Como atualizar sem perder dados

1. **👤 Perfil** → **📤 Exportar** (guarde o JSON)
2. Publique a nova versão
3. **👤 Perfil** → **📥 Importar** → selecione o backup

> Atualizando no mesmo domínio, os dados são mantidos automaticamente. O backup é garantia extra.

---

## 🏗️ Tecnologias

| Tecnologia | Uso |
| ---------- | --- |
| **Next.js 16** | Framework React (static export) |
| **React 19** | Interface |
| **TypeScript** | Tipagem segura |
| **Tailwind CSS 4** | Estilização |
| **Recharts** | Gráficos |
| **Notification API** | Alertas de vencimento |
| **localStorage** | Persistência offline |
| **PWA** | Instalável como app nativo |

---

## 📂 Estrutura

```
src/
├── app/
│   ├── page.tsx
│   ├── layout.tsx
│   └── globals.css
├── components/
│   ├── FinanceApp.tsx      # Navegação e estado global
│   ├── Dashboard.tsx
│   ├── ExpensesTab.tsx
│   ├── RevenueTab.tsx
│   ├── VehiclesTab.tsx
│   ├── CompareTab.tsx
│   ├── ProfileTab.tsx
│   ├── DueAlerts.tsx       # Alertas de vencimento (v9.0)
│   ├── MonthChart.tsx
│   ├── MonthSelector.tsx
│   ├── Avatar.tsx
│   ├── AvatarPicker.tsx
│   └── WelcomeScreen.tsx
└── lib/
    ├── types.ts
    ├── storage.ts          # Persistência e migrações
    ├── utils.ts            # Datas, moeda, cálculos
    └── notifications.ts    # Notification API (v9.0)
```

---

## 💻 Desenvolvimento

```bash
npm install
npm run dev      # http://localhost:3000
npm run build    # gera a pasta out/
```

---

## 📄 Licença

Uso pessoal e livre. Use, modifique e distribua como quiser.

---

Feito com ❤️ para quem quer controlar suas finanças
