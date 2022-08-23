# Configurando o Git

Git é um sistema de versão que nos permite o gerenciamento de alterações no código fonte e manter seu histórico de versões.

Existem vários sistemas de controle de versão como CVS, SVN , git sendo o mais popular para o controle de versão.

## configurações globais para Git

Verifique se o Git está instalado e disponível na linha de comando, digitando o seguinte no prompt de comando:
git --version

Para configurar seu nome de usuário para ser usado pelo Git, digite o seguinte no prompt:
git config --global user.name "Your Name"

Para configurar seu email para ser usado pelo Git, digite o seguinte no prompt:
git config --global user.email <your email address>

Você pode verificar sua configuração global padrão do Git, você pode digitar o seguinte no prompt:
git config --list

  ## Comandos básicos
  
  Inicializar repositório(quando incializamos ele marca o ramo master do meu git.
  git init
  
  Verificar o status do git, e ele informa o status atual da pasta
  git status
  
  adicionar o arquivo a área de preparação do repositótio git, ou seja adicionar na área de teste
  git add .
  
  submeter o estado atual de nossas ppastas em nosso repositório git. Ou seja será enviado ao repositório git
  git commit -m "first commit"
  
  mostra o log de todos os commits colocados no meu repositório de dados.
  git log --oneline
  
  para verificar o arquivo de um commit anterior ou do commit atual e depois trabalhar com esse arquivo.
  
  git log -oneline (veja um breve log de commits 
  
 git checkout <codigo de controle 900cfcf> <nome arquivo exemplo index.html>
  
