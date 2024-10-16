# Tema - Inclusão Social

  # Introdução
  
  Este projeto tem como finalidade de divulgar o movimento escoteiro e o GETS (Grupo Escoteiro Terra da Saudade).
Um dos principais motivos para a construção deste projeto é facilitar o cadastro dos possíveis escoteiros/voluntários
e facilitar o controle de dados para os chefes, como por exemplo: ter um certo controle das pessoas que mudam de endereço,
se vai parar de participar das atividades do grupo e entre outros.

  # O que se espera?

  Se espera que o projeto seja bastante utilizado pela comunidade de escoteiros e que facilite o dia a dia dos chefes
  que são responsáveis pelo controle do grupo.

  # Features

  O nosso projeto tem como foco um cadastro simples de se fazer, uma comunicação com os chefes do grupo de maneira mais
  fácil e sem precisar falar com eles diretamente logo de cara, assim podendo tirar as maiorias das dúvidas dentro do
  nosso site e ter uma comunicação à distância sem precisar falar diretamente com os chefes do grupo para finalização
  de cadastro.

  O nosso projeto tem muito foco em acessibilidade, assim podendo facilitar o uso dos usuários que acabam tendo mais
  dificuldade com o uso da tecnologia, deixando bem prático e bem simplificado a utilização do nosso software.

# Requisitos Não Funcionais

# Requisitos Funcionais

# Regras de Negócio

# Projeto Integrador

## Sumário

