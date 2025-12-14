# ATMT Chatbot - Laravel MVC Application

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![MVC Pattern](https://img.shields.io/badge/Architecture-MVC-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## 📋 About The Project

This repository contains the source code for a **Chatbot Application** developed during a **1-month internship at ATMT**.

The project is built using the **Laravel** PHP framework, following the **Model-View-Controller (MVC)** architectural pattern. It is designed to automate customer interactions, answer frequently asked questions, and provide support services relevant to ATMT's business operations (e.g., query handling, user assistance).

### 🎯 Objective
The primary goal of this project was to create an interactive conversational interface that enhances user engagement and reduces manual support workload by providing instant responses to common queries.

---

## 🚀 Features

* **Interactive Chat Interface**: A user-friendly, real-time chat widget for users to send queries.
* **MVC Architecture**: Clean separation of logic (Controllers), data (Models), and presentation (Views).
* **Admin Dashboard**: (Optional - *Enable if applicable*) A backend panel to view chat logs and manage bot responses.
* **Keyword/Logic Matching**: Processes user input and fetches appropriate responses from the database.
* **Data Persistence**: Stores conversation history and user details in a MySQL database.
* **Responsive Design**: The chat interface is optimized for both desktop and mobile devices.

---

## 🛠️ Technology Stack

* **Backend Framework**: [Laravel](https://laravel.com/) (PHP)
* **Frontend**: HTML5, CSS3, JavaScript (jQuery/AJAX for asynchronous messaging)
* **Templating Engine**: Laravel Blade
* **Database**: MySQL
* **Server**: Apache/Nginx

---

## ⚙️ Installation & Setup

Follow these steps to set up the project locally.

### Prerequisites
Ensure you have the following installed:
* PHP (v8.0 or higher)
* Composer
* MySQL
* Node.js & NPM (optional, for compiling assets)

### Steps

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/kushagrakushwah/CHATBOT-ATMT-Laravel-MVC-.git](https://github.com/kushagrakushwah/CHATBOT-ATMT-Laravel-MVC-.git)
    cd CHATBOT-ATMT-Laravel-MVC-
    ```

2.  **Install PHP Dependencies**
    ```bash
    composer install
    ```

3.  **Environment Setup**
    * Duplicate the `.env.example` file and rename it to `.env`.
    ```bash
    cp .env.example .env
    ```
    * Open the `.env` file and configure your database credentials:
    ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    ```

4.  **Generate Application Key**
    ```bash
    php artisan key:generate
    ```

5.  **Run Migrations**
    Create the necessary tables in your database:
    ```bash
    php artisan migrate
    ```

6.  **Serve the Application**
    Start the local development server:
    ```bash
    php artisan serve
    ```
    The application will be accessible at `http://127.0.0.1:8000`.

---

## 📂 Project Structure

A brief overview of the key folders in this Laravel project:

* `app/Http/Controllers`: Contains the logic for handling chat requests (e.g., `ChatController.php`).
* `app/Models`: Database models representing tables (e.g., `Message.php`, `User.php`).
* `resources/views`: Blade templates for the frontend UI (e.g., `welcome.blade.php`, `chat/index.blade.php`).
* `routes/web.php`: Define the URL routes for the chatbot.
* `database/migrations`: Schema definitions for the database tables.

---

## 💡 How It Works

1.  **User Input**: The user types a message in the chat interface.
2.  **AJAX Request**: JavaScript sends the message to a Laravel Controller via a POST request.
3.  **Processing**: The Controller analyzes the input (using keyword matching or NLP logic) and queries the database for a matching answer.
4.  **Response**: The system returns the response to the frontend, which updates the chat window dynamically without reloading the page.

---

## 👨‍💻 Author

**Kushagra Kushwah**
* **Role**: Intern (1 Month)
* **Company**: ATMT
* **GitHub**: [kushagrakushwah](https://github.com/kushagrakushwah)

---

## 📝 License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
