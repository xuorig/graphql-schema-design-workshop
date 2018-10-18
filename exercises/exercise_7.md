## Exercise 7: Nullability

Given the following schema IDL, decide which fields should be nullable or not:

```
type Query {
  products(ids: [ID!]): [Product!]!
  cart(id: ID!): Cart! @service("CartService")
}

type Cart {
  id: ID
}

type Product {
  name: String
  description: String
  image: Image! @dbColumn("image_id")
}
```
