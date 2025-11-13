 Cookies & Sessions PHP

Aplicação simples desenvolvida em PHP que demonstra o uso de cookies e sessões para armazenar informações e preferências do usuário.
Projeto criado como parte dos estudos de desenvolvimento web e para praticar o gerenciamento de estado no PHP.

 Sobre o Projeto

O CookiesSessionsPHP apresenta exemplos práticos do uso de cookies e sessões no PHP.
Inclui um exemplo de login com sessão ativa e outro de tema personalizado utilizando cookies.
O objetivo é mostrar como o PHP mantém informações entre páginas e como isso pode ser aplicado em sistemas web reais.

🛠️ Tecnologias Utilizadas
Categoria	Ferramenta
Linguagem	PHP
Servidor Local	XAMPP / WAMP / Laragon
Versão Recomendada	PHP 7.4 ou superior
Navegador	Google Chrome / Firefox
Editor de Código	Visual Studio Code / Sublime

 Estrutura do Projeto
```
CookiesSessionsPHP/
│
├── exemplo_login/
│   ├── index.php        
│   ├── validar.php      
│   ├── dashboard.php    
│   └── sair.php         
│
├── exemplo_tema/
│   ├── index.php        
│   ├── set_tema.php    
│   └── style.css       
│
└── README.md
```
 Lógica de Sessão (Login)
<?php
session_start();
$usuario = $_POST['usuario'];
$senha = $_POST['senha'];

if ($usuario === "admin" && $senha === "1234") {
    $_SESSION['usuario'] = $usuario;
    header("Location: dashboard.php");
} else {
    echo "Usuário ou senha inválidos!";
}
?>

 Lógica de Cookie (Tema)
<?php
$tema = $_GET['tema'] ?? 'claro';
setcookie('tema', $tema, time() + (86400 * 30)); // expira em 30 dias
header("Location: index.php");
?>

 Funcionalidades Implementadas

 Login simples com validação de credenciais
 Manutenção da sessão ativa entre páginas
 Logout que destrói a sessão e redireciona o usuário
 Escolha de tema (claro ou escuro) salva em cookie
 Organização de código em pastas separadas por exemplo

 Possíveis Melhorias

Integrar autenticação com banco de dados MySQL

Adicionar mensagens de erro e sucesso estilizadas

Aplicar proteção contra XSS e CSRF

Criar um sistema de cadastro de usuários

Adicionar lembrar-me com cookies criptografados

 Autor

Nome: Laerte Ferraz da Silva Júnior
Instituição: Curso Técnico em Informática – Escola Ulbra São Lucas
Disciplina: Desenvolvimento Web II – PHP
Professor: Jeferson Leon

 Licença

Projeto desenvolvido para fins educacionais.
Livre para uso, modificação e estudo, desde que mantidos os créditos ao autor.

“Aprender PHP é entender como o servidor conversa com o navegador. Bora codar e testar!” 🧠💻
