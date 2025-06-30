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

### 2

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

- no arquivo wp-config.php copie o trecho fornecido e cole acima da linha: `/* That's all, stop editing! Happy publishing. */`

- no arquivo .htaccess na mesma pasta. Substitua o conteúdo atual do arquivo pelo código fornecido na instalação da rede.
