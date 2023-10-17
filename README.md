# MongoDB Commands

## **Show Database :**

> To display all the available databases, you can use the command `show db`.

**Syntax :**

```js
show db
```

## **Use Database Or Create Database :**

> Whenever we perform operations or create a database, we can make use of the `use db` command. This command allows us to switch to a specific database and perform further operations within it.

**Syntax :**

```js
use db
```

**Example :**

```js
use college
```

## **Create Collection :**

To create a collection, you can use the `createCollection()` method in MongoDB.

**Example :**

```js
db.createCollection("students");
```

This will create a collection named `"students"` in the current database.

## **Insert One Document :**

> To insert only one document in a collection, we can make use of the `insertOne()` command.

**Syntax :**

```js
insertOne();
```

**Example :**

```js
db.students.insertOne({ name: "Shyam", RollNo: "21", Address: "Pune" });
```

## **Insert Multiple Document :**

> To insert multiple documents in a collection, we can make use of the `insertMany()` command.

**Syntax :**

```js
insertMany();
```

**Example :**

```js
db.students.insertMany([
  {
    name: "Shyam",
    RollNo: "21",
    Address: "Pune",
  },
  {
    name: "Ram",
    RollNo: "22",
    Address: "Mumbai",
  },
  {
    name: "",
    RollNo: "22",
    Address: "Nagar",
  },
]);
```

## **Find Documents from Collection :**

> The `find()` method is used to search for documents within a specified range according to some criteria.

**Syntax :**

```js
find();
```

**Example :**

```js
db.students.find({ RollNo: "22" });
```

> This will return all the students with roll number as '22'.

## **Update Documents In A Collection :**

> You can update existing document using the `updateOne()`, `updateMany()` methods.

- `updateOne()` :

  >Updates only one matching record in collection, if no records are matched then it does not perform any operation and returns an error message.

**Syntax :**

```js
updateOne({key:value}, {$set: {key:value}});
```

**Example :**

```js
// Update one student in collection
db.students.updateOne(
  {
    name: "Shyam",
  },
  { 
    $set: { Address: "New York" } 
  }
)
```

- `updateMany():`

  > The `updateMany()` method updates all documents that match the specified filter.

**Syntax :**




