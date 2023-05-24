# Basic Queries And Table Creation In SQL (PostgreSQL), and Comparing With MongoDB First Impression

I learned basic queries using SELECT, FROM, WHERE, ORDER BY, LIKE, DESC, and how to select specific columns and search for specific patterns of data in SQL. My first database management system I learned was MongoDB. Personally, I like SQL slightly more than NoSQL, mainly due to the way the logic flows. In MongoDB, a query is done using a method-like query on a database object like find, delete, and update. We then pass in the object we are looking for. I like SQL better in that it follows a more structural approach, where the commands can be explained in order. For example, given this query:
```
SELECT total
FROM billing
WHERE total BETWEEN 100 AND 200;
ORDER BY total DESC;
```
This query can easily be translated in English command-by-command: "Get all the totals from the billing table that are between 100 and 200, and sort them in descending order." Personally, I like this approach to queries because it can be quickly understood, and becomes increasingly useful as the complexity grows in the queries. 

However, personally, I think MongoDB shines in the area of creating data collections quickly. With MongoDB, creating a new set of data is as simple as calling the "db.collection.insertOne()" method, which will also create the collection if it does not already exist. Validation can be done, and that is actually a little hard to read in MongoDB, but nonetheless this still works nicely. We can also simply decouple the validation from the database and have the validation in the backend code itself. In PostgreSQL, we have to call:
```
CREATE TABLE myTableName(
  id SERIAL, 
  name text NOT NULL, 
  someNumber numeric CHECK (someNumber > 0)
)
```
This is actually nicer in terms of validation for me, because it reads like english and is easy to read and write. To summarize, I personally like PostgreSQL in terms of the ease of learning, logic, and work flow. However, I do like MongoDB as a web developer because JSON-like objects are very nice to make schema from because I have to work with JavaScript objects anyway for retrieving and displaying data. Adding data for a new user with no collections yet is very easy with a simple call to the insertOne method.
