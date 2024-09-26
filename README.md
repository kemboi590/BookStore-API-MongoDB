# BookStore API

This is a simple BookStore API built with **ASP.NET Core** and **MongoDB**. The API follows the **MVC** pattern and provides basic CRUD functionality for managing books in a MongoDB database.

## Features

- ASP.NET Core Web API using the MVC pattern.
- MongoDB for database storage.
- CRUD operations (Create, Read, Update, Delete) for managing books.
- Proper separation of concerns between Controllers, Models, and Services.

## Project Structure

## Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download) install it from the official website.
- [MongoDB](https://www.mongodb.com/try/download/community) installed locally or a MongoDB Atlas cloud database.
- Visual Studio or any preferred code editor.

## Setup and Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/kemboi590/BookStore-API-MongoDB.git
   cd BookStoreApi
   ```

2. **Install project dependencies**:

   ```bash
   dotnet restore
   ```

3. **MongoDB Setup**:

- You will need to configure the MongoDB connection string and database settings in _appsettings.json_

```code
{
  "BookStoreDatabase": {
    "ConnectionStrings": "your-mongo-db-connection-string",
    "DatabaseName": "BookStore",
    "BooksCollectionName": "Books"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```

4. **Run the Application**:

```code
dotnet run
```

5. **Testing your API**:

- **Get all Books**:

```code
GET /api/Books
```

- **Get Book by ID**:

```code
GET /api/Books
```

- **Create a new Book**:

```code
POST /api/Books
Body:
{
    "bookName": "Design Patterns",
    "price": 54.43,
    "category": "Computers",
    "author": "Ralph Johnson"
}

```

- **Update a Book**:

```code
PUT /api/Books/{id}
```

- **Delete a Book**:

```code
DELETE /api/Books/{id}
```
