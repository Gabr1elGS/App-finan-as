# 💰 Controle Financeiro v8.0

Aplicativo de controle financeiro pessoal 100% offline. Gerencie seus gastos, salário, dividendos e agora também seus **veículos** — direto do celular, sem precisar de internet ou banco de dados.

---

## 📱 Screenshots

| Tela de Boas-vindas                    | Dashboard              | Gastos                          |
| -------------------------------------- | ---------------------- | ------------------------------- |
| Crie seu perfil com nome, foto ou avatar | Resumo completo do mês | Adicione e gerencie contas      |

| Receitas             | Veículos 🆕                          | Perfil                 |
| -------------------- | ----------------------------------- | ---------------------- |
| Salário e dividendos | Abastecimentos, manutenções e km/L  | Backup e configurações |

---

## ✨ Novidades da v8.0

### 🚗 Nova Aba Veículos

Uma aba inteira dedicada aos seus veículos, com navegação própria na barra inferior:

- Cadastre **quantos veículos** quiser (carro, moto, etc.)
- Card individual por veículo com hodômetro atualizado (🛣️ km)
- Exclusão com confirmação — remove junto todos os abastecimentos e manutenções do veículo

### ⛽ Controle de Abastecimento

- Registre cada abastecimento com **valor (R$), litros, km do hodômetro e data**
- Escolha o combustível: **⛽ Gasolina** ou **🌿 Álcool**
- **Média de consumo automática (km/L)** calculada a partir do hodômetro
- Estatísticas do mês: **Km percorridos**, **Litros** consumidos e média geral
- Edite ou apague qualquer abastecimento

### 🔧 Manutenções do Veículo

- Registre manutenções com descrição, valor e data (ex: troca de óleo, pneus)
- Histórico completo por veículo
- Edite ou apague individualmente

### 🔗 Integração opcional com a aba Gastos

- Ao salvar um abastecimento ou manutenção, escolha se o valor **também entra na aba Gastos**
- As categorias **Abastecimento** e **Veículo** são criadas automaticamente
- Prefere controlar separado? Sem problema: o registro pode ficar **apenas na aba Veículos**

### 💳 Forma de Pagamento nos Gastos

- Todo gasto agora pode ser marcado como **💵 Dinheiro** ou **💳 Cartão**
- Badge roxa de identificação em cada item da lista
- Nova categoria padrão: **Cartões**

### 🖼️ Foto de Perfil

- Além dos 20 avatares de emoji, agora você pode usar uma **foto da galeria**
- Validação de imagem com mensagens de erro amigáveis
- Remova a foto e volte para o emoji quando quiser

### 📱 Instalação facilitada

- Novo card **"Instalar no celular"** na aba Perfil, com o passo a passo
- Selos informativos: 🌐 100% Offline • 📱 PWA • 💾 Backup

### 🗂️ Estrutura de dados v8

- Nova estrutura de armazenamento (`version: 8`) com `vehicles`, `fuelEntries` e `maintenances`
- **Backups de versões antigas são migrados automaticamente** ao importar — nada se perde

---

## ✨ Funcionalidades

### 👤 Perfil do Usuário

- Cadastro com nome e avatar personalizado
- **20 opções de emoji** ou **foto da galeria** 🆕
- Edição de perfil a qualquer momento

### 💸 Gestão de Gastos

- Cadastro de categorias ilimitadas
- Categorias padrão: Alimentação, Moradia, Transporte, Saúde, Lazer, Educação, **Cartões** 🆕, Outros
- Adicionar contas com nome, valor e categoria
- **💳 Forma de pagamento: Dinheiro ou Cartão** 🆕
- ☑️ Marcar contas como **pagas**
- ✏️ Editar qualquer gasto
- 🔄 Marcar gastos como **recorrentes**
- 🗑️ Excluir gastos

### 💵 Gestão de Receitas

- Cadastro de **Salário** e **Dividendos** separados
- ☑️ Marcar como **recebido**
- ✏️ Editar receitas
- 🔄 Marcar receitas como **recorrentes**
- 📅 Dividendos com múltiplos meses
- ½ Marcar dividendo como pagamento parcial

### 🚗 Veículos 🆕

