## Exercise 2.0: Use the Schema, Luke!

We are still building an e-commerce API. While looking at our use cases, we realize that it is possible for users to *fetch a product by name*, but our front end application also needs to *fetch products by IDs*, internally. Design a schema that would let the API client do both.

```
type Query {

}

type Mutation {

}
```

# Exercise 2.1:

Products are categorized by what kind of products they are. The categories might be `Entertainment`, `Clothing`, `Food`. Add a field to the product type that would help API users to fetch this category.

```
type Product {
  ...
}
```

# Exercise 2.2:

We're going to add a second mutation to our schema: `applyDiscount`, which takes a discount code and applies it to a cart. One thing though: a discount may apply to shipping costs too or not, and our mutation needs to take account of that. For example, one may apply a discount to the product price only, or apply a discount and apply it to both the product prices and shipping price. Design the mutation field:

```
type Mutation {
  applyDiscount(...)
}
```

# Exercise 2.3

A user of our e-commerce platform can create events for their actual shops. An event might be a halloween sale for example. These events have a `name`, a `description`, a list of `attendees`, and have a start time and end time. Design the type to represent an event:

```
type Event {
  ...
}
```
