Sure! Here's the documentation converted into a block of code in Markdown format:

# Babel Idiomas

## Overview
Babel Idiomas is a project aimed at creating a system for language learning. It includes functionalities for managing courses, students, and scheduling classes.

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Features](#features)
4. [Configuration](#configuration)
5. [Contributing](#contributing)
6. [License](#license)
7. [Contact](#contact)

## Installation
To install and set up Babel Idiomas, follow these steps:

1. **Clone the repository:**
   ```sh
   git clone https://github.com/luangaldinodev/babel-idiomas.git
   cd babel-idiomas
   ```

2. **Install dependencies:**
   ```sh
   composer install
   ```

3. **Set up the environment file:**
   Copy `.env.example` to `.env` and configure your environment variables:
   ```sh
   cp .env.example .env
   ```

4. **Generate the application key:**
   ```sh
   php artisan key:generate
   ```

5. **Run the migrations:**
   ```sh
   php artisan migrate
   ```

6. **Start the development server:**
   ```sh
   php artisan serve
   ```

## Usage
To use Babel Idiomas, follow these steps:

1. **Access the application:**
   Open your web browser and navigate to `http://localhost:8000`.

2. **Register and log in:**
   Create a new user account and log in to access the system.

3. **Manage your data:**
   Use the provided interface to manage courses, students, and schedules.

## Features
- **User Authentication:** Register and log in to access the system.
- **Course Management:** Create, update, and delete courses.
- **Student Management:** Add, update, and remove students.
- **Class Scheduling:** Schedule and manage class timings.

## Configuration
Configuration is managed via the `.env` file. Key configuration options include:

- **Database Configuration:** Set the database connection details.
- **Mail Configuration:** Configure the mail settings for notifications.

## Contributing
We welcome contributions to Babel Idiomas! To contribute, follow these steps:

1. **Fork the repository:**
   Click the "Fork" button on the top right of the repository page.

2. **Clone your fork:**
   ```sh
   git clone https://github.com/<your-username>/babel-idiomas.git
   cd babel-idiomas
   ```

3. **Create a new branch:**
   ```sh
   git checkout -b feature/my-new-feature
   ```

4. **Make your changes and commit them:**
   ```sh
   git commit -m 'Add some feature'
   ```

5. **Push to the branch:**
   ```sh
   git push origin feature/my-new-feature
   ```

6. **Create a pull request:**
   Open a pull request on the original repository.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
If you have any questions or need support, please contact us at [support@babelidiomas.com](mailto:support@babelidiomas.com).
```

Now you can use this block of code directly in your `DOCUMENTATION.md` file.