Moviee DB Queries:- 

Questions:- 

1:- get all documents 

2:- get all documents with writer set to "Quentin Tarantino" 

3:- get all documents where actors include "Brad Pitt" 

4:- get all documents with franchise set to "The Hobbit" 

5:- get all movies released in the 90s 

6:- get all movies released before the year 2000 or after 2010 

7:- count the number of writer from the movie collection 

8:- update an actor named "Samuel L. Jackson" to the movie "Pulp Fiction" 

9:- find all movies that have a synopsis that contains the word "Gandalf" 

10:- display the movie collection  based on year in descending order. 

11:- Display last two recent movie . 

Solutions:-  


1:- db.movie.find()

2:- db.movie.find({writer:"Quentin Tarantino"})

3:-mydb> db.movie.findMany({actors:"Brad Pitt"})

4:-mydb> db.movie.find({franchise:"The Hobbit"})

5:-db.movie.find({year:{$lt:2000}})

6:-db.movie.find({$or:[{year:{$lt:2000}},{year:{$gt:2010}}]})

7:-mydb> db.movie.distinct('writer').length

mydb> db.movie.distinct('writer')

8:-db.movie.update({title:"Pulp Fiction"},{$push:{"actors":"Samuel L. Jackson"}})

9:-

10:-mydb> db.movie.find().sort({year:-1})

11:-db.movie.find().sort({year:-1}).limit(2)


