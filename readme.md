# Repositório da Imersão DevOps - Alura Google Cloud

>*Esse README foi originalmente redigido pela equipe Alura em sua aula de imersão. Pequenas alterações foram feitas por mim durante as aulas. Você vai encontrar alguns arquivos docker na minha versão.*

Este projeto é uma API desenvolvida com FastAPI para gerenciar alunos, cursos e matrículas em uma instituição de ensino.

👇Para saber o conteúdo da imersão e como começar:
<details>
   
## Pré-requisitos

- [Python 3.10 ou superior instalado](https://www.python.org/downloads/)
- [Git](https://git-scm.com/downloads)
- [Docker](https://www.docker.com/get-started/)

## Passos para subir o projeto

1. **Faça o download do repositório:**
   [Clique aqui para realizar o download](https://github.com/guilhermeonrails/imersao-devops/archive/refs/heads/main.zip)

2. **Crie um ambiente virtual:**
   ```sh
   python3 -m venv ./venv
   ```

3. **Ative o ambiente virtual:**
   - No Linux/Mac:
     ```sh
     source venv/bin/activate
     ```
   - No Windows:
     ```sh
     venv\Scripts\activate
     ```

4. **Instale as dependências:**
   ```sh
   pip install -r requirements.txt
   ```

5. **Execute a aplicação:**
   ```sh
   uvicorn app:app --reload
   ```

6. **Acesse a documentação interativa:**

   Abra o navegador e acesse:  
   [http://127.0.0.1:8000/docs](http://0.0.0.0:8000/docs)
   >*Talvez você aqui precise usar [http://localhost:8000/docs](http://localhost:8000/docs) caso não abra pelo link acima no seu ambiente*

   Aqui você pode testar todos os endpoints da API de forma interativa.

---

## Estrutura do Projeto

- `app.py`: Arquivo principal da aplicação FastAPI.
- `models.py`: Modelos do banco de dados (SQLAlchemy).
- `schemas.py`: Schemas de validação (Pydantic).
- `database.py`: Configuração do banco de dados SQLite.
- `routers/`: Diretório com os arquivos de rotas (alunos, cursos, matrículas).
- `requirements.txt`: Lista de dependências do projeto.

---

- O banco de dados SQLite será criado automaticamente como `escola.db` na primeira execução.
- Para reiniciar o banco, basta apagar o arquivo `escola.db` (isso apagará todos os dados).

</details>

## 🧠 Conhecimento Adquiridos na Imersão DevOps - Alura Google Cloud:

- Utilizei uma API construida com FastAPI.
- Primeiro contato Docker, uso do Docker Hub e seus comandos essenciais (`docker build`, `docker run`, entre outros).
- Gerei um Dockerfile com auxilio do **Gemini integrada ao VSCode**.
- Aprendi sobre os benefícios do Docker para ambientes isolados, escaláveis e reproduzíveis (chega do *"Mas na minha máquina roda"*).
- Criação de um workflow no GitHub Actions para a etapa de `docker-image`. A action automatiza o build da imagem Docker diretamente no repositório.
- Conheci também o `.dockerignore` e implementei para otimizar o processo de build (ignorando cache, por exemplo).
- Um papo sobre CI/CD e boas práticas na automação de ambientes.
- Introdução ao **YAML** e criando o arquivo `docker-compose.yml` (Utilizando o Gemini para gerar a estrutura com mapeamento de volumes e portas).
- Dentro do `docker-compose.yml` ainda instrui o comando `uvicorn` com `--reload` no ambiente de desenvolvimento para acelerar o fluxo de testes e ajustes.
- Explorei o **Google Cloud Platform** e seus recursos.
- Usei o *Artifact Registry** para armazenar a imagem Docker.
- E fiz Deploy da API via **Cloud Run**, tornando-a **serverless**.
- O Cloud Run cuidou do resto. Forneci o container Docker e ele lidou com provisionamento, escalabilidade, segurança e disponibilidade.