- 🚘 Cadastro de múltiplos veículos
- ⛽ Abastecimentos com litros, hodômetro e tipo de combustível
- 📏 Cálculo automático de **km percorridos** e **média km/L**
- 🔧 Histórico de manutenções com valores
- 🔗 Lançamento opcional na aba Gastos com um toque

### 📅 Controle por Mês

- Seletor de mês com **calendário visual**
- Navegação por setas ◀ ▶
- Indicador de meses com dados (bolinha verde)
- Botão rápido "📍 Ir para mês atual"

### 🔄 Gastos e Receitas Recorrentes

- Marque itens fixos como recorrentes
- Copie todos os recorrentes do mês anterior com um toque
- Avisos inteligentes quando não há nada para copiar

### 📊 Dashboard (Resumo)

- Saldo do mês com indicador visual
- Cards de Salário e Dividendos
- ✅ Contas pagas vs ⏳ pendentes (com totais em R$)
- 🏆 Ranking de categorias
- 📋 Últimas contas do mês

### 📈 Comparativo Mensal

- Visão de todos os meses com gráficos
- Gastos, salário e dividendos de cada mês
- 🏆 Categoria com maior gasto
- Saldo mensal

### 📦 Backup e Restauração

- 📤 Exportar dados em JSON
- 📥 Importar dados de backup
- 🔄 **Migração automática** de backups antigos para a estrutura v8 🆕

---

## 🛡️ Privacidade

- **100% Offline** — nenhum dado é enviado para a internet
- Dados salvos no **localStorage** do navegador
- Sem banco de dados, sem servidor, sem rastreamento
- Seus dados são somente seus

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
3. Toque em **"Instalar aplicativo"** ou **"Adicionar à tela inicial"**
4. O app aparece como ícone no celular!

---

## 🔄 Como Atualizar

1. No app atual: vá em **👤 Perfil** → toque **📤 Exportar**
2. Faça o deploy da nova versão
3. Abra o app atualizado → **👤 Perfil** → **📥 Importar**
4. Selecione o arquivo de backup
5. Pronto! ✅ — backups antigos são **migrados automaticamente** para a v8.0

---

## 🗂️ Histórico de Versões

| Versão | Destaques |
| ------ | --------- |
| **v8.0** | 🚗 Aba Veículos (abastecimento, manutenção, km/L) • 💳 Forma de pagamento (Dinheiro/Cartão) • 🖼️ Foto de perfil • 📱 Card de instalação • Migração automática de backups |
| v6.0–7.x | Melhorias de interface, desempenho e estabilidade |
| v5.0 | 📈 Dividendos com múltiplos meses • ½ Pagamento parcial • 🔤 Ordenação alfabética • 📊 Gráficos na aba Comparar • 🎮 Novo ícone |
| v4.5 | Versão inicial pública |

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
│   ├── page.tsx           # Página principal
│   ├── layout.tsx         # Layout base
│   └── globals.css        # Estilos globais
├── components/
│   ├── FinanceApp.tsx     # App principal e navegação
│   ├── Dashboard.tsx      # Tela de resumo
│   ├── ExpensesTab.tsx    # Aba de gastos
│   ├── RevenueTab.tsx     # Aba de receitas
│   ├── VehiclesTab.tsx    # Aba de veículos (abastecimento + manutenção) 🆕
│   ├── CompareTab.tsx     # Aba de comparação
│   ├── ProfileTab.tsx     # Aba de perfil
│   ├── MonthChart.tsx     # Gráficos
│   ├── MonthSelector.tsx  # Seletor de mês
│   ├── AvatarPicker.tsx   # Foto/emoji do perfil 🆕
│   └── WelcomeScreen.tsx  # Tela de boas-vindas
├── lib/
│   ├── types.ts           # Tipos (Vehicle, FuelEntry, Maintenance...) 🆕
│   ├── storage.ts         # localStorage + migração v8 🆕
│   └── utils.ts           # Utilitários
public/
├── manifest.json          # Configuração PWA
├── icon-192.png           # Ícone 192x192
└── icon-512.png           # Ícone 512x512
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

Feito com ❤️ para quem quer controlar suas finanças — e agora também seus veículos 🚗
