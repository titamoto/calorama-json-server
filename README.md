# Calorama Server 🗃️

This is a repo for the JSON-Server of the Calorama web-app.
The server is deployed on https://calorama.onrender.com.

The GitHub repo for the Calorama app is located at https://github.com/titamoto/calorama.

## Setup

Fork and clone this repo. Then install the dependencies by running:

```sh
npm install
```

## Seeding Data

To set up your database, update the `db/seeds.json` file to contain an object
with a key pointing to an array of data, like this:

```json
{
  "foods": [
    {
      "id": 1,
      "name": "cucumber",
      "image": "./images/cucumber.jpg",
      "type": "vegetable",
      "grams": 100,
      "calories": 10
    },
    {
      "id": 2,
      "name": "tomato",
      "image": "./images/tomato.jpg",
      "type": "vegetable",
      "grams": 100,
      "calories": 19
    }
  ]
}
```

Then, run `npm run seed` to copy data from the `db/seeds.json` file to the
`db/db.json` file. `json-server` uses the `db.json` file to create your RESTful
API, so make sure your `db.json` file is always up to date!

Any time you want to reset your database back to your original data, run
`npm run seed` again. Doing this will overwrite all the data in your `db.json`
file, so make sure you don't have any data in that file that you don't mind
losing!

## Running the Server Locally

To run your server in development mode, run:

```sh
npm run dev
```

While running in development mode, the server will re-load any time you make
changes to the `db.json` file, so you can test our your seed data.

While your server is running, you can make requests to
[http://localhost:3000](http://localhost:3000). Check it out in the browser to
make sure your server works!
