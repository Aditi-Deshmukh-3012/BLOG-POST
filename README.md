# 📝 Blog Post CRUD Application

A simple blog post platform where users can create, view, edit, and delete posts. Built with **Node.js**, **Express.js**, **MySQL**, **EJS**, and **CSS**. The application follows RESTful architecture and uses server-side rendering.



## 🚀 Features

- Create a new blog post with a username and content
- View all blog posts (newest first)
- View post details on a separate page
- Edit an existing post
- Delete a post
- Responsive and clean UI using custom CSS
- Server-side sorting using `created_at` timestamps



## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Frontend**: EJS (Embedded JavaScript Templates), HTML, CSS
- **Database**: MySQL
- **Templating**: EJS
- **Routing**: RESTful routes with method-override for PUT and DELETE



## 📁 Project Structure

project/
│
├── views/ # EJS templates (home, new, edit, view)
├── public/ # Static CSS files
├── app.js # Main Express app
├── db.js # MySQL DB connection
├── package.json # Dependencies
└── README.md # Project overview


## 📦 Installation

1. **Clone the repository**
   git clone https://github.com/your-username/blog-post-crud-app.git
   cd blog-post-crud-app


Install dependencies:

npm install

Setup MySQL Database

Create a database and table with the following schema:

CREATE TABLE posts (
    id VARCHAR(255) PRIMARY KEY,
    username VARCHAR(255),
    content TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

Configure DB in db.js:

const connection = mysql.createConnection({
    host: "localhost",
    user: "your_username",
    password: "your_password",
    database: "your_database"
});

Run the app:

node app.js

Navigate to http://localhost:3000/posts

🔒 Security

Input is escaped to prevent SQL Injection (using prepared statements).

ScreenShots:

Home Page:

<img width="1913" height="877" alt="Screenshot 2025-07-23 235426" src="https://github.com/user-attachments/assets/9a6dc0bf-0b6c-478a-a56b-a4f7a0094922" />


Creating new post:

<img width="1918" height="533" alt="Screenshot 2025-07-23 235441" src="https://github.com/user-attachments/assets/fb33f0e9-c007-412b-92ad-37c5b913597e" />


Edit Post:

<img width="1915" height="365" alt="Screenshot 2025-07-23 235501" src="https://github.com/user-attachments/assets/c11adffb-2076-4bbf-ade5-0b38499d40be" />


View Post:

<img width="1919" height="444" alt="Screenshot 2025-07-23 235511" src="https://github.com/user-attachments/assets/0bd65709-3559-4722-91da-3db3c9e67701" />




