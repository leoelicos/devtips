# devtips

Node.js, Express.js, uuid

![Node.js](https://img.shields.io/badge/16.15.0%20LTS-0?label=Node.js&style=for-the-badge&labelColor=white&color=black) ![Express.js](https://img.shields.io/badge/4.18.1-0?label=Express&style=for-the-badge&labelColor=white&color=black) ![uuid](https://img.shields.io/badge/8.3.2-0?label=uuid&style=for-the-badge&labelColor=white&color=black)

## Introduction

devtips builds on top of an application that allows users to give tips or suggestions, as well as leave feedback. The extension is that it has a wildcard route for serving up a 404 page, as well as a diagnostics route for logging usage statistics like failed form validation.

The app uses `express.js` to coordinate the routes, and `uuid` to generate unique error ids. The app is deployed on Heroku.

I made this app to learn about `Express` including `helpers`, `middleware`, the `public` folder, `routes`, and `server.js`.

## Installation

| Steps                | Details                                               |
| -------------------- | ----------------------------------------------------- |
| Install Node.js      | Download it at https://nodejs.org/en/                 |
| Clone this repo      | ` git clone https://github.com/leoelicos/devtips.git` |
| Install dependencies | ` npm install`                                        |

## Usage

### Insomnia

| Steps                                                  | Details                                                           |
| ------------------------------------------------------ | ----------------------------------------------------------------- |
| Start the server from command line                     | `npm start`                                                       |
| Go to the root                                         | GET `localhost:3001`                                              |
| Try to add a Tip but with an error                     | Tip: "Use kebab-case for CSS!" User: "Leo"                        |
| Note the alert that it is invalid                      | `Invalid username! Min. 4 characters`                             |
| …or another kind of error                              | `Tip must be at least 15 characters`                              |
| Click OK                                               |                                                                   |
| See these diagnostic logs in Insomnia                  | GET `localhost:3001/api/diagnostics` in `Insomnia` or a browser   |
| Test the wildcard route with a page that doesn't exist | GET `https://dvtps.herokuapp.com/test` in `Insomnia` or a browser |

### Heroku Deployment

| Steps                                                  | Details                                     |
| ------------------------------------------------------ | ------------------------------------------- |
| Go to the root                                         | https://dvtps.herokuapp.com/                |
| Try to add a Tip but with an error                     | Tip: "Use kebab-case for CSS!" User: "Leo"  |
| Note the alert that it is invalid                      | `Invalid username! Min. 4 characters`       |
| …or another kind of error                              | `Tip must be at least 15 characters`        |
| Click OK                                               |                                             |
| See these diagnostic logs                              | https://dvtps.herokuapp.com/api/diagnostics |
| Test the wildcard route - something that doesn't exist | https://dvtps.herokuapp.com/test            |

## Video Demo

https://user-images.githubusercontent.com/99461390/170290283-a197c255-1c7b-4c4a-95f6-b4dba9ef8e82.mp4

---

## Screenshots

### Screenshot: Insomnia diagnostics

![Insomnia diagnostics](https://user-images.githubusercontent.com/99461390/170288512-d3969299-7829-400f-944e-787e7caf5cce.jpg)

### Screenshot: Heroku testing - bad username

![Heroku testing - bad username](https://user-images.githubusercontent.com/99461390/170288533-c910593c-26b5-41a6-8b28-eb937c316cf0.jpg) ![Heroku testing - alert](https://user-images.githubusercontent.com/99461390/170288546-8ec84157-dd59-4eab-9935-8edceab217d9.jpg)

### Screenshot: Heroku diagnostics

![Heroku diagnostics](https://user-images.githubusercontent.com/99461390/170288554-ef91fc1e-2090-4759-9c14-f7b64a02fd65.jpg)

## Credits

- BCS Resources

## License

&copy; Leo Wong <leoelicos@gmail.com>

Licensed under the [MIT License](./LICENSE).
