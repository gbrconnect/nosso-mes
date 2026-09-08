# Nosso Mês, demonstração

Demonstração pública do **Nosso Mês**, o controle financeiro do casal em um arquivo só.

A página abre já com dados de exemplo. Quem visita pode mexer em tudo sem medo:
nada sai do navegador de quem está usando e nada chega até aqui.

## O que dá para ver na demonstração

- Painel do mês, com visão de 1, 3 ou 6 meses e do ano
- Despesas fixas que se repetem sozinhas em todos os meses
- Salários e outras rendas
- Cartões e faturas, com leitura de PDF e de OFX ou lançamento manual
- Parcelamentos que caem sozinhos nos próximos meses
- Orçamento por categoria
- Metas e reserva de emergência
- Resumo do mês para imprimir ou salvar em PDF

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | O app inteiro, em um arquivo só |
| `og.png` | Imagem que aparece quando o link é compartilhado |
| `apple-touch-icon.png`, `icone.png` | Ícones |
| `.nojekyll` | Diz ao GitHub Pages para publicar os arquivos como estão |

## Botão "Quero o meu"

O botão fica escondido até você colocar o endereço da página de venda.
Abra o `index.html`, procure por `const LINK_COMPRA=''` e coloque o link entre as aspas:

```js
const LINK_COMPRA='https://pay.kiwify.com.br/seu-produto';
```

## Publicar

Repositório público, aba **Settings**, item **Pages**, origem **Deploy from a branch**,
branch `main` e pasta `/ (root)`.
