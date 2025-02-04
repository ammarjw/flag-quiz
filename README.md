# Flag Quiz

This project is a simple quiz application where users guess the country based on a displayed flag. It stores quiz data in a PostgreSQL database and renders dynamic questions on a webpage. The goal of this project was to practice server-side rendering, database integration, and handling form submissions.

![App Screenshot](public/images/flag-quiz.png)

## Features
- Randomly displays flag-based quiz questions.
- Users can submit answers and receive immediate feedback.
- Tracks and displays the total number of correct answers.
- Data storage with PostgreSQL for quiz questions.
- Responsive design for desktop and mobile devices.

## Technologies Used
- **Node.js**: JavaScript runtime for server-side development.
- **Express.js**: Web framework for handling HTTP requests and routing.
- **PostgreSQL**: Relational database for storing quiz data.
- **EJS (Embedded JavaScript Templates)**: For dynamic server-side rendering.
- **Body-parser**: For parsing incoming request bodies.
- **dotenv**: For environment variable management.

## How to Run the Project

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ammarjw/flag-quiz.git
   cd flag-quiz-app
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Create a `.env` file** in the project root with the following configuration:

   ```plaintext
   DB_USER=postgres
   DB_HOST=localhost
   DB_NAME=world
   DB_PASSWORD=your_password_here
   DB_PORT=5432
   PORT=3000
   ```

4. **Run the app:**

   Using Nodemon for auto-reload on code changes:

   ```bash
   nodemon index.js
   ```

   Or simply:

   ```bash
   node index.js
   ```

   ### Quick Tip
   If Nodemon isn't installed:

   ```bash
   npm install -g nodemon
   ```

5. **Open the app:**  
   Visit [http://localhost:3000](http://localhost:3000) in your browser to see the app in action.

## Importing Flags Data

You can import flag data into the PostgreSQL database using a CSV file (e.g., `flags.csv`).

1. **Create the `flags` table:**

   ```sql
   CREATE TABLE flags (
     id SERIAL PRIMARY KEY,
     name VARCHAR(255) NOT NULL,
     flag VARCHAR(255) NOT NULL
   );
   ```

2. **Import the CSV file:**

   - Use pgAdmin or psql to import the `flags.csv` data into the `flags` table.
   - In pgAdmin, right-click on the `flags` table, select **"Import/Export Data"**, and choose the CSV file.

## Notes
- Ensure PostgreSQL is running and the `world` database is properly set up.
- The project focuses on functionality with basic styling. Feel free to improve the UI or add new features.
