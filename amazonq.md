# PHP-based Product Management System

This project is a PHP-based web application for managing products, user authentication, and customer support.

The system provides a comprehensive solution for businesses to handle their product inventory, user accounts, and customer interactions. It features a user-friendly interface for product management, including creation, editing, and deletion of products. The application also includes a secure login system and a dashboard for easy navigation.

Key features of this product management system include:
- User authentication and authorization
- Product CRUD (Create, Read, Update, Delete) operations
- Search functionality for products
- Customer support form
- Responsive design for various devices

## Repository Structure

```
.
├── assets/
│   ├── conteudo/
│   ├── database/
│   ├── html/
│   └── styles/
├── dash.php
├── deletar-produto.php
├── editar-produto.php
├── form-criar-produto.php
├── form-editar-produto.php
├── form-editar-usuario.php
├── form-suport.php
├── index.php
├── login.php
└── produtos.php
```

### Key Files and Directories:

- `assets/`: Contains subdirectories for various application components
  - `conteudo/`: PHP files for different pages and components
  - `database/`: PHP scripts for database operations and authentication
  - `html/`: HTML templates for creating the user interface. These files are used solely for interface creation and do not contain any system logic.
  - `styles/`: CSS files for styling
- `index.php`: Main entry point of the application
- `login.php`: Handles user authentication
- `produtos.php`: Manages product listing and search
- `dash.php`: User dashboard
- `form-criar-produto.php`: Form for creating new products
- `form-editar-produto.php`: Form for editing existing products
- `deletar-produto.php`: Handles product deletion

## Database Schema

The application uses two main tables in its database schema: 'usuarios' for user management and 'produtos' for product information.

### Table: usuarios

| Field | Type         | Description                |
|-------|--------------|----------------------------|
| id    | INT          | Unique identifier for user |
| nome  | VARCHAR(255) | User's name                |
| email | VARCHAR(255) | User's email address       |
| senha | VARCHAR(255) | User's password (hashed)   |

### Table: produtos

| Field        | Type         | Description                     |
|--------------|--------------|----------------------------------|
| id_produto   | INT          | Unique identifier for product    |
| nome_produto | VARCHAR(255) | Name of the product              |
| info_produto | VARCHAR(255) | Detailed information about product|
| nome_img     | VARCHAR(255) | Name of the product image file   |
| path_img     | VARCHAR(255) | Path to the product image file   |

## Usage Instructions

### Installation

1. Ensure you have a web server with PHP support (e.g., Apache, Nginx) and MySQL installed.
2. Clone the repository to your web server's document root.
3. Import the database schema (not provided in the repository structure, you may need to create this based on the application's requirements).
4. Configure the database connection in `assets/database/conexao.php`.

### Configuration

1. Open `assets/database/conexao.php` and update the database credentials:

```php
$servername = "localhost";
$username = "your_username";
$password = "your_password";
$dbname = "your_database_name";
```

2. Ensure that the web server has write permissions for the `assets` directory.

### Getting Started

1. Navigate to the application's URL in your web browser.
2. Log in using your credentials or create a new account if required.
3. Use the dashboard to manage products, view reports, or access customer support features.

### Product Management

To add a new product:
1. Click on "Add Product" in the dashboard.
2. Fill out the form in `form-criar-produto.php`.
3. Submit the form to create the product.

To edit a product:
1. Navigate to the product list.
2. Click on the "Edit" button next to the product you want to modify.
3. Update the information in the form provided by `form-editar-produto.php`.
4. Save your changes.

To delete a product:
1. Go to the product list.
2. Click on the "Delete" button next to the product you want to remove.
3. Confirm the deletion when prompted.

### Search Functionality

The application includes a search feature for products:

1. On the products page, locate the search input field.
2. Enter your search query.
3. Press Enter or click the search button.
4. The page will reload with filtered results based on your search term.

### Search Function in produtos.php

The search functionality in `produtos.php` is implemented using a combination of client-side JavaScript and server-side PHP processing. Here's how it works:

1. Client-side (JavaScript):
   - The `assets/database/busca.js` file contains the client-side logic for the search function.
   - It listens for the "Enter" key press event on the search input field (element with ID "search").
   - When the user presses "Enter", the `searchData()` function is triggered.
   - This function redirects the user to `produtos.php` with the search query appended as a URL parameter.

2. Server-side (PHP):
   - The `produtos.php` file handles the server-side processing of the search query.
   - When a search query is present in the URL parameters, the script likely performs the following actions:
     a. Retrieves the search query from the `$_GET` superglobal.
     b. Sanitizes the input to prevent SQL injection attacks.
     c. Constructs a SQL query to search for products matching the query in relevant fields (e.g., nome_produto, info_produto).
     d. Executes the query against the 'produtos' table in the database.
     e. Fetches the matching results.
     f. Renders the filtered product list in the HTML output.

This approach allows for a responsive search experience, where users can quickly search for products without needing to interact with additional buttons or forms. The search results are dynamically loaded on the same page, providing a seamless user experience.

### Troubleshooting

Common issues and solutions:

1. Database Connection Errors:
   - Ensure that the database credentials in `assets/database/conexao.php` are correct.
   - Verify that the MySQL service is running on your server.
   - Check if the specified database exists and the user has proper permissions.

2. File Permission Issues:
   - If you encounter errors related to file writing or reading, check the permissions of the `assets` directory and its subdirectories.
   - Ensure that the web server process has read and write access to necessary directories.

3. Search Not Working:
   - Verify that the JavaScript file `assets/database/busca.js` is properly linked in your HTML.
   - Check the browser console for any JavaScript errors.
   - Ensure that the element with ID "search" exists in your HTML structure.

Debugging:

To enable debug mode:
1. Open `assets/database/conexao.php`.
2. Add the following lines at the beginning of the file:

```php
error_reporting(E_ALL);
ini_set('display_errors', 1);
```

This will display PHP errors on the page, which can help identify issues.

For JavaScript debugging:
1. Open your browser's developer tools (usually F12 or right-click and select "Inspect").
2. Go to the Console tab to see any JavaScript errors or logs.

## Data Flow

The application follows a typical PHP web application data flow:

1. User sends a request by accessing a PHP file (e.g., `produtos.php`).
2. The PHP script connects to the database using the credentials in `assets/database/conexao.php`.
3. Database queries are executed to fetch or manipulate data.
4. The PHP script processes the data and generates HTML output.
5. The server sends the generated HTML back to the user's browser.

For the search functionality:
1. User enters a search term in the input field.
2. The JavaScript in `assets/database/busca.js` captures the Enter key press.
3. The script redirects to `produtos.php` with the search term as a query parameter.
4. `produtos.php` processes the search parameter and queries the database for matching products.
5. The filtered results are displayed to the user.

```
[User] -> [Browser] -> [PHP Scripts] -> [Database]
   ^                        |
   |                        v
[HTML Response] <- [Generated HTML]
```

Note: Ensure that all database queries are properly sanitized to prevent SQL injection attacks. Use prepared statements or parameterized queries for enhanced security.