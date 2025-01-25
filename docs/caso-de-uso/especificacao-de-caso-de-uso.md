# Documentação de Casos de Uso

## UC01: Gerenciar Conta do Usuário
### Breve Descrição
Este caso de uso permite ao usuário criar, editar e excluir sua conta na plataforma, além de atualizar suas informações pessoais, como endereço, senha e métodos de pagamento.

### Fluxo Básico de Eventos
1. O usuário acessa a área de configurações da conta.
2. O sistema exibe as opções de gerenciamento de conta, como atualizar perfil, alterar senha e configurar métodos de pagamento.
3. O usuário realiza a alteração desejada.
4. O sistema valida e salva as alterações.

### Fluxos Alternativos
#### Fluxo Alternativo 1: O usuário deseja excluir sua conta
- O usuário seleciona a opção de excluir conta.
- O sistema solicita a confirmação e uma senha válida.
- O sistema verifica se o usuário possui pedidos pendentes ou assinaturas ativas.
- Caso não haja pendências, a conta é excluída.

### Fluxos de Exceção
- O usuário insere uma senha inválida ao tentar alterar ou excluir informações.
- O sistema solicita nova senha.

### Pré-Condições
- O usuário precisa estar logado em sua conta.

### Pós-Condições
- As alterações realizadas pelo usuário são refletidas imediatamente.

### Requisitos Especiais
- As alterações de senha devem ser protegidas por autenticação multifator (MFA).
- A exclusão de conta deve gerar uma confirmação por e-mail.

---

## UC02: Logar no Sistema
### Breve Descrição
Permite que o usuário acesse sua conta na plataforma, utilizando credenciais válidas (e-mail/telefone e senha) ou métodos alternativos, como autenticação por biometria ou via redes sociais.

### Fluxo Básico de Eventos
1. O usuário acessa a tela de login.
2. O sistema solicita as credenciais (e-mail/telefone e senha).
3. O usuário insere as informações e clica em "Entrar".
4. O sistema valida as credenciais e autentica o usuário.
5. O sistema redireciona o usuário à sua conta.

### Fluxos Alternativos
#### Fluxo Alternativo 1: Recuperar Senha
- O usuário clica em "Esqueci minha senha".
- O sistema envia um e-mail/SMS com instruções para redefinição.
- O usuário redefine a senha e retorna à tela de login.

### Fluxos de Exceção
- Credenciais inválidas: o sistema exibe uma mensagem de erro e permite nova tentativa.

### Pré-Condições
- O usuário deve ter uma conta registrada na plataforma.

### Pós-Condições
- O usuário será autenticado e terá acesso às funcionalidades disponíveis.

### Requisitos Especiais
- O sistema deve suportar autenticação multifator (MFA).

---

## UC03: Registrar Usuário
### Breve Descrição
Permite que novos usuários criem uma conta na plataforma, fornecendo informações básicas e aceitando os termos de uso.

### Fluxo Básico de Eventos
1. O usuário acessa a tela de registro.
2. O sistema solicita informações como nome, e-mail, senha e telefone.
3. O usuário insere as informações e confirma o registro.
4. O sistema valida os dados e cria a conta.
5. O sistema envia um e-mail/SMS de confirmação.

### Fluxos Alternativos
#### Fluxo Alternativo 1: Registro via redes sociais
- O usuário seleciona a opção de registro por redes sociais.
- O sistema redireciona para a rede social escolhida.
- Após a autorização, o sistema recupera os dados básicos do usuário e cria a conta.

### Fluxos de Exceção
- Dados inválidos ou incompletos: o sistema exibe mensagens de erro e solicita correção.

### Pré-Condições
- O usuário não deve possuir uma conta ativa na plataforma.

### Pós-Condições
- A conta do usuário será criada e ele poderá fazer login.

### Requisitos Especiais
- Senhas devem atender aos critérios de segurança (mínimo de 8 caracteres, números e caracteres especiais).

---

## UC04: Atendimento ao Cliente
### Breve Descrição
Permite que os usuários entrem em contato com o suporte para tirar dúvidas, relatar problemas ou obter ajuda relacionada a pedidos e serviços.

### Fluxo Básico de Eventos
1. O usuário acessa a página de suporte.
2. O sistema exibe as opções de atendimento (chat, telefone, FAQ, e-mail).
3. O usuário seleciona o canal desejado e descreve sua solicitação.
4. O sistema registra a solicitação e direciona ao atendente ou apresenta uma resposta automática.

