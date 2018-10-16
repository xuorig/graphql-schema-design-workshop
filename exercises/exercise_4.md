## Exercise 4.0: Static Queries

Given this pseudo code, which builds a query depending on if products should be shown or not, write a GraphQL query
that could achieve the same but in a static way, using GraphQL variables.

HINT: look into the `@include` and `@skip` directives.

```
let fetchProducts = shouldFetchProducts();
let productsFragment = null;

if fetchProducts {
  productsFragment = `
    products { name }
  `
}

query = `
  query {
    shop {
      name
      description
      ${productsFragment}
    }
  }
`

fetch(query)
```
