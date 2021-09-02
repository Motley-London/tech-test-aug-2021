# tech-test-aug-2021
Motley's Technical Test for https://angel.co/l/2vJv6g

The technical test will mainly happen via a (virtual) face-to-face. The various parts of the test are descirbed below; some of which will require work prior to the actual interview.

## Part 1

Write a function in Javascript that takes csv data (as a string) and parses it into an array of objects. The keys for the objects should be taken from the header line in the csv file (i.e. don't assume you know the keys beforehand). And you can assume that all the values are strings. If a value is missing, use an empty string for the output.

For example, the input:

```
product, price, review, in_stock
Gold Romeo Square Hoops, 85.00, Stunning! I love them., true,
Gold Siren Hoops, 110.00, , false,
Half Moon Pearl Earrings, 70.00, Delightful! Dressy without being garish., true
```

would return the array:

```
[
    {
        "product": "Gold Romeo Square Hoops",
        "price": "85.00",
        "review": "Stunning! I love them.",
        "in_stock": "true"
    },
    {
        "product": "Gold Siren Hoops",
        "price": "110.00",
        "review": "",
        "in_stock": "false"
    },
    {
        "product": "Half Moon Pearl Earrings",
        "price": "70.00",
        "review": "Delightful! Dressy without being garish.",
        "in_stock": "true"
    }
]
```

We'll review your code during the interview, but you don't need to send it beforehand.

## Part 2

This part doesn't require you to write any code. It's just about describing a solution during the tech interview.

At Motley, we work with multiple designers who are individually paid commission based on the sales of their designs. All products are sold via a Shopify store-front at motley-london.com. Currently, we use the Shopify API to automate the commission calculation. This part of the technical test will require you to describe how you'd write a function to calculate the commission. The biggest part of this is reading through the Shopify API documentation, and figuring out what API calls will be needed, and how to use the returned data to calculate the commission.

Some specifics:

- Every product has a single designer
- The commission for each designer is calculated as a fixed percentage of the total orders of the products they designed
- Assuming you can identify which designer a product belongs to via the product id
- Commission is calculated each quarter
- Discounts and Refunds need to be accounted for
- You can ignore tax

## Part 3

This part will be a pair programming exercise, where we'll build a small UI component together. We'll start with some boilerplate, and fill in the rest. We'll be using React.js. There isn't anything to prepare for this part.

## Part 4

For the final part, we'll ask you to describe how the Javascript event loop works, and how it relates to Promises and async functions.
