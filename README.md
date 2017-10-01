# GraphQLCasts
Completed Code Examples from GraphQL with React


To serve fake data - https://github.com/typicode/json-server
npm install -g json-server
npm install --save nodemon
npm run dev
npm run json:server

To access json server:
http://localhost:3000

To access GraphQL:
http://localhost:4000/graphql


Sample query:

{
  user(id: "40"){
    id,
    firstName,
    age,
    company {
      id,
      name
    }
  },
  apple: company(id: "1"){
    ...companyDetails
    users{
      id,
      firstName
    }
  }
}

fragment companyDetails on Company {
  id
  name
  description  
}



Mutations

mutation{
  addUser(firstName: "Stephen", age: 27){
    id
    firstName
    age
  }
}

mutation{
  deleteUser(id: "123"){
    id
    firstName
    age
  }
}

mutation{
  editUser(id: "H1CfKKRo-", age: 27 ){
    id
    firstName
    age    
  }
}
