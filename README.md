# Node Express Server with REST API and Svelte.dev as web framework

Based on [node-express-server-rest-api](https://github.com/rwieruch/node-express-server-rest-api) project that was combined with Svelte.dev project created by

```
npx degit sveltejs/template my-svelte-project
```

## Features

- Babel 7
- Environment Variables
- Express
- REST API
- Svelte.dev
- Hot reload

## Requirements

- [node & npm](https://nodejs.org/en/)
- [git](https://www.robinwieruch.de/git-essential-commands/)

## Installation

- `git clone git@github.com:keenmate/node-express-svelte.git`
- `cd node-express-svelte`
- `npm install`
- `npm run dev` to run development environment with hot reload
- OR
- `npm start` to just serve already generated data in public folder and REST endpoints
- optional: include _.env_ in your _.gitignore_

### GET Routes

- visit http://localhost:3000
  - / will display Hello world page generated with svelte
  - /messages
  - /messages/1
  - /users
  - /users/1

### Beyond GET Routes

#### CURL

- Create a message with:
  - `curl -X POST -H "Content-Type:application/json" http://localhost:3000/messages -d '{"text":"Hi again, World"}'`
- Delete a message with:
  - `curl -X DELETE -H "Content-Type:application/json" http://localhost:3000/messages/1`

#### Postman

- Install [Postman](https://www.getpostman.com/apps) to interact with REST API
- Create a message with:
  - URL: http://localhost:3000/messages
  - Method: POST
  - Body: raw + JSON (application/json)
  - Body Content: `{ "text": "Hi again, World" }`
- Delete a message with:
  - URL: http://localhost:3000/messages/1
  - Method: DELETE
