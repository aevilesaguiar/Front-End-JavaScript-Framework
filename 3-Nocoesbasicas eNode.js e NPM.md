# Noções básicas de Node.js e NPM

Objetivos e Resultados

Neste exercício, você aprenderá os conceitos básicos de Node e NPM. Ao final deste exercício, você será capaz de:

Configure o arquivo package.json na pasta do projeto para configurar seu Node e NPM para este projeto

Instale um módulo NPM e use-o em seu projeto

Inicializando package.json
No prompt de comando em sua pasta git-test , digite

1
npm init
Siga as instruções e responda às perguntas da seguinte forma: aceite os valores padrão para a maioria das entradas, exceto defina o ponto de entrada como index.html

Isso deve criar um arquivo package.json em sua pasta git-test .

Instalando um módulo NPM

Instale um módulo NPM, lite-server, que permite executar um servidor web de desenvolvimento baseado em Node.js e servir seus arquivos de projeto. Para fazer isso, digite o seguinte no prompt:

npm install lite-server --save-dev


Em seguida, abra package.json em seu editor e modifique-o conforme mostrado abaixo. Observe a adição de duas linhas, a linha 7 e a linha 9.

![image](https://user-images.githubusercontent.com/52088444/186238621-3b2f4291-79b3-48bd-9a3a-80381bc44301.png)

Em seguida, inicie o servidor de desenvolvimento digitando o seguinte no prompt:

npm start

Isso deve abrir sua página index.html em seu navegador padrão.

Se você agora abrir a página index.html em um editor e fizer alterações e salvar, o navegador deverá atualizar imediatamente para refletir as alterações.

Configurando .gitignore
Em seguida, crie um arquivo no diretório do projeto chamado .gitignore ( Nota : o nome começa com um ponto) Em seguida, adicione o seguinte ao arquivo .gitignore

node_modules

Faça um git commit e envie as alterações para o repositório online. Você notará que a pasta node_modules não será adicionada ao commit e não será carregada no repositório.

Conclusões
Neste exercício, você aprendeu a configurar o package.json, instalar um pacote npm e iniciar um servidor de desenvolvimento.

