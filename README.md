## GET /tarefas

Este endpoint é utilizado para listar todas as tarefas existentes no sistema. Ao fazer uma solicitação GET para `/tarefas`, o cliente receberá uma resposta em formato JSON contendo um array de objetos, cada um representando uma tarefa.

### Resposta

A resposta bem-sucedida terá um status HTTP 200 e o corpo da resposta conterá um array de objetos com as seguintes propriedades:

- **id**: O identificador único da tarefa.
    
- **nome**: O nome da tarefa.
    
- **dataEntrega**: A data de entrega da tarefa.
    
- **responsavel**: O responsável pela tarefa.
    

Exemplo de resposta:

``` json
[
    {
        "id": 0,
        "nome": "",
        "dataEntrega": "",
        "responsavel": ""
    }
]

 ```


## POST /tarefas

Este endpoint é utilizado para a criação de uma nova tarefa. O corpo da requisição deve ser enviado no formato JSON e deve incluir os seguintes parâmetros:

- **nome** (string): O nome da tarefa a ser criada.
    
- **responsavel** (string): O nome do responsável pela tarefa.
    
- **dataEntrega** (string): A data de entrega da tarefa no formato DD/MM/AAAA.
    

### Exemplo de Requisição

``` json
{
  "nome": "Realizar provas acadêmicas",
  "responsavel": "Carlos",
  "dataEntrega": "10/09/2025"
}

 ```

### Resposta

Uma vez que a tarefa é criada com sucesso, a resposta terá um status HTTP 200 e retornará um JSON contendo os seguintes campos:

- **id** (integer): O identificador único da tarefa criada.
    
- **nome** (string): O nome da tarefa.
    
- **responsavel** (string): O nome do responsável pela tarefa.
    
- **dataEntrega** (string): A data de entrega da tarefa.
    

### Exemplo de Resposta

``` json
{
  "id": 0,
  "nome": "",
  "responsavel": "",
  "dataEntrega": ""
}

 ```

Este endpoint é essencial para gerenciar as tarefas dentro do sistema, permitindo que os usuários criem novas entradas de forma eficiente.


## PUT /tarefas/{id}

Este endpoint é utilizado para atualizar uma tarefa existente com o ID especificado na URL. O corpo da requisição deve conter os dados da tarefa que você deseja modificar.

#### Parâmetros da Requisição

- **nome** (string): O nome da tarefa a ser atualizada.
    
- **responsavel** (string): O responsável pela tarefa.
    
- **dataEntrega** (string): A data de entrega da tarefa, no formato DD/MM/AAAA.
    

#### Exemplo de Corpo da Requisição

``` json
{
  "nome": "Meditar",
  "responsavel": "Gabriel - 4711797",
  "dataEntrega": "15/09/2025"
}

 ```

#### Resposta

Após a execução bem-sucedida da requisição, o servidor retornará um status HTTP 200 e um corpo de resposta em formato JSON, que inclui os campos da tarefa atualizada.

``` json
{
  "id": 0,
  "nome": "",
  "dataEntrega": "",
  "responsavel": ""
}

 ```

### Observações

- O ID da tarefa deve ser fornecido na URL.
    
- Certifique-se de que os dados enviados no corpo da requisição estejam corretos para que a atualização ocorra conforme esperado.


## DELETE /tarefas/id

Este endpoint é responsável por remover uma tarefa específica do sistema. O parâmetro `id` refere-se ao identificador único da tarefa que será excluída.

## Parâmetros

- `id` (string): O identificador único da tarefa que você deseja excluir.
    

## Resposta

- **Status**: 200
    
- **Content-Type**: text/xml
    

A resposta indica que a operação de exclusão foi realizada com sucesso.