1. [Configuração De Ambiente](#environment-configuration)
    - [Instalação do Nodejs](#nodejs-instalation)
    - [Como puxar o repositório para o meu computador?](#how-to-pull)
2. [Baixando e configurando ESLint](#make-eslint-configurations)
3. [Como fazer o deploy](#deploy)
4. [Boas práticas do trabalho com git](#good-practices)

<a id="environment-configuration"></a>

## Configurações De Ambiente

<a id="nodejs-instalation"></a>

### Instalação do Nodejs

1. Verifique se você possue o `Node.js` instalado executando o seguinte comando: `node --version`. Se o comando não retornar
a versão do Node.js, então siga para os próximos passos. Caso contrário, pule para a próxima sessão.
2. Instale o Node.js no seu computador seguindo o passo a passo abaixo que corresponde ao seu sistema operacional.
  - Windows:
    - Acessar o site oficial do Node.js [https://nodejs.org/en](node.js)
    - Baixar a versão LTS (Long-Term Support)
    - Execute o primeiro passo para verificar se a instalação foi concluída com sucesso
      - Caso ainda não funcione, tente executar os seguintes passos:
        1. Feche e abra o seu terminal
        2. Execute novamente o comando `node --version`. Caso ainda não funcione, execute os próximos passos.
        3. Abra o Power Shell em modo administrador
        4. Execute o seguinte comando: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`
        5. Rode novamente o comando `node --version`.
  - Mac:
    - No terminal no Mac, insira os seguintes comandos:
      ```bash
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)";
        brew update;
        brew install node;
      ```
    - Em seguida, execute `node --version` e confirme se a instalação foi concluída com sucesso
  - Linux
    - No terminal no Linux, insira os seguintes comandos:
      ```bash
        sudo apt update
        sudo apt install curl
        sudo curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
        nvm install --lts
      ```

<a id="how-to-pull"></a>

### Como puxar o repositório para o meu computador?

1. Para trazer o repositório do GitHub para o seu computador, execute um dos seguintes comandos (o mais comum é p HTTPS, mas se souber o que está fazendo, pode executar qualquer um dos outros):
    - HTTPS
        ```bash
          git clone https://github.com/Interdisciplinary-Project/Frontend.git
        ```
    - SSH
        ```bash
          git clone git@github.com:Interdisciplinary-Project/Frontend.git
        ```
    - GitHub CLI
        ```bash
          gh repo clone Interdisciplinary-Project/Frontend
        ```
2. Agora, execute os seguintes comandos para configurar o seu ambiente de desenvolvimento:
    ```bash
      cd Frontend # Este comando irá entrar dentro da pasta do projeto
      npm i # Este comando irá instalar todas as dependências necessárias para rodar o projeto
      code . # Este comando só deverá ser usado se você estiver usando o Visual Studio Code como Editor de Código Fonte
      npm run dev # Este comando irá rodar o ambiente de desenvolvimento onde você poderá ver suas alterações em tempo real
    ```

<a id="make-eslint-configurations"></a>

### Baixando e configurando o ESLint

#### Observação

Caso não queira instalar manualmente, rodar o projeto com o comando `npm run dev`
que a extensão será instalada automaticamente e o projeto já será rodado para
você começar a desenvolver. Caso queira realizar a instalação manual vá para
a próxima sessão. Após a instalação da extensão, vá para a sessão [Configurações do ESLint](#eslint-configuration)

Caso haja algum problema ao executar o comando `npm run dev`, siga os seguintes passos:

1. Execute `npm run build`. Se nenhum problema acontecer, execute `npm run start`. Caso
algum erro aconteça, vá para o próximo passo.
2. Neste momento, você deve ir para a branch main com `git switch main` e executar um
`git pull origin main`. Após isso, vá novamente para o passo número 1. Se mesmo assim
o problema persistir, entre em contato com o líder do projeto.

### Instalação manual

1. Inicialmente se faz necessário instalar uma extensão chamada `ESLint`. Para isso, procurem a aba de extensões (ou usem o atalho `ctrl+x`). Daí, pesquisem por `ESLint` e irá aparecer a extensão abaixo. Instale-a e vá para o próximo passo.

![image](https://github.com/user-attachments/assets/29d0aa7f-4c0e-42f3-95e6-b839c2a52086)


<a id="eslint-configuration"></a>

### Configurações do ESLint

1. Agora, com a extensão já instalada, você deve abrir o JSON de configurações do VSCode. Para isso, use o atalho `ctrl+shift+p`. Irá aparecer a seguinte barra de pesquisa:

![image](https://github.com/user-attachments/assets/e3b55b90-774b-4996-bf81-f299aef784ce)


2. Agora, pesquise `Preferences: Open User Settings (JSON)` e tecle `Enter`.
3. Dentro do par de {} que irá ter neste arquivo (caso ele não tenha nenhuma configuração previamente preenchida), insira os comandos abaixo

![image](https://github.com/user-attachments/assets/8d324304-e8ff-4af4-a1d5-9c7806e8bece)


<a id="deploy"></a>

## Como fazer o deploy

Para realizar o deploy, basta executar o seguinte comando:

```bash
npm run deploy
```

Esse comando irá executar o linting, o build e o deploy. Assim, somente o código mais atualizado irá subir para produção

<a id="good-practices"></a>

## Boas práticas do trabalho com git

Quando se trabalha em um repostiório de código compartilhado utilizando Git, existem algumas práticas que são interessante de se seguir. Segue uma lista do que sempre (ou quase sempre) deve ser feito antes de iniciar qualquer desenvolvimento.

1. Sempre que for realizar alguma alteração no código, crie uma nova branch a partir da main. Para fazer isso, siga os seguintes passos:
  - Execute o comando `git switch main` para garantir que você está na branch principal
  - Execute `git switch -c NOME_DA_SUA_BRANCH` para criar uma nova branch a partir da main
  - Faça todo o seu desenvolvimento. Então, quando quiser enviar as suas alterações para o GitHub, execute:
      ```bash
        git add .
        git commit -m "AQUI_VAI_UMA_MENSAGEM_DE_COMMIT_QUE_DESCREVA_DE_FORMA_CLARA_AS_SUAS_ALTERAÇÕES"
        git push origin ESCREVA_AQUI_O_NOME_DA_SUA_BRANCH
      ```
  - Vá até o seu GitHub, no repositório Frontend, e clique no botão verde de `Compare & Pull Request`.
    ![image](https://github.com/user-attachments/assets/9b05956b-95db-4415-abaf-c26ba14aee51)
  - Confira se a sua branch está na direita e na esquerda está a branch main
  - ![image](https://github.com/user-attachments/assets/7932559e-c057-4c96-8ddb-b67a07edf335)
  - Clique no botão de `Create Pull Request`
  - ![image](https://github.com/user-attachments/assets/43340389-3de9-481b-a979-e7b0619f09bd)
  - Ao fim, você chegará nesta tela. Não faça mais nada e avise alguém para revisar o código (pelo WhatsApp mesmo) e fazer o merge do seu código com a branch principal
    ![image](https://github.com/user-attachments/assets/4d4ec816-2ca8-4eb2-a2e0-1a980c7930b1)
2. Sempre que finalizar uma tarefa e for iniciar a próxima tarefa garanta que a sua branch main esteja atualizada e jamais crie novas branchs de desenvolvimento a partir de qualquer outra branch que não seja a main. Assim, após a criação do seu `Pull Request`, execute os seguintes passos:
    ```bash
      git switch main
      git pull origin main # Se tiver confiança, pode executar somente git pull
      # Aqui você pode criar sua nova branch de desenvolvimento normalmente e seguir trabalhando
    ```
3. Garanta que o seu código esteja funcionando antes de subir para o GitHub. Ou seja, teste o que você fez e garanta que não quebrou também o que já estava pronto anteriormente.



