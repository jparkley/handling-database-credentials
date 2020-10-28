# Node.js: How To Handle Your Database Credentials

This is is a simple solution to handle passing of database credentials in Node.js to connect to MongoDB.

# Installation / Configuration

1. Install the npm package, "dotenv"
```
npm i dotenv
```

2. Create a ".env" file with your DB credentials.

3. Usage
```
const mongoose = require("mongoose");
const dotenv = require("dotenv").config();

// Connect to MongoDB
const dbUrl = "mongodb+srv://" + dotenv.parsed.DB_USER + ":" + dotenv.parsed.DB_PASSWORD  + "@" + dotenv.parsed.DB_HOST + "/" + dotenv.parsed.DB_DATABASE;
mongoose.connect(dbUrl, { useNewUrlParser: true, useUnifiedTopology: true });
```

# Links
This project requires [Node.js](https://nodejs.org/) v12+ to run.
[npmjs.com/package/dotenv] https://www.npmjs.com/package/dotenv 

# Contributing
Please feel free to contribute or add comments. 
- Fork it (https://github.com/jparkley/readme)
:musical_note:


## License

This project is licensed under the [CC0 1.0 Universal](LICENSE.md)
