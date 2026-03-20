# Jogo da Forca (Adivinhe)

Aplicativo simples de adivinhação de palavras desenvolvido com React + TypeScript + Vite. É um jogo estilo forca em que o usuário tenta acertar letras de uma palavra oculta, recebendo dica e limite de tentativas.

## 🚀 Visão Geral

- Palavra aleatória selecionada de um conjunto (`WORDS` em `src/utils/words.ts`).
- Usuário digita letra por letra e confirma.
- Letras certas são exibidas na posição correta, letras repetidas são validadas e evitadas.
- Pontuação corresponde ao total de letras corretas encontradas.
- Jogo termina quando todas as letras são descobertas (vitória) ou quando esgotam as tentativas.
- Possibilidade de reiniciar a qualquer momento.

## 🧩 Componentes Principais

- `App.tsx`: lógica central, estados e controle de fluxo (início, fechamento, tentativas, fim de jogo, etc.).
- `Header`: exibe status de tentativas usadas e botão reiniciar.
- `Tip`: exibe dica associada à palavra.
- `Letter`: exibe letra revelada ou placeholder.
- `Input`: campo de entrada para o palpite.
- `Button`: botão de confirmação.
- `LettersUsed`: lista de letras já tentadas com information se foram corretas ou não.

## 🛠️ Tecnologias

- React 18
- TypeScript
- Vite
- CSS Modules

## 📁 Estrutura do Projeto

- `src/App.tsx`
- `src/utils/words.ts`
- `src/components/Header/index.tsx`
- `src/components/Tip/index.tsx`
- `src/components/Letter/index.tsx`
- `src/components/Input/index.tsx`
- `src/components/Button/index.tsx`
- `src/components/LettersUsed/index.tsx`

## 📝 Como executar

1. Clonar o repositório

```bash
git clone https://github.com/gmarquini/adivinhe.git
cd adivinhe
```

2. Instalar dependências

```bash
npm install
```

3. Rodar aplicação em modo de desenvolvimento

```bash
npm run dev
```

4. Abrir no navegador quando o Vite fornecer o endereço (`http://localhost:5173` geralmente).

## ✅ Regras do Jogo

- A cada tentativa, o número de letras usadas aumenta e a letra é marcada como correta/incorreta.
- O jogo permite até `len(palavra) + 5` tentativas.
- Se acertar todas as letras, alerta de vitória e reinicia.
- Se passar do limite, alerta de derrota e reinicia.

## 📌 Sugestões futuras

- adicionar timer e ranking
- animações e som
- persistência de pontuação localStorage
- maior banco de palavras com categorias

---

Feito para portfolio: demonstrando lógica de estado, componentes reutilizáveis e controle de interface com React + TypeScript.
