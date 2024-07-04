### Basics
Query an object.
Query:
```graphql
{books}
```
Responce:
```graphql
{
  "errors": [
    {
      "message": "`books` is an object, interface or union type field. Leaf selections on objects, interfaces, and unions without subfields are disallowed.",
      "locations": [
        {
          "line": 1,
          "column": 2
        }
      ],
      "extensions": {
        "declaringType": "Query",
        "field": "books",
        "type": "[Book!]!",
        "responseName": "books",
        "specifiedBy": "http://spec.graphql.org/October2021/#sec-Field-Selections-on-Objects-Interfaces-and-Unions-Types"
      }
    }
  ]
}
```
Does not query ab object.
```graphql
{
  books {
    bookId
    name
    genre
    pages
  }
}
```
```graphql
{
  "data": {
    "books": [
      {
        "bookId": 17,
        "name": "Harry Potter",
        "genre": "FANTASY",
        "pages": 267
      },
      {
        "bookId": 54,
        "name": "Memory Man",
        "genre": "HORROR",
        "pages": 560
      },
      {
        "bookId": 66,
        "name": "Exhalation",
        "genre": "HORROR",
        "pages": 368
      },
      {
        "bookId": 91,
        "name": "SomeName",
        "genre": "HORROR",
        "pages": 333
      }
    ]
  }
}
```
Related entities
```graphql
{
  books {
    bookId
    name
    genre
    pages
    author {
      authorId
      name
    }
  }
}
```
```graphql
{
  "data": {
    "books": [
      {
        "bookId": 17,
        "name": "Harry Potter",
        "genre": "FANTASY",
        "pages": 267,
        "author": {
          "authorId": 110,
          "name": "J.K. Rowling"
        }
      },
      {
        "bookId": 54,
        "name": "Memory Man",
        "genre": "HORROR",
        "pages": 560,
        "author": null
      },
      {
        "bookId": 66,
        "name": "Exhalation",
        "genre": "HORROR",
        "pages": 368,
        "author": null
      },
      {
        "bookId": 91,
        "name": "SomeName",
        "genre": "HORROR",
        "pages": 333,
        "author": null
      }
    ]
  }
}
```
operation type
```graphql
query {
  books {
    bookId
    name
    genre
    pages
    author {
      authorId
      name
    }
  }
}
```
assign a name for a query
```graphql
query GetBooks {
  books {
    bookId
    name
    genre
    pages
    author {
      authorId
      name
    }
  }
}
```
