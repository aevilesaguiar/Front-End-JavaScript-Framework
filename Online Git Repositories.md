# Online Git Repositories

Configurando um repositório Git Online
Inscreva-se para uma conta no Bitbucket ( https://bitbucket.org ) ou no GitHub ( https://github.com ). Observe que os repositórios privados no GitHub exigem uma conta paga e não estão disponíveis para contas gratuitas.

Em seguida, configure um repositório Git online chamado git-test . Observe a URL do seu repositório Git online.

Defina o repositório Git local para definir sua origem remota
No prompt, digite o seguinte para configurar seu repositório local para vincular ao seu repositório Git online:

git remote add origin <repository URL>

Enviando seus commits para o repositório online. No prompt, digite o seguinte para enviar os commits para o repositório online:

git push -u origin master


Clonar um repositório online
Para clonar um repositório online em seu computador, digite o seguinte no prompt:
git clone <repository URL>
