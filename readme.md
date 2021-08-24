//To start any modules use the codes
npm init
npx express-generator --hbs
npm install
npm install nodemon -g
"start": "nodemon ./bin/www"
npm install express-handlebars
npm i express-fileupload
npm install mongodb
in cmd: "C:\Program Files\MongoDB\Server\4.4\bin\mongo.exe"
delete db: db.product.deleteMany({})
to show dbs: show dbs
to use dbs: use db_name
to show collections: show collections
to get details of collections: db.getCollectionInfos();
to get content inside the collection: db.collection_name.find().pretty();

//extra additions to index.js

var MongoClient = require('mongodb').MongoClient
router.post('/submit',function(req,res){
  console.log(req.body)
  MongoClient.connect("mongodb://localhost:27017",function(err,client){
    if(err){
    
      console.log('error')
    }
    else{
      client.db('new').collection('user').insertOne(req.body)
    }
  })
  res.send('Got it')
})

//To format code
ctrl+k+f

Steps:
index.hbs =  navbar add+ cards add
index.html = 