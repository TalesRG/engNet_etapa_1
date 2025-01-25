## UC01: Gerenciar Conta do Usuário
### Breve Descrição: 
Este caso de uso permite ao usuário criar, editar e excluir sua conta na plataforma, além de atualizar suas informações pessoais, como endereço, senha e métodos de pagamento.

### Fluxo Básico de Eventos:

1. O usuário acessa a área de configurações da conta.
2. O sistema exibe as opções de gerenciamento de conta, como atualizar perfil, alterar senha e configurar métodos de pagamento.
3. O usuário realiza a alteração desejada.
4. O sistema valida e salva as alterações.

### Fluxos Alternativos:

#### Fluxo Alternativo 1: O usuário deseja excluir sua conta:
- O usuário seleciona a opção de excluir conta.
- O sistema solicita a confirmação e uma senha válida.
- O sistema verifica se o usuário possui pedidos pendentes ou assinaturas ativas.
- Caso não haja pendências, a conta é excluída.

### Fluxos de Exceção:

- O usuário insere uma senha inválida ao tentar alterar ou excluir informações. 
- O sistema solicita nova senha.
### Pré-Condições: 
- O usuário precisa estar logado em sua conta.

### Pós-Condições: 
- As alterações realizadas pelo usuário são refletidas imediatamente.

### Requisitos Especiais:

As alterações de senha devem ser protegidas por autenticação multifator (MFA).
A exclusão de conta deve gerar uma confirmação por e-mail.