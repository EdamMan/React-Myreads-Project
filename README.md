# React-Myreads-Project

## About Project
In the MyReads React project, a bookshelf app is created that allows you to select and categorize books you have read, are currently reading, or want to read

## Features of Myreads Project
+ user can add books to a specific categorize like (Currently Reading, Want to Read, Read)
+ user can move books from any categorize to any categorize the user wants.
+ user can search books from an BookAPI and get the result based on the input.
+ user can add the books on their choice in any categorize.

## Deployed in Heroku
Project link is [MyReads](https://myreads-status-reactapp.herokuapp.com/)

## TL;DR

To get started developing right away:

* install all project dependencies with `npm install`
* start the development server with `npm start`

## Backend Server

To simplify your development process, we've a backend server for develop against. The provided file [`BooksAPI.js`](src/BooksAPI.js) contains the methods that will need to perform necessary operations on the backend:

* [`getAll`](#getall)
* [`update`](#update)
* [`search`](#search)

### `getAll`

Method Signature:

```js
getAll()
```

* Returns a Promise which resolves to a JSON object containing a collection of book objects.
* This collection represents the books currently in the bookshelves in your app.

### `update`

Method Signature:

```js
update(book, shelf)
```

* book: `<Object>` containing at minimum an `id` attribute
* shelf: `<String>` contains one of ["wantToRead", "currentlyReading", "read"]  
* Returns a Promise which resolves to a JSON object containing the response data of the POST request

### `search`

Method Signature:

```js
search(query)
```

* query: `<String>`
* Returns a Promise which resolves to a JSON object containing a collection of a maximum of 20 book objects.
* These books do not know which shelf they are on. They are raw results only. You'll need to make sure that books have the correct state while on the search page.

## Important
The backend API uses a fixed set of cached search results and is limited to a particular set of search terms, which can be found in [SEARCH_TERMS.md](SEARCH_TERMS.md). That list of terms are the _only_ terms that will work with the backend, so don't be surprised if your searches for Basket Weaving or Bubble Wrap don't come back with any results.

## Create React App

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).




