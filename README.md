# Diagnostic Routes

Node.js, Express.js, uuid

![Node.js](https://img.shields.io/badge/16.15.0%20LTS-0?label=Node.js&style=for-the-badge&labelColor=white&color=black) ![Express.js](https://img.shields.io/badge/4.18.1-0?label=Express&style=for-the-badge&labelColor=white&color=black) ![uuid](https://img.shields.io/badge/8.3.2-0?label=uuid&style=for-the-badge&labelColor=white&color=black)

## Introduction

Diagnostic Routes builds on top of an application that allows users to give tips or suggestions, as well as leave feedback. The extension is that it has a wildcard route for serving up a 404 page, as well as a diagnostics route for logging usage statistics like failed form validation.

The app uses `express.js` to coordinate the routes, and `uuid` to generate unique error ids. The app is deployed on Heroku.

I made this app to learn about `Express` including `helpers`, `middleware`, the `public` folder, `routes`, and `server.js`.

## Installation

| Steps                | Details                                                                      |
| -------------------- | ---------------------------------------------------------------------------- |
| Install Node.js      | Download it at https://nodejs.org/en/                                        |
| Clone this repo      | ` git clone https://github.com/leoelicos/bcs-10-command-line-word-guess.git` |
| Install dependencies | ` npm install`                                                               |

## Usage

### Insomnia

| Steps                                                  | Details                                                                                 |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| Start the server from command line                     | `npm start`                                                                             |
| Go to the root                                         | GET `localhost:3001`                                                                    |
| Try to add a Tip but with an error                     | Tip: "Use kebab-case for CSS!" User: "Leo"                                              |
| Note the alert that it is invalid                      | `Invalid username! Min. 4 characters`                                                   |
| …or another kind of error                              | `Tip must be at least 15 characters`                                                    |
| Click OK                                               |                                                                                         |
| See these diagnostic logs in Insomnia                  | GET `localhost:3001/api/diagnostics` in `Insomnia` or a browser                         |
| Test the wildcard route with a page that doesn't exist | GET `https://leoelicos-diagnostic-routes.herokuapp.com/test` in `Insomnia` or a browser |

### Heroku Deployment

| Steps                                                  | Details                                                           |
| ------------------------------------------------------ | ----------------------------------------------------------------- |
| Go to the root                                         | https://leoelicos-diagnostic-routes.herokuapp.com/                |
| Try to add a Tip but with an error                     | Tip: "Use kebab-case for CSS!" User: "Leo"                        |
| Note the alert that it is invalid                      | `Invalid username! Min. 4 characters`                             |
| …or another kind of error                              | `Tip must be at least 15 characters`                              |
| Click OK                                               |                                                                   |
| See these diagnostic logs                              | https://leoelicos-diagnostic-routes.herokuapp.com/api/diagnostics |
| Test the wildcard route - something that doesn't exist | https://leoelicos-diagnostic-routes.herokuapp.com/test            |

## Video Demo

---

## Screenshots

### Screenshot: Routes

### Screenshot: 404 page

### Screenshot: Deployed on Heroku

## Credits

-  BCS Resources

## License

&copy; Leo Wong <leoelicos@gmail.com>

Licensed under the [MIT License](./LICENSE).
