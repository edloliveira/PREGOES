# Gerador de Propostas

Gera propostas comerciais para licitações em **Word (.docx)** e **PDF**, 100% no navegador (PWA, funciona offline).
Marca e modelo saem em colunas separadas.

## Arquivos
| Arquivo | Para quê |
|---|---|
| `index.html` | O app inteiro (HTML + CSS + JS + biblioteca do Word) |
| `sw.js` | Service worker (offline) – precisa ser um arquivo separado |
| `manifest.webmanifest` + `icons/` | Instalação como app – precisam ser arquivos separados |

## Publicar no GitHub Pages
1. Crie um repositório e envie o **conteúdo** desta pasta (não a pasta em si).
2. Em **Settings → Pages**, escolha *Deploy from a branch*, branch `main`, pasta `/ (root)`.
3. Acesse `https://SEU-USUARIO.github.io/NOME-DO-REPO/` e, no Chrome/Edge/Safari, instale o app.

## Rodar localmente
```
python -m http.server 8080
```
Abra `http://localhost:8080`. (Abrir o `index.html` direto também funciona, só sem o modo offline/instalável.)

## Dados
Ficam no `localStorage` do navegador (nada é enviado a servidor). Use **Exportar → Backup** para guardar uma cópia.
CSV de itens: `item;descricao;unidade;quantidade;valor_referencia;valor_unitario;marca;modelo`.
