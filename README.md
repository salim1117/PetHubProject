# 🐾 PetHub — Pet E-Commerce & Care Platform

A full-stack Java web application for buying pets, pet products, booking vet appointments, and managing pet care — built with Java Servlets, JSP, and MySQL.

## Features

- 🐶 **Buy Pets** — Browse and purchase dogs, cats, birds, and fish
- 🛒 **Shop Products** — Pet food, grooming, accessories, and treats
- 📅 **Book Appointments** — Schedule vet consultations
- 🛍️ **Cart & Wishlist** — Add products to cart or save for later
- 📦 **Order Management** — Place, track, and cancel orders
- 👤 **User Authentication** — Register, login, profile update, password reset
- 🔐 **Admin Panel** — Manage products, orders, and users
- 💬 **Chatbot** — AI-powered pet care assistant (OpenAI GPT)
- ⭐ **Reviews** — Product ratings and reviews
- 📞 **Contact Us** — Submit inquiries

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Java Servlets (Jakarta EE) |
| Frontend | JSP, HTML, CSS, JavaScript |
| Database | MySQL |
| Server | Apache Tomcat |
| Connector | MySQL Connector/J 8.0.33 |

## Project Structure

```
PetHubProject/
├── src/main/java/com/MVC/
│   ├── Controller/        # Servlets (request handling)
│   └── Model/             # Business logic & DB access
└── src/main/webapp/
    ├── *.jsp              # View pages
    ├── WEB-INF/
    │   ├── web.xml
    │   └── lib/           # JAR dependencies
    └── Images/            # Static assets
```

## Setup & Installation

### Prerequisites
- Java 11+
- Apache Tomcat 10+
- MySQL 8+
- IDE: Eclipse / IntelliJ

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/PetHubProject.git
cd PetHubProject
```

### 2. Import the database
```bash
mysql -u root -p < pethub.sql
```

### 3. Configure environment variables

Set the following environment variables before starting Tomcat:

| Variable | Description | Default |
|----------|-------------|---------|
| `DB_URL` | JDBC connection URL | `jdbc:mysql://localhost:3306/PetHub` |
| `DB_USER` | MySQL username | `root` |
| `DB_PASS` | MySQL password | *(empty)* |

**Linux/macOS:**
```bash
export DB_URL=jdbc:mysql://localhost:3306/PetHub
export DB_USER=root
export DB_PASS=yourpassword
```

**Windows:**
```cmd
set DB_URL=jdbc:mysql://localhost:3306/PetHub
set DB_USER=root
set DB_PASS=yourpassword
```

### 4. Chatbot (Optional)
To enable the AI chatbot, set your OpenAI API key in [ChatbotServlet.java](src/main/java/com/MVC/Controller/ChatbotServlet.java):
```java
private static final String API_KEY = System.getenv("OPENAI_API_KEY");
```
Then:
```bash
export OPENAI_API_KEY=sk-...
```

### 5. Deploy
Import the project into Eclipse as a Dynamic Web Project and deploy to Tomcat, or build a `.war` and drop it into Tomcat's `webapps/` folder.

## Default Admin Credentials
After importing the SQL, the admin account is the first user (`id=1`). Update credentials directly in the database.

## Screenshots
> Add screenshots of Home, Product, Cart, and Admin pages here.

## License
This project is for educational purposes.
