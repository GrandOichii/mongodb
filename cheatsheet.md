# MongoSH Chearsheet

## Commands
* `show dbs` - list all databases
* `use <db name>` - switches to the specified db. If doens't exists, cretes it first. **Will not be visible if doens't have any collections.**
* `db.createCollection("<collection name>")` - creates a new collection in the current db.
* `db.dropDatabase()` - drops the current db.
* `db.<collection name>.insertOne(<json>)` - creates a new entry in the specified collection. **_id is created automatically.**
* `db.<collection name>.insertOne(<[json]>)` - creates a new entry for each item in the list in the specified collection.
* `db.<collection name>.find()` - lists all entries of the specified collection.
* `db.<collection name>.find().limit(<amount>)` - lists the first \<amount\> entries of the specified collection.
* `db.<collection name>.find().sort(<sort params>)` - lists all entries of the specified collection in a sorted format (using the sort parameters).
* `db.<collection name>.find(<query>, <projection>)` - lists all entries of the specified collection, uses the *query* argument to select the matching entries and displays them using the *projection* argument.
* `db.<collection name>.updateOne(<query>, <update>)` - updates the first entry that matches the *query* argument using the *update* argument. (example: `{$set: {name: "new_name"}, $unset: {old: ""}}`)
* `db.<collection name>.updateOne(<query>, <update>)` - same as `updateOne`, instead selects all the entries. To match all, set *query* to `{}`.
* `db.<collection name>.deleteOne(<query>)` - deletes the first entry that matches the `query` argument.
* `db.<collection name>.deleteMany(<query>)` - deletes all entries that match the `query` argument.