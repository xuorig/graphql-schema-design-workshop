## Exercise 6.0: Mutations

Our schema allows API clients to fetch data about our store, but does not yet allow them to modify or interact
with our e-commerce platform. In this exercise, we will design a mutation, or a set of mutations that will allow users to:

1. Create a Cart
2. Update a Cart (Adding, Removing Items, Updating the Shipping Address)

```
type Mutation {
  # ...
}
```

*Hint: Don't forget, Domain > Data. The concept also applies to mutations!*

## Exercise 6.1: Mutations

You discover one of the API clients for our application have a special use case. Their cart
page allows users to update their cart all at once. A user might:

  - Add an item
  - Remove an other one
  - Update the shipping Address
  - And click save

Can you think of the GraphQL query or queries needed to do this? Does this change how we designed our schema?

```
query SaveAllTheThings {
  # ...
}
```

## Exercise 6.2: Mutations

Design the mutation "Payload" type for a `addItemToCart` mutation:

```
type Mutation {
  addItemToCart(cartId: ID!, item: Item!, quantity: Int!: AddItemToCartPayload
}

type AddItemToCartPayload {
  ...
}
```

  - How does a client fetch the updated information?
  - How does a client add an error on the quantity field?
  - How does a client know if the mutation succeeded?
