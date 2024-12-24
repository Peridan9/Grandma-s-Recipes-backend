# 🍲 Grandma's Recipes - Backend 🍴

This repository contains the **backend** implementation for the "Grandma's Recipes" project, developed as part of the **Web Development Environments** course at Ben-Gurion University. The backend provides a robust API for recipe and user management, connecting to both an external API and a MySQL database.

---

## ✨ Features

- **User Management:**
  - Registration and authentication using JWT.
  - Storage of user details, favorite recipes, and personal recipes.

- **Recipe Management:**
  - Retrieve family and personal recipes from the database.
  - Integrate with an external recipe API for general recipes.
  - Random, detailed, and filtered recipe searches.

- **Database Integration:**
  - MySQL database for persistent storage of users, recipes, and interactions.

- **External API Integration:**
  - Use Spoonacular API for recipe search and information.
  - Fetch general recipes and store static data for testing.

---

## 📚 API Endpoints

### User Endpoints
- `POST /register` - Register a new user.
- `POST /login` - User login and JWT token generation.
- `GET /users/:id` - Fetch user details.

### Recipe Endpoints
- `GET /recipes/random` - Get random recipes from the external API.
- `GET /recipes/:id` - Fetch detailed recipe information.
- `POST /recipes/favorites` - Add a recipe to favorites.
- `GET /recipes/favorites` - Retrieve user’s favorite recipes.
- `POST /recipes/family` - Add a new family recipe.
- `GET /recipes/family` - Retrieve all family recipes.

---

## 🛠️ Technologies Used

- **Node.js**: JavaScript runtime for building scalable server-side applications.
- **Express.js**: Web framework for managing routes and middleware.
- **MySQL**: Relational database for storing users and recipes.
- **Spoonacular API**: External API for fetching general recipe data.

---

## 📂 File Structure

```
Grandma-s-Recipes-backend/
├── .github/
│   └── workflows/
│       └── node.js.yml
├── dist/
│   ├── index.html
│   └── main.js
├── routes/
│   ├── recipe.js
│   └── user.js
├── sql scripts/
│   ├── create_tables.sql
│   └── insert_data.sql
├── .gitignore
├── README.md
├── fullchain.pem
├── index.html
├── main.js
├── package-lock.json
├── package.json
└── privkey.pem
```

---

## 🖍️ Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Peridan9/Grandma-s-Recipes-backend.git
   cd Grandma-s-Recipes-backend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure the database:**
   - Install MySQL and create a database.
   - Execute the SQL scripts located in the `sql scripts/` directory to set up the necessary tables and initial data.
   - Update database credentials in the appropriate configuration file (e.g., `main.js` or a dedicated config file).

4. **Start the server:**
   ```bash
   npm start
   ```

5. **Access the API at:**
   ```
   https://localhost:3000
   ```

---

## 🌟 External API Integration

This project integrates with the [Spoonacular API](https://spoonacular.com/food-api/docs) for recipe-related operations:
- **Endpoints Used:**
  - `Search Recipes`
  - `Get Recipe Information`
  - `Get Random Recipes`
- **Daily Query Limit:** To avoid exceeding the limit, static data is stored for development purposes.
