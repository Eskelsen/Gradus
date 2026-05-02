# 🧠 AI Constitution — Calorias → Passos (Frontend Only)

---

## 🎯 Objetivo

Construir uma aplicação web extremamente simples, mobile-first, que calcula:

- calorias totais de um produto consumido
- quantidade de passos necessários para queimar essas calorias
- tempo estimado de caminhada

A aplicação deve ser totalmente funcional offline e sem backend.

---

## 📦 Escopo

- Aplicação 100% frontend
- Um único arquivo `index.html` contendo:
  - HTML
  - CSS
  - JavaScript (inline ou embutido)
- Opcional: `sw.js` para funcionamento offline (PWA básica)

---

## 🧮 Regras de cálculo (OBRIGATÓRIO)

A IA deve sempre usar exatamente estas fórmulas:

### Calorias totais
calorias_total = (calorias_por_100 / 100) * peso_total

### Passos necessários
passos = calorias_total * 20

### Tempo estimado
tempo_minutos_total = passos / 100

---

## ⏱️ Formatação do tempo (OBRIGATÓRIO)

O tempo deve ser exibido como:

X min Y s

Onde:
- minutos = inteiro
- segundos = resto da conversão

Exemplo:
1250 passos → 12 min 30 s

---

## 🔢 Arredondamento

- calorias_total → inteiro (Math.round)
- passos → inteiro (Math.round)
- tempo:
  - minutos → inteiro (Math.floor)
  - segundos → inteiro (Math.floor)

---

## 🧾 Interface (UI)

A tela deve conter apenas:

### Inputs editáveis:
1. Calorias por 100g ou 100ml
2. Peso total do produto (g ou ml)

### Outputs (não editáveis):
1. Calorias totais
2. Passos necessários
3. Tempo estimado

---

## ⚡ Comportamento

- O cálculo deve ser **automático**
- Atualizar imediatamente ao digitar (evento input)
- Não deve existir botão de "Calcular"

---

## 🧠 Validação

- Campos vazios → não calcular
- Valores inválidos → limpar outputs
- Não permitir números negativos

---

## 📱 Mobile-first (OBRIGATÓRIO)

- Layout otimizado para celular
- Inputs grandes e fáceis de usar
- Tipografia legível
- Espaçamento confortável
- Evitar rolagem desnecessária

---

## 🎨 Estilo visual

A IA pode escolher entre:

- CSS puro simples (preferencial)
OU
- Inclusão de Bootstrap via CDN (permitido, mas opcional)

Regras:
- Não usar frameworks JS
- Visual limpo e funcional
- Sem excesso de elementos

---

## 🔌 Offline (PWA leve)

Se implementar `sw.js`, deve:

- Cachear:
  - index.html
  - assets necessários
- Permitir funcionamento offline completo

Não implementar features avançadas de PWA.

---

## 🧱 Arquitetura

- Código deve ser simples e direto
- Evitar modularização desnecessária
- Tudo pode ficar no mesmo arquivo

---

## 🛑 Restrições

- ❌ Não usar backend
- ❌ Não usar APIs externas
- ❌ Não usar frameworks JS (React, Vue, Angular)
- ❌ Não usar bibliotecas desnecessárias
- ❌ Não complicar a estrutura

---

## ✅ Boas práticas obrigatórias

- Código legível e direto
- Variáveis com nomes claros
- Separar minimamente:
  - captura de input
  - cálculo
  - renderização

---

## 🧪 Estratégia de implementação

A IA deve:

1. Criar primeiro a versão funcional mínima
2. Garantir que funciona corretamente
3. Só depois melhorar visual ou UX

---

## 🔍 Auto-validação (OBRIGATÓRIO)

Antes de responder, a IA deve verificar:

- O app funciona sem backend?
- O cálculo está EXATAMENTE conforme definido?
- O comportamento é automático?
- Está simples o suficiente?
- Funciona bem em mobile?

Se qualquer resposta for "não", corrigir antes de finalizar.

---

## 🧠 Regra de ouro

Se existir dúvida entre:

- adicionar algo
- manter simples

👉 escolher sempre manter simples