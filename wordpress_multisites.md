# Habilitação de Multisites no WordPress

## O que é o WordPress Multisite?

- O recurso Multisite do WordPress permite gerenciar múltiplos sites a partir de um único painel de administração.
- Ele é ideal para redes de sites com conteúdos e funcionalidades semelhantes

## Níveis de Administração

### Super Admin

- Ativar e gerenciar o modo Multisite;
- Definir permissões de usuários em toda a rede;
- Instalar e gerenciar plugins e temas (visível para todos os sites da rede);

### Site Admin

- O Site Admin (Administrador de Site) gerencia um ou mais sites dentro da rede, conforme suas permissões.
- Ativar ou desativar plugins (apenas os já disponíveis na rede);
- Gerenciar conteúdo, temas e configurações do(s) site(s) atribuídos;

## Etapas para Habilitar o WordPress Multisite

### 1 Fazer backup

- instalr plugin `All-in-One WP Migração e Backup`

### 2 Inserir Diretiva Multisite no Arquivo de Configuração

- na pasta xampp\htdocs\wordpress edite o arquivo wp-config.php
- acrescentar `define( 'WP_ALLOW_MULTISITE', true );` acima da linha `/* That's all, stop editing! Happy publishing. */`

### 3 Desativar Plugins Temporariamente

- Antes de configurar a rede, é recomendável desativar todos os plugins para evitar conflitos.

### 4 Instalar a Rede

- No painel do WordPress: Ferramentas > Instalação da Rede.
- entrar em ferramentas: instalação da rede
- Escolha o tipo de estrutura:
  - Subdiretórios (seusite.com/site1)
  - Subdomínios (site1.seusite.com) (requer configuração de DNS e servidor)
- Informe o nome da rede e o email do administrador.
- clique em instalar

## 5 Configurando os Arquivos do WordPress

<img src="https://raw.githubusercontent.com/KarolDegan/wordpress/refs/heads/main/imagens/terceira.png" width="600" height="300"  style="margin-left: 150px; margin-bottom: 20px; margin-top: 10px;">

- no arquivo wp-config.php copie o trecho fornecido e cole acima da linha: `/* That's all, stop editing! Happy publishing. */`

```php
define( 'MULTISITE', true );
define( 'SUBDOMAIN_INSTALL', false );
define( 'DOMAIN_CURRENT_SITE', 'localhost' ); #mudar para seu domínio
define( 'PATH_CURRENT_SITE', '/wordpress/' );
define( 'SITE_ID_CURRENT_SITE', 1 );
define( 'BLOG_ID_CURRENT_SITE', 1 );
```

- no arquivo .htaccess na mesma pasta. Substitua o conteúdo atual do arquivo pelo código fornecido na instalação da rede.

```bash
RewriteEngine On
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
RewriteBase /wordpress/
RewriteRule ^index\.php$ - [L]

# add a trailing slash to /wp-admin
RewriteRule ^([_0-9a-zA-Z-]+/)?wp-admin$ $1wp-admin/ [R=301,L]

RewriteCond %{REQUEST_FILENAME} -f [OR]
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^ - [L]
RewriteRule ^([_0-9a-zA-Z-]+/)?(wp-(content|admin|includes).*) $2 [L]
RewriteRule ^([_0-9a-zA-Z-]+/)?(.*\.php)$ $2 [L]
RewriteRule . index.php [L]
```
