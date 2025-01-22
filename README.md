# Como Executar o Projeto

Este guia fornece instruções detalhadas para executar o projeto em sistemas Linux e Windows. Siga as etapas abaixo para garantir que todas as dependências necessárias sejam instaladas corretamente e o projeto funcione sem problemas.

---

## Pré-requisitos

Antes de começar, certifique-se de instalar as seguintes dependências principais:

- [NodeJS](https://nodejs.org/en/download)
- [npm](https://www.npmjs.com/)

### Requisitos de Versão

- **Node.js**: v22.13.1
- **npm**: v10.9.2

---

## Configuração

### Linux

Execute os comandos abaixo no terminal para configurar o ambiente:

```bash
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

# Download and install Node.js:
nvm install 22

# Verify the Node.js version:
node -v # Should print "v22.13.1".
nvm current # Should print "v22.13.1".

# Verify npm version:
npm -v # Should print "10.9.2".
```

### Windows

Siga estas etapas no PowerShell:

```powershell
# Download and install fnm:
winget install Schniz.fnm

# Download and install Node.js:
fnm install 22

# Verify the Node.js version:
node -v # Should print "v22.13.1".

# Verify npm version:
npm -v # Should print "10.9.2".
```

### Executando o Projeto Localmente

Após configurar o ambiente, siga as instruções abaixo para executar o projeto:

1. **Instalar dependências do projeto**

Na raiz do projeto, execute:

```bash
npm install
```
2. **Iniciar o servidor de desenvolvimento**

Após instalar as dependências, execute:

```bash
npm run serve
```
Esse comando já abre o seu navegador no localhost.


## Histórico de Versão

| Versão   | Data       | Autor(es)                                  | Descrição                                                                                   |
|----------|------------|--------------------------------------------|---------------------------------------------------------------------------------------------|
| `0.1`    | 22-01-2025 | [Bruno](https://github.com/brunobreis)     | Versão inicial do documento/projeto.                                                        |