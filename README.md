# Blogging Application

This is a simple blogging application built using Node.js, Express.js, and MongoDB. Users can register, login, create blogs, and view blogs by different authors.

## Features

- **User Authentication:** Users can register with unique usernames and passwords. Authentication is done securely using JWT tokens.
- **Create Blogs:** Authenticated users can create blogs with titles and content. Each blog is associated with an author.
- **View Blogs:** Users can view blogs created by different authors.
- **Authorization:** Routes are protected using JWT tokens to ensure only authenticated users can create and view blogs.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your_username/blog-app.git
    ```

2. Install dependencies:

    ```bash
    cd blog-app
    npm install
    ```

3. Set up environment variables:
   
    Create a `.env` file in the root directory and add the following variables:

    ```plaintext
    PORT=5500
    MONGODB_URI=mongodb+srv://<username>:<password>@<your-cluster-url>/blogs
    ACCESS_TOKEN_SECRET=your_secret_key
    ```

4. Start the server:

    ```bash
    npm start
    ```

5. The server should now be running on `http://localhost:5500`.

## API Endpoints

- `POST /api/register`: Register a new user.
- `POST /api/login`: Login and generate access token.
- `POST /api/blogs`: Create a new blog (requires authentication).
- `GET /api/blogs/:authorID`: Get blogs by a specific author (requires authentication).
- `GET /api/blogs`: Get all blogs (requires authentication).

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- bcrypt
- JSON Web Tokens (JWT)

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE).



