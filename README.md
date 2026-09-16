# Cardápio Digital: pedido pronto no WhatsApp

> **Código-fonte privado.** Este repositório é uma vitrine do projeto: telas, decisões
> e resultados. O código pode ser apresentado sob solicitação.

Produto que eu vendo para restaurantes e pizzarias de delivery. O cliente abre um link
no celular, monta o pedido sozinho e ele chega **pronto no WhatsApp da casa**: itens,
observações, endereço, forma de pagamento, troco e total calculado. Sem aplicativo para
baixar, sem cadastro e sem comissão por pedido.

"Pizzaria Bella Massa", com cardápio e dados de demonstração.

![React](https://img.shields.io/badge/React_18-20232A?logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite_5-646CFF?logo=vite&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?logo=framer&logoColor=white)
![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-F38020?logo=cloudflare&logoColor=white)

---

## O fluxo do pedido

<table>
  <tr>
    <td align="center"><img src="imagens/01-cardapio-inicio.png" width="230"><br><sub>1. Cardápio por categorias, com número e preço de cada item</sub></td>
    <td align="center"><img src="imagens/02-cardapio-busca.png" width="230"><br><sub>2. Busca por nome ou ingrediente, sem se importar com acentos</sub></td>
    <td align="center"><img src="imagens/03-cardapio-produto.png" width="230"><br><sub>3. Ingredientes, quantidade e observação por item</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="imagens/04-cardapio-barra-pedido.png" width="230"><br><sub>4. Barra fixa com o total do pedido</sub></td>
    <td align="center"><img src="imagens/05-cardapio-carrinho.png" width="230"><br><sub>5. Revisão do pedido, com a observação abaixo do item</sub></td>
    <td align="center"><img src="imagens/06-cardapio-checkout.png" width="230"><br><sub>6. Entrega ou retirada, pagamento e troco</sub></td>
  </tr>
</table>

<p align="center">
  <img src="imagens/07-pedido-no-whatsapp.png" width="300"><br>
  <sub>7. A mensagem que chega no WhatsApp da loja (simulação com o texto real gerado pelo cardápio)</sub>
</p>

### No computador
<p align="center">
  <img src="imagens/08-cardapio-desktop.png" width="900"><br>
  <sub>O mesmo cardápio em tela larga, com os itens em grade</sub>
</p>

---

## Extensão: convite de casamento digital

A mesma ideia aplicada a eventos. O convidado abre o convite pelo link, confirma
presença pelo WhatsApp com a mensagem pronta e escolhe uma cota da lista de presentes
via Pix. Tem contagem regressiva, programação do dia e animação de abertura.

<table>
  <tr>
    <td align="center"><img src="imagens/09-convite-capa.png" width="260"><br><sub>Capa com contagem regressiva</sub></td>
    <td align="center"><img src="imagens/10-convite-presente-pix.png" width="260"><br><sub>Lista de presentes com Pix copia e cola</sub></td>
  </tr>
</table>

---

## Decisões de projeto

- **Sem backend.** O pedido vira um link `wa.me` com a mensagem formatada. Não há
  servidor, banco de dados nem pagamento online para manter, e o custo de operação é zero.
- **Um cliente novo em minutos.** Tudo que muda de uma loja para outra fica em um
  arquivo de configuração e em um cardápio em JSON. Os dados reais de cada cliente
  ficam fora do repositório.
- **Pensado para a hora do pico.** Mobile-first, leve o bastante para abrir em 3G e em
  celular antigo. A navegação por categorias acompanha a rolagem.
- **Conta sempre certa.** Os valores são somados em centavos inteiros, sem erro de
  ponto flutuante. A taxa de entrega pode ser fixa, grátis ou "a combinar".
- **Sem foto de banco de imagem.** O layout é tipográfico de propósito: foto genérica
  gera reclamação quando o produto chega diferente. As fotos reais entram item por item.
- **Publicação contínua.** Hospedado na Cloudflare Pages. Uma mudança de preço entra
  no ar cerca de um minuto depois do `git push`.

---

## Stack

| Parte | Tecnologias |
| --- | --- |
| **Cardápio** | React 18, Vite 5, Framer Motion, CSS próprio |
| **Convite** | HTML, CSS e JavaScript puros, sem dependências |
| **Hospedagem** | Cloudflare Pages com deploy a cada push |

---

## Contato

Desenvolvido por **Halyson Henrique**. Quer ver o código ou uma demonstração?
Entre em contato pelo [LinkedIn](https://www.linkedin.com/in/halysonhenrique/) ou pelo [GitHub](https://github.com/halysonhenrique).
