# Store-and-retrieve-data-in-PostgreSQL
Store and retrieve data in PostgreSQL
Learning Path API
A simple Express.js REST API connected to a PostgreSQL database for managing users.

Setup Instructions
Follow these steps to set up and run the project:

1. Prerequisites
PostgreSQL installed and running

Node.js and npm installed

2. Create the Database
Open your terminal and create a new PostgreSQL database:

bash
Copy
Edit
createdb learning_path_db
3. Create the users Table
Run the SQL script to create the table:

bash
Copy
Edit
psql -d learning_path_db -f sql/create_users_table.sql
4. Configure Database Connection
Open config/db.js and update the password field to match your PostgreSQL password:

js
Copy
Edit
const pool = new Pool({
  user: 'postgres',
  host: 'localhost',
  database: 'learning_path_db',
  password: 'yourpassword', // <-- replace with your actual password
  port: 5432,
});
5. Install Project Dependencies
In the project root folder, run:

bash
Copy
Edit
npm install
6. Start the Server
Run the following command:

bash
Copy
Edit
npm start
You should see:

pgsql
Copy
Edit
Server is running on port 3000
API Endpoints
Method	Endpoint	Description
GET	/users	Get all users
GET	/users/:id	Get a user by ID
POST	/users	Create a new user
PUT	/users/:id	Update a user by ID
DELETE	/users/:id	Delete a user by ID

Testing the API
Use Postman or Insomnia to test the endpoints.
Make sure your server is running at http://localhost:3000.

