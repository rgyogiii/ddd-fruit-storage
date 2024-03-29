# Fruit Storage System
> A system to do a crud operations using Domain Driven Design approach
> 
[![LinkedIn](https://img.shields.io/static/v1?label=&message=LinkedIn&color=%230A66C2&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/romar-george-doinog)

## Built With

[![node - v20.9.0](https://img.shields.io/static/v1?label=node&message=v20.9.0&color=2ea44f&logo=nodedotjs)](https://nodejs.org/en/blog/release/v20.9.0)
[![npm - 8.19.3](https://img.shields.io/badge/npm-8.19.3-CB3837?logo=npm&logoColor=%23CB3837)](https://nodejs.org/en/blog/release/v20.9.0)
[![mongoosejs - 8.1.1](https://img.shields.io/static/v1?label=mongoosejs&message=8.1.1&color=%23880000&logo=mongoose&logoColor=%23880000)](https://mongoosejs.com/)
[![GraphQL](https://img.shields.io/static/v1?label=&message=GraphQL&color=%23E10098&logo=graphql&logoColor=white)](https://mongoosejs.com/)
[![MongoDB](https://img.shields.io/static/v1?label=&message=MongoDB&color=%2347A248&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![jest](https://jestjs.io/img/jest-badge.svg)](https://github.com/jestjs/jest)

## Prerequisites

Before you begin, ensure you have met the following requirements:

* You have `MongoDB` installed on your machine
* You have installed the latest `node` and `npm` verions

## Getting started

```sh
# Clone this repository
$ git clone https://github.com/georgeromarrr/ddd-fruit-storage.git

# Install dependencies
$ npm install

# Run the app development
$ npm run dev

# Run the app
$ npm start

# Run the test
$ npm test
```

## Development

Still under development

```sh
# to check cron job functionalities
$ git branch cronjob_dev

# run the app development
$ npm run dev
```

## Using GraphQL

To interact with the API, use these queries and mutations:

* GetFruitStorage

```
query GetFruitStorage {
  getFruitStorage {
    status
    message
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
  }
}
```

* FindFruit

```
query FindFruit($name: String!) {
  findFruit(name: $name) {
    status
    message
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
  }
}
```

* CreateFruit

```
mutation CreateFruitForFruitStorage($name: String!, $description: String, $limitOfFruitToBeStored: Int) {
  createFruitForFruitStorage(name: $name, description: $description, limitOfFruitToBeStored: $limitOfFruitToBeStored) {
    status
    message
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
 
  }
}
```
* StoreFruit

```
mutation StoreFruitToFruitStorage($name: String!, $amount: Int) {
  storeFruitToFruitStorage(name: $name, amount: $amount) {
    status
    message
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
  }
}
```
* RemoveFruit

```
mutation RemoveFruitFromFruitStorage($name: String!, $amount: Int) {
  removeFruitFromFruitStorage(name: $name, amount: $amount) {
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
    message
    status
  }
}
```
* UpdateFruit

```
mutation UpdateFruitForFruitStorage($name: String!, $description: String, $limitOfFruitToBeStored: Int) {
  updateFruitForFruitStorage(name: $name, description: $description, limitOfFruitToBeStored: $limitOfFruitToBeStored) {
    status
    message
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
  }
}
```
* DeleteFruit

```
mutation DeleteFruitFromFruitStorage($name: String!, $forceDelete: Boolean) {
  deleteFruitFromFruitStorage(name: $name, forceDelete: $forceDelete) {
    status
    message
    data {
      id
      name
      description
      amount
      limitOfFruitToBeStored
    }
  }
}
```


<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[jest-image]: https://jestjs.io/img/jest-badge.svg
[jest-url]: https://github.com/jestjs/jest
[linkedin-image]: https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki
