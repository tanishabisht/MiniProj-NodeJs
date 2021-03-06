# Node Js

## Branches
- expressJs
- templating_engine
  - Examples: (ejs, pug, handlebars)
- MVC
  - Modal: Represents data structure and data manipulation functions
  - View: What user sees
  - Controller: The in between logic that tells which Model to work with and which View to render
  - Routes: on what path which controller should execute
- MongoDB
  - Creating db connection
  - Setting up db connection
  - `insertOne() | insertMany()`: Save documents in collection of db
  - `find().toArray()`: Fetch all data from collection
  - `find({ _id:new mondodb.ObjectId(id) }).next()`: Fetch data by id from collection
  - `updateOne({ _id:new mondodb.ObjectId(id) }, {$set:{title,desc})`: Update data by id from collection
  - `deleteOne({ _id:new mondodb.ObjectId(id) })`: Delete document by id from collection
- Mongoose
  - refer [mongoose documentation](https://mongoosejs.com/docs/)
  - `mongoose.connect('url')`: setting db connection
  - `mongoose.Schema()`: creating Schema
  - `mongoose.model('Name of the model', name_of_schema)`: create a model
  - This creates a collection with the model_name all smalls and plural
  - Add document
  - Fetch all documents
  - Fetch document by id
  - Delete document by id
  - Update document by id
  - POPULATE
    ```javascript
    .populate('fieldName', 'what field to keep and what not')
    .populate('userId', 'name -_id').execPopulate()
    ```
  - SELECT: `.select('title price -_id')`



## Dependencies
- `express`: provides middleware functionality to nodejs and handles nitty-gritty work so that we could focus on the logic
- `mongodb`: gives access to mongodb driver that helps connect with our mongodb database
- `mongoose`: encapsulates mongodb syntax into classes, which are easy to understand for a non-mongodb user
- `ejs`: templating engine
- `body-parser`: for parsing post requests
- `bcryptjs`: for password encryption and decryption