## Exercise 3.0: Abstract Types

We have just realized that our shopping cart contains `items`, but that an item may either be a `Product`, or a `GiftCard`. Can you
design the cart type for clients to be able to fetch that information?

```
type Cart {
  items: [?]
}
```

## Exercise 3.1: Abstract Types

Our e-commerce platform also supports discounts. A `Cart` has a *list of discounts* that have been applied to it. The problem is that
there are different types of discounts: `DiscountCode`, is a discount that was applied through a code during checkout. `AutomaticDiscount` is a discount added by our application when some conditions are met, and `OwnerDiscount`, which a discount activated by the shop owner for a specific customer.

Can you complete the following IDL so that `discounts` returns an abstract type for these discount types?

```
type AutomaticDiscount {
  value: Money!
  conditions: [DiscountCondition]
}

type DiscountCode {
  value: Money!
  code : String!
}

type OwnerDiscount {
  value: Money!
  reason: String!
}

type Cart {
  discounts: [?]!
}
```

## Exercise 3.2: Abstract Types

While working on these abstract types you notice that your `Product` object, and another `ProductVariant` object (The red version of a t-shirt for example) have a lot of similar fields. You end needing to write resolvers for both of them pretty often. How would you design a schema for a `Product` and `ProductVariant` object that both have a `name`, `description`, and other various fields:

A) Interface

B) Union

C) Just leave them be
