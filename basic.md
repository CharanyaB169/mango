# BasicMango Database Query Results

## Dataset Info
- Database: employee
- Collection: collection
- Total: 5 employees
- Fields: _id, name, age, address

##  Remove Field Age Permanently Whose Name ='Kushal' Using unset Operator

**Query:**
```javascript
db.details.updateOne({ name: "Kushal" },{ $unset: { age: "" } })
```

### Output:
```json
[
  {
     "_id": 1,
     "name": "Abhinandan",
     "age": 21,
     "address": "Highway 37, Canada"
  },
  {
     "_id": 3,
     "name": "Pradeep",
     "age": 22,
     "address": "Apple st 652, UK"
  },
  {
     "_id": 5,
     "name": "Kushal",
     "address": "Valley 345, Australia"
  },
  {
     "_id": 2,
     "name": "Yasin Sharief",
     "age": 23,
     "address": "Lowstreet 27, USA"
  },
  {
     "_id": 4,
     "name": "Mukesh",
     "age": 26,
     "address": "Mountain 21, Canada"
  }
]
```

---

##  Remove Field Age Permanently In Documnent Using unset Operator 

### Query:
```javascript
db.collection.updateMany({},{ $unset: { age: "" } })
```

### Output:
```json
[
  {
     "_id": 1,
     "name": "Abhinandan",
     "address": "Highway 37, Canada"
  },
  {
     "_id": 3,
     "name": "Pradeep",
     "address": "Apple st 652, UK"
  },
  {
     "_id": 5,
     "name": "Kushal",
     "address": "Valley 345, Australia"
  },
  {
     "_id": 2,
     "name": "Yasin Sharief",
     "address": "Lowstreet 27, USA"
  },
  {
     "_id": 4,
     "name": "Mukesh",
     "address": "Mountain 21, Canada"
  }
]
```
---