--------------- Windows + R -----------------
npm install json-server
Usage
Create a db.json or db.json5 file

{
  "posts": [
    { "id": "1", "title": "a title", "views": 100 },
    { "id": "2", "title": "another title", "views": 200 }
  ],
  "comments": [
    { "id": "1", "text": "a comment about post 1", "postId": "1" },
    { "id": "2", "text": "another comment about post 1", "postId": "1" }
  ],
  "profile": {
    "name": "typicode"
  }
}
View db.json5 example
Pass it to JSON Server CLI

$ npx json-server db.json
Get a REST API

$ curl http://localhost:3000/posts/1
{
  "id": "1",
  "title": "a title"
}

--------------------------------------------------------------------------------
GET    /posts
GET    /posts/:id
POST   /posts
PUT    /posts/:id
PATCH  /posts/:id
DELETE /posts/:id

# Same for comments
GET   /profile
PUT   /profile
PATCH /profile

