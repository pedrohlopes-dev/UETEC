# UEtec 👕

Sistema web de e-commerce desenvolvido para facilitar o processo de compra e gerenciamento de uniformes acadêmicos da **ETEC de Poá**, eliminando filas e processos manuais.

> Trabalho de Conclusão de Curso — Técnico em Informática para Internet  
> ETEC de Poá · Centro Paula Souza · 2025

---

## 📋 Sobre o Projeto

A UEtec é uma plataforma que centraliza os pedidos de uniformes da instituição, oferecendo uma experiência de compra prática e segura para alunos e responsáveis, além de um painel administrativo para funcionários gerenciarem estoque e pedidos.

**Problema resolvido:** alunos precisavam se deslocar até a escola em dias sem aula, enfrentar filas e aguardar dias para confirmar seus pedidos.

---

## ✨ Funcionalidades

### Cliente
- Cadastro com validação de e-mail institucional (`@etec.sp.gov.br`)
- Login com autenticação segura (senha criptografada com `password_hash`)
- Catálogo de produtos com carrinho de compras
- Seleção de tamanho e quantidade por produto
- Finalização de pedido com geração de código único
- Histórico de pedidos com status em tempo real

### Administrador
- Painel administrativo com controle de estoque
- Adição, edição e remoção de produtos
- Visualização de pedidos e relatório de vendas
- Upload de imagens de produtos

---

## 🛠️ Tecnologias Utilizadas

| Camada | Tecnologias |
|--------|------------|
| Front-end | HTML5, CSS3, JavaScript |
| Back-end | PHP |
| Banco de dados | MySQL (via WampServer) |
| Design | Figma |
| Versionamento | Git & GitHub |
| Gerenciamento | Trello (Kanban + Scrum) |

---

## 🗄️ Banco de Dados

O sistema conta com 9 tabelas relacionais:

`etecs` · `clientes` · `usuarios` · `categorias` · `produtos` · `pedidos` · `itens_pedido` · `pagamentos` · `avaliacoes`

---

## 🚀 Como Rodar Localmente

**Pré-requisitos:** XAMPP ou WampServer instalado.

1. Clone o repositório:
```bash
git clone https://github.com/pedrohlopesdeoliveira/UETEC.git
```

2. Mova a pasta para o diretório do servidor:
```bash
# XAMPP
mv UETEC /opt/lampp/htdocs/

# WampServer (Windows)
# Mova para C:\wamp64\www\
```

3. Importe o banco de dados pelo phpMyAdmin:
   - Crie um banco chamado `uetecbd`
   - Importe o arquivo `.sql` disponível na pasta `/banco`

4. Configure a conexão em `php/conexao.php`:
```php
private $host = "localhost";
private $user = "SEU_USUARIO";
private $senha = "SUA_SENHA";
private $banco = "uetecbd";
```

5. Acesse no navegador:
```
http://localhost/UETEC/
```

---

## 👥 Equipe

| Nome |
|------|
| Guilherme Caetano Lima |
| Gustavo de Souza Carvalho |
| Jeferson Cordeiro dos Santos |
| Pedro Henrique Lopes de Oliveira |

> Orientação: Prof.ª Cintia Batista Pinto da Silva e Prof.ª Carla Fabiane Calixto da Silva Nunes

---

## ⚠️ Observações

- O projeto foi desenvolvido em ambiente local (XAMPP/WampServer) e não está hospedado em servidor externo.
- As credenciais de banco de dados foram removidas do repositório por segurança — configure o `conexao.php` conforme o passo acima.
- Algumas funcionalidades do painel administrativo estavam em desenvolvimento no momento da entrega do TCC.

---

*© 2025 · 3° Informática para a Internet — ETEC de Poá*
