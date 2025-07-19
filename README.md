My Blog System 🚀
Project Description
This is a mini-project built using React and Tailwind CSS, featuring user authentication (login, registration) and user-based blog post management. The application simulates a backend using localStorage for data persistence.

Features ✨

  User Authentication: Register new accounts, log in, and log out. 🔐
  
  User-Specific Content: Logged-in users can create, view, edit, and delete their own blog posts. ✍️
  
  Public Blog List: View all published blog posts. 📚
  
  Single Post View: Read the full content of individual blog posts. 📖
  
  Responsive Design: Styled with Tailwind CSS for a modern and adaptive user interface. 📱💻
  
  Local Storage Backend: Data (users and posts) is persisted in the browser's localStorage. 💾

Setup Instructions 🛠️
To get this project up and running on your local machine, follow these steps:

Clone the repository:

    git clone https://github.com/Hikma2003/Blog-system.git
    cd Blog-system

Install dependencies:

    npm install

Install Tailwind CSS and its peer dependencies (v3):

    npm install -D tailwindcss@^3.0.0 postcss autoprefixer

Generate Tailwind CSS config files:

    npx tailwindcss init -p

Ensure tailwind.config.js is configured:
Verify that your tailwind.config.js content array includes "./index.html" and "./src/**/*.{js,jsx,ts,tsx}".
      
      // tailwind.config.js
      /** @type {import('tailwindcss').Config} */
      export default {
        content: [
          "./index.html",
          "./src/**/*.{js,jsx,ts,tsx}",
        ],
        theme: {
          extend: {},
        },
        plugins: [],
      }

Create src/dist directory:

    mkdir src/dist

(If you are on Windows and mkdir doesn't work, use md src\dist or create it manually through your file explorer.)

Add Tailwind directives to src/index.css:
Ensure src/index.css contains:

    /* src/index.css */
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

Update package.json scripts:
Add/verify the following scripts in your package.json:
      
      "build:css": "tailwindcss -i ./src/index.css -o ./src/dist/tailwind.css --minify",
      "watch:css": "tailwindcss -i ./src/index.css -o ./src/dist/tailwind.css --watch"

Update src/main.jsx import:
Ensure src/main.jsx imports the compiled CSS:

    // src/main.jsx
    import './dist/tailwind.css';

Run the application:
Open two separate terminal windows in the project root:

In the first terminal, start the Tailwind CSS watcher:

    npm run watch:css

In the second terminal, start the React development server:

    npm run dev

Your application will be available at http://localhost:5173/ (or a similar address).

Screenshots / Demo (Optional) 📸

<img width="2560" height="1600" alt="Screenshot (19)" src="https://github.com/user-attachments/assets/7e24d888-5169-41c6-bfd8-ba90fb68fd9f" />


