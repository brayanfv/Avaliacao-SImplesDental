#  Professional Rating API
A REST API for managing professionals and their contacts.



## Description
This API is designed for managing professionals and their contacts, making it a great foundation for CRM platforms, HR systems, or internal team directories.This API allows you to register, edit, list and delete professionals and their respective contacts. Ideal for CRM systems or team management.



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


### Professionals
- `GET /profissionais` - Lists all professionals
- `GET /profissionais/{id}` - Searches for a professional by ID
- `POST /profissionais` - Creates a new professional
- `PUT /profissionais/{id}` - Updates a professional
- `DELETE /profissionais/{id}` - Removes a professional

### Contacts
- `GET /contatos` - Lists all contacts
- `GET /contatos/{id}` - Searches for a contact by ID
- `POST /contatos` - Creates a new contact
- `PUT /contatos/{id}` - Updates a contact
- `DELETE /contatos/{id}` - Removes a contact


### Request Example

### POST /profissionais

```json
{
  "id": 1,
  "nome": "Brayan Miguel Favarin",
  "cargo": "Estagiario",
  "nascimento": "2004-11-17",
  "created_date": "2025-04-10",
  "contatos": [
    {
      "nome": "celular",
      "contato": "88 88888-8888",
      "created_date": "2025-04-10",
      "profissional_id": 1
    },
  ]
}
