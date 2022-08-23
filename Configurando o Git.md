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