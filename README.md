#  Professional Rating API
A REST API for managing professionals and their contacts.



# Description
This API allows you to register, edit, list and delete professionals and their respective contacts. Ideal for CRM systems or team management.



# Technologies Used
- Java 17
- Spring Boot
- PostgreSQL
- Lombok
- JPA / Hibernate



# How to Run the Project Locally
### Prerequisites
- Java 17+
- Maven
- PostgreSQL
- (Optional) Postman or Insomnia to test the API
  
# <br> 

  ### Steps


### 1. Clone the repository:

```bash
git clone https://github.com/youruser/project-name.git
```

### 2. Configure the database in  application.properties:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/assessment
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

### 3. Run the project:

```bash
./mvnw spring-boot:run
```

# <br> 

### Available Endpoints


### Profissionais
- `GET /profissionais` - Lista todos os profissionais
- `GET /profissionais/{id}` - Busca um profissional por ID
- `POST /profissionais` - Cria um novo profissional
- `PUT /profissionais/{id}` - Atualiza um profissional
- `DELETE /profissionais/{id}` - Remove um profissional

### Contatos
- `GET /contatos` - Lista todos os contatos
- `GET /contatos/{id}` - Busca um contato por ID
- `POST /contatos` - Cria um novo contato
- `PUT /contatos/{id}` - Atualiza um contato
- `DELETE /contatos/{id}` - Remove um contato


### Request Example

### POST /profissionais

```json
{
  "id": 1,
  "nome": "Brayan Miguel Favarin",
  "cargo": "Estagiario",
  "nascimento": "2004-11-17",
  "created_date": "2025-04-10"
  "contatos": [
    {
      "nome": "celular",
      "contato": "88 88888-8888"
      "created_date": "2025-04-10",
      "profissional_id": 1
    },
  ]
}
