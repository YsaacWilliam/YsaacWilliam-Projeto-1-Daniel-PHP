# YsaacWilliam-Projeto-1-Daniel-PHP

🎮 Projeto CRUD de Clientes e Jogos Gratuitos

Este projeto foi desenvolvido como atividade prática da disciplina de Programação Web, com o objetivo de aplicar os conceitos de CRUD (Create, Read, Update, Delete) utilizando PHP e MySQL, além de HTML e CSS.

O sistema possui dois módulos principais:
Cadastro de Clientes
Cadastro de Jogos Gratuitos, com links de download fornecidos pelas próprias empresas desenvolvedoras.

🧠 Objetivo

O projeto visa demonstrar o funcionamento completo de um CRUD em PHP com integração ao MySQL, permitindo:
Cadastrar novos registros (Create)
Listar registros existentes (Read)
Editar informações (Update)
Excluir registros (Delete)

⚙️ Tecnologias Utilizadas

PHP 8+
MySQL (MariaDB)
HTML5
CSS3
XAMPP / WAMP (para ambiente local)

🗂️ Estrutura do Projeto

📁 Projeto/
├── index.php                 # Página inicial com navegação
├── config.inc.php            # Conexão com o banco de dados
├── clientes-admin.php        # Lista e gerencia clientes
├── clientes-cadastro.php     # Insere novos clientes
├── clientes-altera.php       # Atualiza dados dos clientes
├── clientes-excluir.php      # Exclui clientes
│
├── jogos-admin.php           # Lista e gerencia jogos
├── jogos-cadastro.php        # Insere novos jogos
├── jogos-altera.php          # Atualiza dados dos jogos
├── jogos-excluir.php         # Exclui jogos
├── jogos.php                 # Página pública de exibição dos jogos
│
├── imagens/                  # Imagens dos jogos
├── css/                      # Estilos do site
└── banco.sql                 # Script do banco de dados

🧩 Estrutura do Banco de Dados

O arquivo banco.sql contém toda a estrutura necessária para o funcionamento do projeto.

Banco de dados: banco

🧍 Tabela clientes:
CREATE TABLE clientes (
  id INT(11) NOT NULL AUTO_INCREMENT,
  cliente VARCHAR(255) NOT NULL,
  cidade VARCHAR(255) NOT NULL,
  estado VARCHAR(100),
  data_cadastro TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (id)
);

🎮 Tabela jogos:
CREATE TABLE jogos (
  id INT(11) NOT NULL AUTO_INCREMENT,
  nome_jogo VARCHAR(255) NOT NULL,
  empresa VARCHAR(255) NOT NULL,
  descricao TEXT,
  link_download VARCHAR(500) NOT NULL,
  imagem VARCHAR(500),
  data_lancamento DATE,
  data_cadastro TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (id)
);

Exemplo de dados inseridos:
INSERT INTO jogos (nome_jogo, empresa, descricao, link_download, imagem, data_lancamento)
VALUES
('Epic Game 1', 'Epic Games', 'Jogo gratuito da semana na Epic Games', 'https://store.epicgames.com/pt-BR/free-games', 'imagens/epic-game1.jpg', '2024-01-15'),
('Steam Free Game', 'Valve', 'Jogo gratuito disponível na Steam', 'https://store.steampowered.com', 'imagens/steam-game.jpg', '2024-02-01');

🚀Como Executar o Projeto:

Instale e inicie o XAMPP (ou WAMP).
Extraia o projeto na pasta htdocs (exemplo: C:\xampp\htdocs\Atividade_Daniel_04_11).
Abra o phpMyAdmin e crie um banco chamado banco.
Importe o arquivo banco.sql fornecido na pasta do projeto.
Edite o arquivo config.inc.php, se necessário:

$servidor = "localhost";
$usuario  = "root";
$senha    = "";
$banco    = "banco";

No navegador, acesse:

http://localhost/Atividade_Daniel_04_11/index.php

🎨 Personalização

Além do css o projeto possui um  fundo animado (como o GIF inspirado no jogo Balatro na área de jogos).

🧩 Funcionalidades Principais

✅ Cadastro de Clientes
✅ Cadastro de Jogos Gratuitos
✅ Edição e exclusão de registros
✅ Exibição pública dos jogos com imagens e links de download
✅ Banco de dados totalmente funcional

💡 Problemas Conhecidos <!--infelizmente-->

Não há validação de tipo de arquivo na hora do upload da imagem.
O sistema aceita qualquer link de download (não verifica se está ativo).
Layout básico, sem responsividade para telas pequenas.

👨‍💻 Desenvolvido por:

Ysaac William
Curso: Ciência da Computação P2 - Programação Web - C
Atividade Avaliativa – Novembro / 2025

