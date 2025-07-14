# Fazer Backup Manual do site wordpress

## Backup Completo

### Salvar o Banco de Dados

- Acesse o phpMyAdmin.
- Selecione o banco de dados usado pelo seu WordPress.
- Vá até a aba **Exportar**.
- Clique em **Exportar** para baixar o arquivo .sql.

<img src="https://raw.githubusercontent.com/KarolDegan/wordpress/refs/heads/main/imagens/quinta.png" width="600" height="200"  style="margin-left: 150px; margin-bottom: 20px; margin-top: 10px;">

### Salvar os Arquivos do Site

- Vá até a pasta onde seu WordPress está instalado: `xampp\htdocs\wordpress`
- Copie toda a pasta para uma segunda pasta
- Verifique se todos os arquivos e subpastas estão incluídos

## Backup Parcial (Somente o Essencial)

### Banco de Dados

- O banco de dados deve ser salvo completamente, da mesma forma descrita no backup completo.

### Arquivos Essenciais

Copie os seguintes arquivos e pastas do diretório WordPress:

- da pasta `wp-content` (copie apenas as subpastas):
  
  - plugins
  - themes
  - uploads

- wp-config.php

- .htaccess (caso você use WordPress Multisite ou regras específicas)

## Restaurando o site a partir do backup parcial

- substituir os arquivos pelos arquivos de backup

### backup do banco

- provavelmente a melhor opção a melhor opção é apagar o banco e subir ele novamente com o seu backup

- apague seu banco wordpress

- crie um mesmo banco seguindo as mesmas configurações de nome, usuário, senha, host, charset, definidas no arquivo `wp-config.php`

- 