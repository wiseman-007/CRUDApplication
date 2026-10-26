# Customer CRUD application (Spring Boot + Vaadin)

A simple CRUD web application written in Java, based on the Spring guide
[Creating CRUD UI with Vaadin](https://spring.io/guides/gs/crud-with-vaadin/).
It was made for a university course to practise Java, Git, GitHub and pull requests.

## Features

- List customers in a grid (id, first name, last name, email)
- Filter customers by last name, with a **Clear filter** button
- Add a customer (**Add customer** button)
- Edit a customer by clicking a row, then **Save**
- Delete a customer by clicking a row, then **Delete**
- Notification after saving or deleting
- Counter showing how many customers are currently displayed

## Requirements

- Java 17 or newer
- Internet connection on the first run (Vaadin downloads its frontend dependencies)

## How to run

```bash
./mvnw spring-boot:run        # Windows: mvnw.cmd spring-boot:run
```

Then open http://localhost:8080 in your browser.

If port 8080 is already in use, add `server.port=8081` to
`src/main/resources/application.properties`.

> The app uses an in-memory H2 database, so all data is reset when the application restarts.

## Project structure

| File | Purpose |
|------|---------|
| `Customer.java` | JPA entity (table `customer`) with id, firstName, lastName, email |
| `CustomerRepository.java` | Spring Data repository, includes search by last name |
| `CustomerEditor.java` | Form component with Save, Cancel and Delete buttons |
| `MainView.java` | Main page: title, filter, grid and editor |
| `CrudWithVaadinApplication.java` | Application entry point, loads sample data at startup |

## Screenshots

Screenshots of the running application and the startup logs are in the [`doc`](doc/) folder.

## Authors

- Repository owner: _your GitHub username_
- Contributions via pull requests: _partner's GitHub username_