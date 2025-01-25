## Breve Descrição
Este caso de uso descreve o processo pelo qual um usuário seleciona produtos, adiciona ao carrinho, escolhe as opções de entrega e pagamento, e conclui a compra.

---

## Fluxo Básico de Eventos
1. O usuário acessa a página do produto e clica em **Adicionar ao Carrinho**.
2. O sistema adiciona o produto ao carrinho e exibe uma mensagem de confirmação.
3. O usuário acessa o **Carrinho de Compras** e clica em **Finalizar Compra**.
4. O sistema solicita que o usuário confirme o endereço de entrega.
5. O usuário seleciona um método de entrega (padrão, expresso, etc.).
6. O sistema exibe as opções de pagamento disponíveis.
7. O usuário seleciona o método de pagamento e insere os dados necessários (cartão de crédito, débito, boleto, etc.).
8. O sistema valida o pagamento e gera um número de pedido.
9. O sistema exibe a confirmação do pedido e o status inicial ("Processando").

---

## Fluxos Alternativos
- **Fluxo Alternativo 1: Produto indisponível no estoque**
    1. O usuário tenta adicionar ao carrinho um produto fora de estoque.
    2. O sistema exibe uma mensagem de erro e sugere produtos similares.

- **Fluxo Alternativo 2: Pagamento falhou**
    1. O usuário insere os dados do pagamento, mas a transação é recusada.
    2. O sistema informa o motivo da falha (por exemplo, saldo insuficiente ou dados incorretos) e permite ao usuário tentar novamente.

- **Fluxo Alternativo 3: Endereço não cadastrado**
    1. O usuário não possui um endereço cadastrado no sistema.
    2. O sistema solicita que o usuário insira um novo endereço antes de continuar.

---

## Fluxos de Exceção
- **Exceção 1: Sessão expirada**
    1. O usuário fica inativo por muito tempo durante o processo de compra.
    2. O sistema desconecta o usuário e solicita que ele faça login novamente.

- **Exceção 2: Produto removido do carrinho**
    1. Durante a finalização, o produto é removido do estoque por outro pedido.
    2. O sistema notifica o usuário e remove o produto do carrinho.

---

## Pré-Condições
- O usuário deve estar logado no sistema.
- O produto deve estar disponível no estoque.

---

## Pós-Condições
- O pedido do usuário é registrado no sistema com um número único.
- O status inicial do pedido é exibido ("Processando").

---

## Pontos de Extensão
- **Adicionar Seguro ao Produto**: Antes de finalizar a compra, o usuário pode optar por adicionar seguro.
- **Cupom de Desconto**: O sistema permite que o usuário insira um cupom de desconto antes de concluir o pagamento.

---

## Requisitos Especiais
- A validação de pagamentos deve ser feita de forma segura utilizando criptografia SSL/TLS.
- O sistema deve suportar diferentes métodos de pagamento, como cartão de crédito, débito, boleto e Pix.

---

## Informações Adicionais
- Após a compra, o sistema deve enviar um e-mail de confirmação contendo os detalhes do pedido, previsão de entrega e nota fiscal eletrônica.
