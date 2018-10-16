# Exercise 5: Domain Driven > Data Driven

Given this existing `Cart` type, that was generated purely from the underlying implementation, try
to redesign it into something that answers the domain a little better.

```
type Cart {
  discountCodes: [DiscountCode!]!
  products: [Product!]!
  shippingAddress: ShippingAddress
  billingAddress: BillingAddress
  shippingPrice: Float
}

type Product {
  quantity: Int!
  price: Float!
  taxes: Float!
  shippable: Boolean
}

type DiscountCode {
  name: String
  value: Float!
}
```

Hint: As a API user, what do I usually want to do with a cart? (How much is my cart? After or before tax? Can the cart be shipped? Are any discounts applied?, etc)
