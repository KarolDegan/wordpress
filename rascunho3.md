## criando um tema para o wordpress

- minicurso Marcelo Xavier Vieira Youtube

- xampp\htdocs : precisa ser criada aqui

- mudar o prefixo das tabelas por segurança


## Multisites

- gerenciar multiplos sites com um pinel de controle
- conteuso e funcionalidades semelantes

### subdiretórios

- exemplo.com/site1
- exemplo.com/site2

### subdomínios

site1.exemplo.com
sete2.exemplo.com


### super Admin

- contola toda a rede de websites 
- ativam os multisites
- permissões de usuários
- instalações de plugns e telas

### site admin

- controla 1 ou mais sites dentro da rede dependendo das permições
- controla se ativa ou desativa os plugins mas não sobre quias tem acesso

##

- no wp_config.php acrescentar `define( 'WP_ALLOW_MULTISITE', true );`
- acima da linha `/* That's all, stop editing! Happy publishing. */`

## All-in-One WP Migração e Backup

- fazer backup

## desativar plugins

- entrar em ferramentas: instalação da rede
- escolher emntre subdiretório e subdomínios
- nome da rede e email do administrador
- instalar

## Habilitando a rede

### acrescentar código no arquivo de configuração
- wp-config.php
- colar o que for apresentado acima da linha `/* That's all, stop editing! Happy publishing. */`

- htaccess
- colar o codigo apresentado no lugar do que estiver no arquivo