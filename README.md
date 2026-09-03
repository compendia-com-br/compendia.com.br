# compendia.com.br

Site da marca **Compendia**, publicado por GitHub Pages no domínio `compendia.com.br`.

## Estado

A página de hoje é um **provisório técnico** — nome, aviso de construção e contato. Ela
existe para que o GitHub Pages tenha o que publicar e para que o certificado HTTPS possa
ser emitido. **Não é a página da marca**, e não passou pelo brandbook.

## O que mora onde

| Endereço | Onde é servido |
|---|---|
| `compendia.com.br` | GitHub Pages, deste repositório |
| `corpus.compendia.com.br` | VPS próprio — a API e o MCP dos acervos, fora do GitHub |

Os dois são independentes. Mexer aqui não afeta o corpus, e vice-versa.

## Publicar uma alteração

Commit na branch `main`. O GitHub Pages reconstrói sozinho, em cerca de um minuto.

O arquivo `CNAME` guarda o domínio e **não pode ser apagado** — sem ele o GitHub devolve o
site para o endereço `github.io` e o domínio para de atender.

## Fonte

`~/claude/projetos/compendia-site`

## Cache dos ativos de marca

Os arquivos em `marca/` são servidos com `cache-control: max-age=14400` (4h) e
têm nome fixo. Sem versionar a URL, uma assinatura nova fica invisível por até
quatro horas — aconteceu três vezes em 03/09/2026, e o sintoma engana: o
arquivo está publicado, a borda é que entrega o anterior.

**Ao trocar qualquer arquivo de `marca/`, atualize o `?v=` no `index.html`.**
O valor é a data-hora da publicação (`date +%Y%m%d%H%M`). Nome igual, URL
diferente: a borda trata como recurso novo e não há o que purgar.
