# GraphQL Mesh Issue demo
Demonstrate an error with a REST 'input' query parameter
```bash
npm install
npm start
```
Open the browser and try the following query
```
query MyQuery {
  getRandomFact(max_length: 100) {
    fact
  }
}
```
Then try this query - error returned by mesh before sending the request due to providing a GET request with a body.
```
query MyQuery {
  getRandomFact(input: "abc", max_length: 100) {
    fact
  }
}
```
