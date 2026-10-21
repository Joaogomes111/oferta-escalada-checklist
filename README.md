# Checklist — Oferta Escalada (do garimpo ao Meta Ads)

Site estático em **um único arquivo** (`index.html`): checklist interativo em **23 passos**
no fluxo real da operação — minerar a oferta com 20+ anúncios ativos, comprar pra ver por
dentro, criar o produto na plataforma, gerar a LP com IA, publicar na Vercel, instalar
pixel + token (CAPI), produzir os criativos no estilo validado e subir a campanha.
Funciona pra Brasil ou qualquer país.

- Dark mode, responsivo (desktop e mobile)
- Progresso salvo no navegador de quem usa (`localStorage`) — cada pessoa tem o seu
- Prints e ilustrações embutidos em base64: funciona offline, sem pasta de assets
- "Traduzindo" em cada passo + dicionário clicável de termos
- 4 blocos de código copiáveis: pixel, InitiateCheckout e os prompts de LP e criativos

## Como colocar no ar (GitHub + Vercel)

1. **GitHub** — crie um repositório (pode ser privado) e suba o conteúdo desta pasta:
   `Add file → Upload files`. O `index.html` precisa ficar na **raiz** do repositório.
2. **Vercel** — em [vercel.com](https://vercel.com), entre com **Continue with GitHub**,
   `Add New → Project`, importe o repositório e clique em **Deploy** (framework: *Other*).
   Em segundos sai a URL `seu-projeto.vercel.app` com SSL.
3. **Domínio próprio (opcional)** — `Settings → Domains`, adicione seu domínio e crie no
   registrador os apontamentos indicados (`A` na raiz e/ou `CNAME` no `www`).

## Como editar depois

Edite o `index.html` direto no editor web do GitHub, salve o commit — a Vercel republica sozinha.

- **Textos dos passos:** procure por `const MODULES`.
- **Trocar ilustração por print real:** cada passo tem `img: IMG["..."]`; os valores ficam em `const IMG`.
- **Dicionário de termos:** procure por `const GLOSS`.

## Estrutura

```
oferta-escalada-checklist/
├── index.html   ← o site inteiro (HTML + CSS + JS + imagens embutidas)
├── README.md
└── .gitignore
```
