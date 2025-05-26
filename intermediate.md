# IntermediateMango Database Query Results

## Dataset Info
- Database: student
- Collection: details
- Total: 4 students
- Fields: _id, name, scores

##  Remove 1st Element In Array Scores in Document Whose Name = Rajiv Using Pop Operator

**Query:**
```javascript
db.collection.updateOne({ name: "Rajiv" },{ $pop: { scores: -1 } })
```

### Output:
```json
[
  {
     "_id": 1,
     "name": "Rajiv",
     "scores": [
     9,10
  ]
  },
  {
     "_id": 2,
     "name": "Yogesh",
     "scores": [
     8,9,10
  ]
  },
  {
     "_id": 3,
     "name": "Vinay",
     "scores": [
      8,9,10
  ]
  },
  {
     "_id": 4,
     "name": "Rakesh",
     "scores": [
     8,9,10
  ]
  }
]
```

---

##  Remove Last Element In Array Scores In Document Whoose Name = Vinay Using Pop Operator 

### Query:
```javascript
db.collection.updateOne({ name: "Vinay" },{ $pop: { scores: 1 } })
```

### Output:
```json
[
  {
    "_id": 1,
     "name": "Rajiv",
     "scores": [
     9,10
  ]
  },
  {
    "_id": 2,
     "name": "Yogesh",
     "scores": [
     8,9,10
  ]
  },
  {
    "_id": 3,
     "name": "Vinay",
     "scores": [
      8,9
  ]
  },
  {
    "_id": 4,
     "name": "Rakesh",
     "scores": [
     8,9,10
  ]
  }
]
```
---