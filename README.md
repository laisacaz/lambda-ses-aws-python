## Lambda para envio de emails através da AWS

### A lambda encontrada nesse repositório realiza o disparo de um email para o destinatário desejado, porém é necessário que sejam realizadas as configurações abaixo:

## Configurações

* #### Configurar emails remetente/destinatário:
  - Para que o email remetente possa realizar os envios e para que o destinatário receba, você precisa torná-los verificados no serviço "Amazon Simple Email Service".
    - Na barra pesquisar escreva "Amazon Simple Email Service" e selecionar a opção encontrada. 
    - No menu lateral esquerdo haverá o menu "Configurações" e dentro dele selecionar a opção "Identidades"
    - Selecionar o botão "Criar identidade"
    - Marcar a opção "Endereço de email"
    - Selecionar "Criar identidade"
    - É preciso cadastrar todos os emails envolvidos no envio e recebimento de emails.
    - A AWS irá disparar um email de confirmação aos emails que foram cadastrados
    - É necessário acessar os emails cadastrados para abrir o link que foi enviado, ou pedir para que o destinatário o acesse, dessa forma ele será verificado.
* #### Dependências:
  - Para que a lambda funcione corretamente, precisa ter instalado o pacote "boto3":
    * O arquivo txt "requirements" já realiza a instalação, através do código que está dentro dele. 
* #### Testando o código:
  - Para testar a lamba dentro da AWS:
  -    
