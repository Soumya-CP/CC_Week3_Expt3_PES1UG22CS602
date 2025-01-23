# CC-week3-Expt3-PES1UG22CS602
## OPTIMIZATION REASONS:
## REASONS FOR CART
Replaced eval with json.loads: Using eval to parse data is unsafe and can execute arbitrary code, posing a major security risk. Instead, json.loads ensures safe and structured parsing of JSON data.
List comprehension for efficiency: The optimized code uses a single list comprehension to fetch and filter product details, reducing nested loops and making the code more concise and readable.
Error handling in get_product: The optimized code ensures that invalid product IDs (those returning None from get_product) are filtered out, improving robustness and preventing potential runtime errors.
Refactoring with @classmethod for Cart.load: This method uses a more Pythonic approach by directly calling the constructor within a class method, improving reusability and readability.


## REASON FOR BROWSE:
The optimized version uses a list comprehension to transform the list of products returned by dao.list_products() into a list of Product objects. This eliminates the need for an explicit loop and intermediate variables (result).
Why it matters:
Reduces verbosity, making the code easier to read and understand.
Improves performance slightly by avoiding the overhead of repeated append calls.
