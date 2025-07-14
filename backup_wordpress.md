# Fazer Backup Manual do site wordpress

## Backup Completo

### Salvar o Banco de Dados

- Acesse o phpMyAdmin.
- Selecione o banco de dados usado pelo seu WordPress.
- Vá até a aba **Exportar**.
- Clique em **Exportar** para baixar o arquivo .sql.

<img src="https://raw.githubusercontent.com/KarolDegan/wordpress/refs/heads/main/imagens/quinta.png" width="800" height="400"  style="margin-left: 150px; margin-bottom: 20px; margin-top: 10px;">

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

### Restaurando os Arquivos

- Substitua os arquivos existentes na instalação atual pelos arquivos do seu backup parcial:

  - wp-content/plugins/
  - wp-content/themes/
  - wp-content/uploads/
  - wp-config.php
  - .htaccess (se aplicável)

### Restaurando o Banco de Dados

- Acesse o phpMyAdmin

- Apague o banco de dados atual (caso esteja corrompido ou desatualizado).

- Crie um novo banco de dados com as mesmas configurações do antigo:
  
  - Nome do banco
  - Usuário
  - Senha
  - Host
  - Charset

    Essas informações devem corresponder ao que está definido no arquivo wp-config.php. Se necessário, edite o wp-config.php para refletir as novas configurações do banco.

- Selecione o banco de dados recém-criado.

- Vá até a aba **Importar**.

<img src="https://raw.githubusercontent.com/KarolDegan/wordpress/refs/heads/main/imagens/sexta.png" width="800" height="400"  style="margin-left: 150px; margin-bottom: 20px; margin-top: 10px;">

- Clique em **Escolher arquivo** e selecione o seu backup do banco de dados (extensão .sql).

- Clique em **Importar** para concluir o processo.