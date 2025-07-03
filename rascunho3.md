# Compartilhar a sua pagina com outras pessas na mesma rede

## Apache

- wp_config.php
`define('WP_HOME','http://192.168.1.100/wordpress');`
`define('WP_SITEURL','http://192.168.1.100/wordpress');`

- httpd-vhosts.conf
```bash
    <VirtualHost *:80> #define a porta 80, mudar isso levaria a mudar alguns outros arquivos como
    DocumentRoot "C:/xampp/htdocs" # os arquivos servidos no site estão a pasta htdocs
    ServerName 192.168.1.100    # diz que o virtualhost será usado com esta URL
    <Directory "C:/xampp/htdocs"> # configura permissões para a pastas do site
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
    </VirtualHost>
```
