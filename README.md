
## Features

- Server

  - User and Message models with `1:N` relation
  - Full CRUD REST API operations for both Message and User models
  - Passport authentication with local `email/password`, Facebook and Google OAuth strategies and JWT protected APIs
  - `User` and `Admin` roles
  - NodeJS server with Babel for new JS syntax unified with React client
  - `async/await` syntax across whole app
  - Joi server side validation of user's input
  - Single `.env` file configuration
  - Image upload with Multer
  - Database seed

- Client

  - React client with functional components and Hooks
  - Redux state management with Thunk for async actions
  - CSS agnostic, so you don't waste your time replacing my CSS framework with yours
  - Home, Users, Profile, Admin, Notfound, Login and Register pages
  - Protected routes with Higher order components
  - Different views for unauthenticated, authenticated and admin user
  - Edit/Delete forms for Message and User with Formik and Yup validation
  - Admin has privileges to edit and delete other users and their messages
  - Layout component, so you can have pages without Navbar
  - Loading states with Loader component
  - Single config file within `/constants` folder

## Installation

Read on on how to set up this for development. Clone the repo.

```
$ git clone https://github.com/nemanjam/mern-boilerplate.git
$ cd mern-boilerplate
```

### Server

#### .env file

Rename `.env.example` to `.env` and fill in database connection strings, Google and Facebook tokens, JWT secret and your client and server production URLs.

#### Generate certificates

Facebook OAuth requires that your server runs on `https` in development as well, so you need to generate certificates. Go to `/server/security` folder and run this.

```
$ cd server/security
$ openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout cert.key -out cert.pem -config req.cnf -sha256
```

#### Install dependencies

```
$ cd server
$ npm install
```

#### Run the server

You are good to go, server will be available on `https://localhost:5000`

```
$ npm run server
```

### Client

Just install the dependencies and run the dev server. App will load on `https://localhost:3000`.

```
$ cd client
$ npm install
$ npm start
```
That's it.