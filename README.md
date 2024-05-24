## Lambda para envio de emails através da AWS

### A lambda encontrada nesse repositório realiza o disparo de um email para o destinatário desejado, porém é necessário que sejam realizadas as configurações abaixo:

## Configurações

* #### Configurar emails remetente/destinatário:
  - Para que o email remetente possa realizar os envios e para que o destinatário receba, você precisa torná-los verificados no serviço "Amazon Simple Email Service".
    - Na barra pesquisar escreva "Amazon Simple Email Service" e selecionar a opção encontrada. 
    - No menu lateral esquerdo haverá o menu "Configurações" e dentro dele selecionar a opção "Identidades"
    - Selecionar o botão "Criar identidade"
    - Marcar a opção "Endereço de email"
    - Escreva qual será o email a verificar
    - Selecionar "Criar identidade"
    - É preciso cadastrar todos os emails envolvidos no envio e recebimento de emails.
    - A AWS irá disparar um email de confirmação aos emails que foram cadastrados
    - É necessário acessar os emails cadastrados para abrir o link que foi enviado, ou pedir para que o destinatário o acesse, dessa forma ele será verificado.
* #### Criar função lambda:
  - Na barra pesquisar escreva "Lambda" e selecionar a opção encontrada.
  - Selecionar o botão criar função
  - Insira o nome da função
  - Selecionar a linguagem de programação Python 3.12
  - Selecionar o botão criar função
* #### Criar permissão para lambda:
  - Para que a lambda consiga realizar o envio de email, é necessário conceder a permissão a ela da seguinte forma:
    - Entrar na lambda criada
    - Selecionar o menu de "Configurações"
    - Selecionar a opção "Permissões"
    - Clicar no link abaixo de "Nome da função"
    - Selecionar o botão "Adicionar permissões" e marcar a opção "Criar política em linha"
    - Procurar pelo serviço "SES"
    - Clicar na opção "Gravação" e marcar as opções "SendRawEmail" e "SendEmail"
    - Em recursos selecionar "Tudo"
    - Dê um nome a permissão e apertar o botão de salvar
* #### Vincular a permissão com a lambda:
  -  
* #### Dependências:
  - Para que a lambda funcione corretamente, precisa ter instalado o pacote "boto3":
    * O arquivo txt "requirements" já realiza a instalação, através do código que está dentro dele. 
* #### Testando o código:
  - Para testar a lamba dentro da AWS:
  -    
