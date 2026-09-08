# Nosso Mês

Controle financeiro do casal. O app inteiro roda em um arquivo HTML,
com as contas e a sincronização apoiadas no Supabase.

## O que tem aqui

| Endereço | O que é |
| --- | --- |
| `/` | O app. Pede e-mail e senha, e guarda os dados na conta de cada cliente |
| `/demo/` | Demonstração pública, sem login, com dados de exemplo |

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | O app com login |
| `demo/index.html` | A demonstração |
| `og.png` | Imagem que aparece quando o link é compartilhado |
| `apple-touch-icon.png`, `icone.png` | Ícones |
| `.nojekyll` | Diz ao GitHub Pages para publicar os arquivos como estão |

## Como liberar um cliente

1. Entre no app com a conta master
2. Aba **Acessos**, informe nome e e-mail da compra e clique em **Gerar acesso**
3. O recado já sai copiado, com link, e-mail, código e instruções. Cole para o cliente
4. O cliente clica em "Tenho um código de convite", informa e-mail e código e escolhe a senha dele

Para cortar um acesso, é o botão **Bloquear** na lista. A pessoa perde a entrada na hora
e os dados dela continuam guardados.

## Botão "Quero o meu" da demonstração

Fica escondido até você preencher o link da página de venda.
Em `demo/index.html`, procure `const LINK_COMPRA=''` e coloque o endereço entre as aspas.

## Onde ficam as configurações do servidor

No topo do `<script>` do `index.html`:

```js
const SB_URL='https://....supabase.co';
const SB_KEY='sb_publishable_...';
```

A chave publishable é feita para ficar visível no navegador. Quem protege os dados são as
políticas de Row Level Security do banco, que só deixam cada pessoa ver a própria linha.
A chave secret nunca deve aparecer aqui.
