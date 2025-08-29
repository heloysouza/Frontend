# 📌 Sistema de Autenticação (Login, Cadastro e Dashboard)

Este projeto é um sistema simples de **autenticação de usuários** em **HTML, CSS e JavaScript**, integrado a uma API hospedada no **Render**. Ele permite que o usuário faça **cadastro**, **login** e acesse uma **área restrita (Dashboard)**.

---

## 🚀 Funcionalidades

- **Cadastro de Usuário**  
  - Nome completo, usuário e senha.  
  - Envio de dados para a API:  
    ```
    POST https://cadastro-usuario-ft46.onrender.com/api/cadastro
    ```
- **Login de Usuário**  
  - Autenticação com usuário e senha.  
  - Se válido, gera um **token JWT** armazenado no `localStorage`.  
  - API de login:  
    ```
    POST https://cadastro-usuario-ft46.onrender.com/api/login
    ```
- **Dashboard (Área Restrita)**  
  - Apenas acessível com **token válido**.  
  - API protegida:  
    ```
    GET https://cadastro-usuario-ft46.onrender.com/api/dashboard
    ```
  - Se o token for inválido ou expirado, o usuário é redirecionado para login.

---

## 🖥️ Estrutura dos Arquivos

📂 projeto-autenticacao ├── index.html        # Página de Login ├── cadastro.html     # Página de Cadastro ├── dashboard.html    # Área restrita (Dashboard) └── README.md         # Documentação do projeto

---

## 🎨 Telas do Sistema

### 🔑 Login (`index.html`)
- Campos: Usuário e Senha  
- Envia dados via **fetch API** para autenticação  
- Armazena o **token JWT** no navegador  
- Redireciona para `dashboard.html` após login  

---

### 📝 Cadastro (`cadastro.html`)
- Campos: Nome Completo, Usuário e Senha  
- Envia dados para criar uma nova conta  
- Exibe mensagem de sucesso ou erro  

---

### 📊 Dashboard (`dashboard.html`)
- Verifica se existe **token no localStorage**  
- Caso não tenha, mostra aviso: *"Você não está logado!"*  
- Caso o token seja inválido/expirado → pede novo login  
- Caso seja válido → exibe mensagem da API e botão **Sair**  

---

## ⚙️ Como Rodar o Projeto Localmente

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/projeto-autenticacao.git

2. Abra os arquivos .html no navegador (não precisa de servidor local).


3. Para funcionamento correto, é necessário que a API esteja online em:

https://cadastro-usuario-ft46.onrender.com




---

🛠️ Tecnologias Utilizadas

HTML5 → Estrutura das páginas

CSS3 → Estilização com gradientes e responsividade

JavaScript (ES6) → Requisições com fetch, manipulação do DOM e localStorage

API REST (Node.js no Render) → Gerenciamento de login, cadastro e autenticação JWT



---

🔐 Fluxo de Autenticação

1. Usuário faz cadastro → cria conta na API.


2. Usuário faz login → recebe token JWT.


3. Token é salvo no localStorage.


4. Ao acessar a dashboard, o token é enviado no header da requisição:

Authorization: Bearer <seu_token>


5. API valida → se válido, retorna mensagem de sucesso.


6. Usuário pode sair (logout) → token removido do localStorage.




---

📌 Melhorias Futuras

Implementar validação de senha forte no cadastro.

Adicionar feedback visual mais amigável (ex: alertas customizados).

Criar sistema de recuperação de senha.

Melhorar o design responsivo para mobile.