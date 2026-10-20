# Checklist — Oferta Escalada (do garimpo ao Meta Ads)

Site estático em **um único arquivo** (`index.html`): checklist interativo em 22 passos
para modelar uma oferta escalada e subir landing, quiz, checkout, deploy e pixel.

- Dark mode, responsivo (desktop e mobile)
- Progresso salvo no navegador de quem usa (`localStorage`) — cada pessoa tem o seu
- Prints e ilustrações embutidos em base64: funciona offline, sem pasta de assets
- Dicionário clicável de termos e "Traduzindo" em cada passo

## Como colocar no ar (GitHub + Vercel)

1. **GitHub** — crie um repositório (pode ser privado) e suba o conteúdo desta pasta:
   `Add file → Upload files` e arraste `index.html` (e os demais arquivos). O `index.html`
   precisa ficar na **raiz** do repositório.
2. **Vercel** — em [vercel.com](https://vercel.com), entre com **Continue with GitHub**,
   clique em `Add New → Project`, importe o repositório e clique em **Deploy**.
   Não precisa configurar nada (framework: *Other*). Em segundos sai a URL
   `seu-projeto.vercel.app` com SSL.
3. **Domínio próprio (opcional)** — no projeto: `Settings → Domains`, adicione seu
   domínio e crie no registrador os apontamentos que a Vercel indicar
   (registro `A` para a raiz e/ou `CNAME` para o `www`).

## Como editar depois

Edite o `index.html` direto no editor web do GitHub (tecla `.` ou botão do lápis),
salve o commit — a Vercel republica sozinha.

- **Textos dos passos:** procure por `const MODULES` no arquivo.
- **Trocar uma ilustração por print real:** cada passo tem `img: IMG["x-y"]`;
  os valores ficam em `const IMG`.
- **Dicionário de termos:** procure por `const GLOSS`.

## Estrutura

```
oferta-escalada-checklist/
├── index.html   ← o site inteiro (HTML + CSS + JS + imagens embutidas)
├── README.md
└── .gitignore
```