### Fluxos Alternativos
#### Fluxo Alternativo 1: Solução por autoatendimento (FAQ)
- O usuário pesquisa sua dúvida na base de conhecimento.
- O sistema exibe as respostas relacionadas.
- Caso a dúvida seja solucionada, o fluxo termina.

### Fluxos de Exceção
- Canal de atendimento indisponível: o sistema sugere canais alternativos.

### Pré-Condições
- O usuário deve ter acesso à página de suporte.

### Pós-Condições
- A solicitação do usuário será registrada ou resolvida.

---

## UC05: Buscar Produto
### Breve Descrição
Permite que o usuário pesquise produtos utilizando palavras-chave.

### Fluxo Básico de Eventos
1. O usuário insere as palavras-chave na barra de pesquisa.
2. O sistema exibe uma lista de produtos correspondentes às palavras-chave.
3. O usuário visualiza os resultados e pode selecionar um produto para mais detalhes.

### Fluxos Alternativos
#### Fluxo Alternativo 1: Nenhum resultado encontrado
- O sistema exibe uma mensagem informando que não foram encontrados resultados.
- O sistema sugere alterações na pesquisa.

### Fluxos de Exceção
- Problema técnico na pesquisa: o sistema exibe uma mensagem de erro e permite nova tentativa.

### Pré-Condições
- O usuário deve ter acesso ao sistema de busca.

### Pós-Condições
- Os resultados da busca são exibidos ao usuário.

---

## UC06: Filtrar Busca
### Breve Descrição
Permite que o usuário refine os resultados da busca utilizando critérios como categoria, preço, marca e avaliação.

### Fluxo Básico de Eventos
1. O usuário seleciona um ou mais filtros na página de resultados.
2. O sistema atualiza os resultados com base nos filtros aplicados.
3. O usuário visualiza os resultados refinados.

### Fluxos Alternativos
#### Fluxo Alternativo 1: Combinação de filtros inválida
- O sistema informa que a combinação de filtros não retorna resultados.
- O sistema sugere ajustes nos filtros.

### Pré-Condições
- O usuário deve realizar uma busca antes de aplicar os filtros.

### Pós-Condições
- O usuário obtém resultados refinados.

---

## UC07: Avaliações e Comentários de Produtos
### Breve Descrição
Permite que os usuários visualizem e publiquem avaliações e comentários sobre produtos.

### Fluxo Básico de Eventos
1. O usuário acessa a página de um produto.
2. O sistema exibe avaliações e comentários de outros usuários.
3. O usuário pode adicionar uma avaliação e comentário, atribuindo uma nota ao produto.

### Fluxos Alternativos
#### Fluxo Alternativo 1: Comentário inadequado
- O sistema exibe uma mensagem informando que o comentário contém linguagem imprópria e bloqueia a publicação.

### Pré-Condições
- O usuário deve estar logado para publicar comentários.

### Pós-Condições
- O comentário do usuário será exibido para outros usuários.

---

## UC08: Denunciar Comentários
### Breve Descrição
Permite que os usuários denunciem comentários inadequados.

### Fluxo Básico de Eventos
1. O usuário clica na opção "Denunciar" em um comentário.
2. O sistema solicita o motivo da denúncia.
3. O usuário insere o motivo e confirma a denúncia.
4. O sistema registra a denúncia para análise.

### Pós-Condições
- O comentário será sinalizado para análise pela equipe de moderação.

---

## UC09: Adicionar a Wishlist (Lista de Desejos)
### Breve Descrição
Permite que o usuário salve produtos de interesse em uma lista para referência futura.

### Fluxo Básico de Eventos
1. O usuário clica em "Adicionar à lista de desejos" na página de um produto.
2. O sistema adiciona o produto à wishlist do usuário.
3. O usuário pode acessar a lista de desejos e gerenciar os produtos salvos.

### Pós-Condições
- O produto será salvo na lista de desejos do usuário.

---

## UC10: Rastrear Pedidos
### Breve Descrição
Permite que o usuário acompanhe o status de seus pedidos.

### Fluxo Básico de Eventos
1. O usuário acessa a seção "Meus pedidos".
2. O sistema exibe a lista de pedidos com status atual.
3. O usuário seleciona um pedido para mais detalhes.

### Pós-Condições
- O usuário obtém informações detalhadas sobre o status de entrega do pedido.
