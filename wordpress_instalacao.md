# Wordpress na máquina local com XAMPP

- **WordPress.org** é a versão gratuita e de código aberto do WordPress.
- É possível **baixar o WordPress para o seu computador**, desenvolver o site localmente e depois **migrar para a web**, desde que você tenha:
  - Um **domínio** (ex: meusite.com)
  - Uma **hospedagem** compatível com PHP e MySQL

## XAMPP

- Fazer download e instalação do XAMPP: [https://www.apachefriends.org/pt_br/index.html](https://www.apachefriends.org/pt_br/index.html)

## Download Wordpress

- Fazer dowmload do wordpress: [https://wordpress.org/download/](https://wordpress.org/download/)

- Extrair o conteudo do arquico `.zip` baixado.

- Dentro do arquivo extraído, você encontrará uma pasta chamada `wordpress`.

- Mova a pasta `wordpress` para o diretório `htdocs` do XAMPP. Esse diretório normalmente está localizado em: `xampp\htdocs`

## Criar banco de dados para o wordpress

- Inicie o XAMPP

- Ative os módulos (start) para os serviços **Apache** e **MySQL**

- Acesse o phpMyAdmin : Digite no navegador `http://localhost/phpmyadmin`

### phpMyAdmin

- No phpMyAdmin, clique em "Novo" (no canto superior esquerdo).

- Crie um banco de dados chamado "wordpress". com a Collation: "utf8mb4_general_ci"
  
- Com o banco de dados `wordpress` selecionado, vá até a aba “Privilégios” no menu superior e clique em “Adicionar conta de usuário”.

- Dê um nome para o usuário e coloque o Nome do Host como `localhost`. ****

- Selecione a opção “conceder todos os privilégios no banco de dados wordpress”.

## Configurar o Arquivo `wp-config.php`

- Localize o arquivo `wp-config-sample.php` dentro da pasta: `xampp\htdocs\wordpress`

- Altere as seguintes linhas com as informações do seu banco de dados:

    ```php
    define( 'DB_NAME', 'nome_do_banco' );
    define( 'DB_USER', 'nome_do_usuário' );
    define( 'DB_PASSWORD', 'sua_senha' );
    define( 'DB_HOST', 'localhost' );
    define( 'DB_CHARSET', 'utf8mb4' );
    $table_prefix = 'wp_'; // ou qualquer outro prefixo que você quiser
    ```

- Salve as alterações como `wp-config.php` na mesma pasta

## Iniciar a Instalação do WordPress no Navegador

- No navegador, acesse o endereço: `localhost/wordpress`

- Escolha o idioma desejado

- Preencha os campos do formulário com as informações do seu site.

<img src="https://raw.githubusercontent.com/KarolDegan/wordpress/refs/heads/main/imagens/primeira.png" width="400" height="400"  style="margin-left: 150px; margin-bottom: 20px; margin-top: 10px;">

- Após preencher, clique no botão **"Instalar WordPress"**.

- Em seguida, clique em **"Acessar"** para fazer login.

<img src="https://github.com/KarolDegan/wordpress/blob/main/imagens/segunda.png?raw=true" width="400" height="200"  style="margin-left: 150px; margin-bottom: 20px; margin-top: 10px;">

## acessar painel de controle do wordpress

- ativar XAMPP
- `localhost/wordpress/wp-admin/` no navegador
