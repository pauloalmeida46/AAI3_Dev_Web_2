<h1>AAI3 de Lista de Tarefas</h1>

<p>Os alunos devem desenvolver uma API usando Express.js para gerenciar uma lista de tarefas. A API deve permitir adicionar, visualizar, atualizar e remover tarefas, além de garantir que não sejam criadas tarefas com o mesmo nome.<p>

# Requisitos
 <p>- Node.js v12 ou superior</p>
 <p>- NPM (gerenciador de pacotes do Node.js) ou yarn</p>
 <p>- GIT (Versôes Atuais)

# 1º Passo: Instalação

<details>
   <summary><b>Clique aqui</b></summary>

 1. Crie uma pasta em sua área de trabalho e abra o terminal do seu sistema operacional. Em seguida vá até a pasta que você criou usando comandos como "cd caminho/até/a/pasta" e "ls" para se localizar mmelhor. Logo em seguida digite:
  
  ```
  git clone https://github.com/pauloalmeida46/AAI3_Dev_Web_2.git .
  ``` 

 2. Com o VSCODE aberto, clique em `File` e depois em `Open Folder`  e selecione a pasta que você criou para rodar a aplicação

 3. Vá na barra `terminal`, em seguida aperte em `new terminal` e digite o código de instalação da dependência necessária: 
  ```
  npm install
  ```

  > _Obs.: Caso esteja usando o yarn, utilize o seguinte comando `yarn install
`_

</details>
<br>

# 2º Passo: Execução da API

<details>
   <summary><b>Clique aqui</b></summary>

 1. Após ter feito o Passo 1, inicie a aplicação no terminal com:
  ```
  node index.js
  ```
  > _Obs.: Ou use `yarn start` caso esteja usando o yarn_

 2. A API estará rodando na porta 3000. Você pode acessá-la em http://localhost:3000

</details>
<br>

# Rotas Disponíveis

<details>
   <summary><b>Clique aqui</b></summary>

## 1. Ver todas as tarefas
   - Rota: GET /tarefas
   - Descrição: Retorna todas as tarefas registradas.
   - Exemplo de Saída:
    
    [
     {
        "id": 1,
        "nome": "Ir para a Fatec",
        "status": false
    },
    {
        "id": 2,
        "nome": "Fazer a tarefa do Cláudio",
        "status": true
     }
    ]
   

## 2. Adicionar uma nova tarefa
   - Rota: POST /tarefas
   - Descrição: Adiciona uma nova tarefa. O status é false por padrão (não concluído).
   - Corpo da Requisição:
   ```
   {
     "nome": "Nome da tarefa"
   }
   ```
   - Exemplo de Resposta:
   ```
   {
    "id": 3,
    "nome": "Nome da tarefa",
    "status": false
   }
   ```

## 3. Atualizar uma tarefa existente
   - Rota: PUT /tarefas/:id
   - Descrição: Atualiza uma tarefa existente utilizando o id como base, mudando o nome e o status da tarefa.
   - Corpo da Requisição:
   ```
   {
    "nome": "Novo nome da tarefa",
    "status": true
   }
   ```
   - Exemplo de Resposta:
   ```
   {
    "id": 1,
    "nome": "Novo nome da tarefa",
    "status": true
   }
   ```

## 4. Excluir uma tarefa
   - Rota: DELETE /tarefas/:id
   - Descrição: Remove uma tarefa da lista com base no id.
   - Exemplo de Resposta:
   ```
   {
    "message": "Tarefa removida com sucesso."
   }
   ```

## 5. Filtrar tarefas por status
   - Rota: GET /tarefas?status=true ou GET /tarefas?status=false
   - Descrição: Filtra as tarefas de acordo com o status (Verdadeiro ou Falso).
   - Exemplo de Resposta:
   ```
   [
    {
     "id": 2,
     "nome": "Fazer compras",
     "status": true
    }
   ]
   ```
</details>
<br>
