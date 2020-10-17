# handling-database-credentials
# A simple solution to handle the passing of database credentials in Node.js connecting to MongoDB

# 1. Install the npm package, "dotenv"
(Refer to this site: https://www.npmjs.com/package/dotenv for more information)

# 2. Create a ".env" file with your DB credentials.

# 3. App.js usage:

const mongoose = require("mongoose");
const dotenv = require("dotenv").config();

// Connect to MongoDB
const dbUrl = "mongodb+srv://" + dotenv.parsed.DB_USER + ":" + dotenv.parsed.DB_PASSWORD  + "@" + dotenv.parsed.DB_HOST + "/" + dotenv.parsed.DB_DATABASE;
mongoose.connect(dbUrl, { useNewUrlParser: true, useUnifiedTopology: true });

   
