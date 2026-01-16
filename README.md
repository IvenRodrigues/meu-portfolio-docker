# 🐳 Meu Primeiro Full Stack com Docker

E aí! 👋
Esse é um projeto prático que desenvolvi para entender como o **Docker** funciona na vida real.
A ideia foi criar um ambiente completo (Site + Banco de Dados + Gerenciador) rodando 100% em containers, sem precisar instalar nada direto na minha máquina.

## 🛠️ O que eu usei
* **Docker Compose:** Para subir tudo com um comando só.
* **Nginx:** Para colocar meu site HTML no ar.
* **PostgreSQL:** O banco de dados para guardar as informações.
* **Adminer:** Uma interface visual para eu ver o banco de dados sem usar linha de comando.

## ⚙️ Como funciona a estrutura
Eu configurei 3 serviços que conversam entre si:
1.  **Site (Porta 8000):** Onde fica a página web.
2.  **Painel do Banco (Porta 8080):** Onde eu logo no Adminer.
3.  **Banco de Dados (Interno):** Fica protegido e não aparece para fora, só o Adminer consegue acessar ele.

## 🚀 Como rodar o projeto
Se você quiser testar na sua máquina:

1.  Clone o repositório.
2.  Crie um arquivo `.env` na pasta raiz (olhe o `.env.example`) com as senhas.
3.  Rode o comando mágico:
    ```bash
    docker compose up -d
    ```
4.  Acesse `http://localhost:8000` para ver o site!

## 🧠 O que eu aprendi
Foi muito massa fazer esse projeto porque aprendi a:
* Usar **Volumes** para não perder os dados do banco quando desligo o container.
* Configurar **Redes (Networks)** para o Adminer achar o Postgres pelo nome.
* Proteger minhas senhas usando variáveis de ambiente (`.env`).
* Resolver conflitos de portas (tive que mudar a porta do Adminer uma hora!).

---
Feito com 💻 e ☕ por ** Iven Rodrigues **
