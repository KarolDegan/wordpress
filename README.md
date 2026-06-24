# Instalação e primeiros acessos ao WordPress (local)

Este Repositório descreve, passo a passo, como instalar o WordPress em uma máquina local usando XAMPP e como realizar os primeiros acessos, incluindo opções para acesso pela rede local, backup e habilitação de Multisite.

## Índice dos arquivos

- [wordpress_instalacao.md](wordpress_instalacao.md) — Guia passo a passo para instalar o WordPress localmente com XAMPP: download, configuração do banco no phpMyAdmin, edição de wp-config.php, execução da instalação via navegador e acesso ao painel (wp-admin). Contém imagens ilustrativas.
- [backup_wordpress.md](backup_wordpress.md) — Instruções para criar backups completos e parciais do WordPress: exportar banco de dados (.sql), copiar pasta do site, quais pastas/arquivos essenciais (plugins, themes, uploads, wp-config.php, .htaccess) e passos para restaurar.
- [acesso_rede_local.md](acesso_rede_local.md) — Como configurar o WordPress local para ser acessado por outros dispositivos na mesma rede: ajustes em wp-config.php (WP_HOME / WP_SITEURL) e configuração de VirtualHost no Apache (httpd-vhosts.conf).
- [wordpress_multisites.md](wordpress_multisites.md) — Passo a passo para habilitar e administrar o recurso Multisite do WordPress: ativação (WP_ALLOW_MULTISITE), instalação da rede pelo painel, diretivas a adicionar ao wp-config.php, regras de .htaccess e como criar novos sites na rede.
