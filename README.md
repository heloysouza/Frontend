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