# project_django_Todo_list


# Documentação do Projeto TODO_List

Este é um projeto de lista de tarefas feito em Django. O projeto permite que os usuários criem, atualizem e excluam tarefas, bem como visualizem uma lista de todas as tarefas.

## Instalação

Para instalar o projeto, siga as instruções abaixo:

1. Clone o repositório do projeto:

   ```
   git clone https://github.com/r1cardoPereira/project_django_Todo_list.git
   ```

2. Crie um ambiente virtual para o projeto:

   ```
   python -m venv venv
   ```

3. Ative o ambiente virtual:

   ```
   source venv/bin/activate
   ```

4. Instale as dependências do projeto:

   ```
   pip install -r requirements.txt
   ```

5. Execute as migrações do banco de dados:

   ```
   python manage.py migrate
   ```
6. Crie um super usuário:

   ```
   python manage.py createsuperuser
   ```   

7. Inicie o servidor de desenvolvimento:

   ```
   python manage.py runserver
   ```

8. Acesse o projeto em seu navegador em `http://localhost:8000/`.

## Uso

Para usar o projeto, siga as instruções abaixo:

1. Acesse o projeto em seu navegador em `http://localhost:8000/`.

2. Crie uma nova tarefa clicando no botão "Crie uma Tarefa" na página inicial.

3. Preencha o formulário de criação de tarefas e clique em "Salvar" para criar a tarefa.

4. Visualize a lista de tarefas clicando no botão "Veja suas Tarefas" na página inicial.

5. Atualize uma tarefa clicando no botão "Editar" ao lado da tarefa desejada na lista de tarefas.

6. Exclua uma tarefa clicando no botão "Excluir" ao lado da tarefa desejada na lista de tarefas.

7. Marque uma tarefa como concluída clicando no botão "Concluir" ao lado da tarefa desejada na lista de tarefas.

## Rotas
```
O projeto define as seguintes rotas:

- A rota "" (vazia) é mapeada para a view "home".
- A rota "all/" é mapeada para a view "TodoListView".
- A rota "create" é mapeada para a view "TodoCreateView".
- A rota "update/<int:pk>" é mapeada para a view "TodoUpdateView", onde "<int:pk>" é um parâmetro que representa o ID da tarefa a ser atualizada.
- A rota "delete/<int:pk>" é mapeada para a view "TodoDeleteView", onde "<int:pk>" é um parâmetro que representa o ID da tarefa a ser excluída.
- A rota "finish/<int:pk>" é mapeada para a view "TodoFinishView", onde "<int:pk>" é um parâmetro que representa o ID da tarefa a ser marcada como concluída.

```


## Funcionalidades

O projeto permite que os usuários realizem as seguintes funcionalidades:

- Criar uma nova tarefa, informando o título e a data limite para a conclusão.
- Visualizar a lista de tarefas, ordenadas pela data limite.
- Atualizar uma tarefa existente, alterando o título ou a data limite.
- Excluir uma tarefa existente.
- Concluir uma tarefa existente, marcando-a como concluída.

## Administração

O projeto também inclui uma área de administração, acessível pela rota "admin/". Na área de administração, é possível gerenciar os usuários e as tarefas do sistema.