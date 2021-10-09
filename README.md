# GraphQL Server using Express
This project involves backend implementation of a graphql server using express. 

## Instructions:
To setup this project please look at the following instructions:
- Clone this repository: `git clone https://github.com/zshanahmed/node-graphql.git`
- Install the dependencies for the project: `npm install`
- Run the backend server: `npm run devStart`
- Visit the url to access the GraphIQL interface: http://localhost:5000/graphql

## Queries:
This GraphQL supports the following queries among other possible query combinations:
#### Authors: 
- All of the authors can be queried as follows:
```
{
  authors {
    id
    name
    books
  }
}
```
- To get a single author the author id needs to to be passed in the query:
```
{
  author(id: 1) {
    name
    books
  }
}
```
- Get all of the books written by the author:
```
  {
    author(id: 1) {
      books
    }
  }
```
#### Books: 
- All of the books can be queried as follows with their author names:
```
{
  books {
    id
    name
    author {
      name
    }
  }
}
```
- To get a single book the book id needs to to be passed in the query:
```
{
  book(id: 1) {
    name
    author
  }
}
```

## Mutations:
The server supports following mutations:
- Adding a book to the database:
```
addBook(name: 'New Name", authorId: 1) 
{
  name
}
```

- Adding an author to database:
```
addAuthor(name: "New Author") {
  name
}
```

