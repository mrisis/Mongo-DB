# Mongo DB

---
# DataBasse

## show databases

```bash
show dbs
```

---

## create a new database

```bash
use name_of_database
```

## delete  a database

```bash
db.dropDatabase()
```

---

# collections 

## show collections

```bash
show collections
```

## create a collection

```bash
db.createCollection('name of collections')
```

## rename a collection

```bash
db.collection_name.renameCollection('new_name')
```

## delete a collection

```bash
db.collection_name.drop()
```

---
# Insert

## insnertOne

```bash
db.collection_name.insertOne({key:"value"})
```

## insertMany

```bash
db.collection_name.insertMnay([{key:"value"},{key:"value"},...])
```

---

# find

## findOne

```bash
db.collection_name.findOne({filter})
```

## find

```bash
db.collection_name.find({filter},{projection})
```

**examples**

__db.user.findOne({name:"reza"})__


__db.user.find({name:"reza"},{name:1 , family:1 ,_id:0})__


---

# UPDATE

## updateOne

```bash
db.collection_name.updateOne({filter},{update},{options})
```

**examples**

``` bash
    db.users.updateOne(
    {name:"reza"},
    {$set:{name:"ali",family:"mohammadi"}},
    {upsert:true}
```

## updateMany

```bash
db.collection_name.updateMany({filter},{update},{options})
```

**examples :**

``` bash
    db.users.updateMany(
    {name:"sara"},
    {$set:{name:"tina",family:"yavari"}},
    {upsert:true}
```

## replaceOne

```bash
db.collection_name.replaceOne({filter},{replacement},{options})
```

**examples :**

``` bash
    db.users.replaceOne(
    {name:"ali"},
    {name:"mamad",family:"rezaei" , age:22}
```

---
# DELETE

## deleteOne

```bash
db.collection_name.deleteOne({filter})
```

**examples :**

``` bash
    db.users.deleteOne(
    {name:"ali"}
```

## deleteMany

```bash
db.collection_name.deleteMany({filter})
```

**examples :**

``` bash
    db.users.deleteMany(
    {name:"reza" , age:22}
```





































