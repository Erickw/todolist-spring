
# TODO List com Spring Boot

Este é um projeto simples de gerenciamento de tarefas (TODO List) desenvolvido com Spring Boot. Ele implementa uma API REST para criar, listar e excluir tarefas, utilizando o banco de dados H2 para persistência.

## Funcionalidades

- Adicionar novas tarefas.
- Listar todas as tarefas.
- Excluir tarefas pelo ID.
- Persistência de dados com H2 Database.
- API REST seguindo boas práticas.

## Pré-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

- **Java JDK 11 ou superior**: [Instalar Java](https://www.oracle.com/java/technologies/javase-downloads.html)
- **Spring Boot CLI Versão inferior a 3.0**: [Instalar Spring Boot CLI](https://spring.io/tools)

## Como executar

### Usando o Spring Boot CLI

1. Clone o repositório:
   ```bash
   git clone https://github.com/Erickw/todo_list_spring_boot.git
   ```

2. Navegue até o diretório do projeto:
   ```bash
   cd todo_list_spring_boot
   ```

3. Execute o projeto:
   ```bash
   mvn spring-boot:run
   ```

### Usando um IDE (Eclipse, IntelliJ, VS Code)

1. Importe o projeto como um projeto Maven/Gradle na sua IDE.
2. Compile e execute o arquivo principal: `TodoListApp.groovy` ou `Main` se estiver configurado como classe principal.

---

## Endpoints da API

### Listar todas as tarefas
**GET** `/tasks`

#### Exemplo de resposta:
```json
[
  {
    "id": 1,
    "title": "Comprar pão",
    "description": "Ir à padaria às 8h",
    "completed": false
  }
]
```

---

### Adicionar uma nova tarefa
**POST** `/tasks`

#### Corpo da requisição:
```json
{
  "title": "Estudar Spring Boot",
  "description": "Estudar durante 2 horas",
  "completed": false
}
```

#### Exemplo de resposta:
```json
{
  "id": 2,
  "title": "Estudar Spring Boot",
  "description": "Estudar durante 2 horas",
  "completed": false
}
```

---

### Excluir uma tarefa
**DELETE** `/tasks/{id}`

#### Exemplo:
```bash
DELETE /tasks/1
```

---

## Tecnologias Utilizadas

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.
- **H2 Database**: Banco de dados em memória.
- **Spring Boot CLI**: Para execução rápida de projetos.
- **Maven**: Para gerenciar as dependências.

---