# Roteiro Ponta Negra — como publicar no GitHub Pages

Este repositório tem um único arquivo (`index.html`) com o roteiro interativo.
Não precisa de build, servidor ou instalação — é só publicar.

## Passo a passo

1. Crie um repositório novo no GitHub (pode ser público ou privado — privado
   também funciona no GitHub Pages se sua conta tiver esse recurso).
2. Suba o arquivo `index.html` para a raiz do repositório (branch `main`).
3. No repositório, vá em **Settings → Pages**.
4. Em **Source**, escolha **Deploy from a branch**.
5. Em **Branch**, selecione `main` e a pasta `/ (root)`. Clique em **Save**.
6. Espere um ou dois minutos. O GitHub mostra o link no topo da mesma página
   (algo como `https://SEU-USUARIO.github.io/NOME-DO-REPO/`).
7. Mandem esse link pra vocês dois. Pronto, está no ar.

## Como funciona a sincronização entre os dois

Este site é **estático** (sem servidor próprio), então cada navegador guarda
os dados localmente (`localStorage`). Isso quer dizer:

- Tudo que vocês adicionarem/editarem fica salvo **naquele navegador/aparelho**,
  mesmo fechando e abrindo de novo.
- Só que as edições **não aparecem automaticamente no aparelho da outra
  pessoa** — não existe um servidor compartilhado por trás.

Pra sincronizar, use os botões da barra de ferramentas:

- **⬇ exportar** — baixa um arquivo `.json` com o roteiro atual.
- **⬆ importar** — carrega um arquivo `.json` que a outra pessoa te mandou,
  substituindo (ou não, ele avisa antes) o que está na tela.

Fluxo sugerido: sempre que um editar bastante, clica em exportar e manda o
arquivo pro outro (WhatsApp, e-mail, o que for). A outra pessoa abre o site e
clica em importar.

### Quer sincronização automática de verdade (sem exportar/importar)?

Dá pra evoluir isso depois trocando o `localStorage` por um bancozinho
gratuito (ex: Firebase Realtime Database, Supabase) — link único, os dois
editam e tudo aparece na hora pro outro, sem precisar exportar nada. Se
quiserem seguir por esse caminho, é só pedir que a gente adapta o arquivo.

## Estrutura

```
/
├── index.html   ← o site inteiro (HTML + CSS + JS + fotos embutidas)
└── README.md    ← este arquivo
```

Nenhum outro arquivo é necessário — as fotos dos cardápios já estão
embutidas dentro do próprio `index.html`.
