# Acesso por IP na Rede Interna

Este guia mostra como configurar seu servidor local (XAMPP + WordPress) para ser acessado por outros dispositivos na mesma rede local.

## configurações do documento `wp_config.php`

- abra o arquivo `wp_config.php` dentro da pasta `xampp\htdocs\wordpress`

- acrescentar os comandos abaixo, acima da linha: `/* That's all, stop editing! Happy publishing. */`

```bash
    define('WP_HOME','http://192.168.1.100/wordpress');
    define('WP_SITEURL','http://192.168.1.100/wordpress');
```

- Substitua 192.168.1.100 pelo IP do seu computador na rede local.

## configurações no documento `httpd-vhosts.conf`

-  abra o arquivo `httpd-vhosts.conf` dentro da pasta `xampp\apache\conf\extra`

- acrescentar os comandos abaixo ao final do documento

```bash
    <VirtualHost *:80> #define a porta 80, mudar isso levaria a mudar alguns outros arquivos
    DocumentRoot "C:/xampp/htdocs" # os arquivos servidos no site estão na pasta htdocs
    ServerName 192.168.1.100    # diz que o virtualhost será usado com esta URL
    <Directory "C:/xampp/htdocs"> # configura permissões para a pastas do site
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
    </VirtualHost>
```
