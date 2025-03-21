# Advanced-Stock-billing-system
### Variables
SKU_number: List to store the SKU numbers of products.

product: List to store the names of products.

price: List to store the price of each product.

Quantity: List to store the quantity of each product..

gst_rate: Variable to store the GST rate, initialized to 0.

discount_rate: Variable to store the percentage discount rate, initialized to 0.

fixed_discount: Variable to store a fixed amount discount, initialized to 0.

product_discounts: Dictionary to store the discount percentage for specific products.

## Function Details
### add_product():
Purpose: This function allows the user to add multiple products to the lists.

Prompts the user to enter the number of products they want to add (size).

For each product, prompts the user to enter:

sku: Unique SKU number.

prod: Product name.

qty: Quantity of the product.

prc: Unit price of the product.

Appends these values to SKU_number, product, Quantity, and price lists respectively.

Allows the user to continue adding products until they decide to stop by entering 'N'.

### view_products():
Purpose: This function allows the user to add multiple products to the lists.

Iterates through the SKU_number list.

Prints the product ID, product name, quantity, and unit price for each product.

### remove_product():
Purpose: This function allows the user to remove a product from the lists.

Prompts the user to enter a product ID to remove.

Checks if the entered ID exists in the SKU_number list.

If found, removes the product from SKU_number, product, Quantity, and price lists and prints a success message.

If not found, prints an error message.

### GST():
Purpose: This function allows the user to set the GST rate.

Prompts the user to enter the GST rate.

Updates the gst_rate variable with the entered value.

Prints a confirmation message.

### apply_discount():
Purpose: This function allows the user to apply discounts.

Prompts the user to select a discount type:

1: Percentage discount on the total bill.

2: Fixed amount discount on the total bill.

3: Discount on specific products.

Based on the user selection:

If 1, prompts for the discount rate and updates discount_rate.

If 2, prompts for the fixed discount amount and updates fixed_discount.

If 3, prompts for the product ID and discount percentage, updates product_discounts dictionary.

Prints a confirmation message for the selected discount type.

### Generate_invoice():
Purpose: This function calculates and prints the final invoice.

Prints a separator line for readability.

Initializes total_price to 0.

Iterates through each product:

Retrieves the original price and quantity.

Calculates the discount amount and discounted price for the product.

Adds the discounted price multiplied by quantity to total_price.

Calculates the total discount amount by applying the percentage discount and fixed discount.

Reduces total_price by the total discount amount.

Calculates the GST amount on the total discounted price.

Calculates the final total price by adding the GST amount.

Prints the invoice details including product information, GST amount, discount amount, and final total price.

### Main Program Loop
Purpose: This loop continuously prompts the user for actions until they choose to exit.
Displays a menu of options for the user to:

#### Add a new product.

#### View all products.

#### Remove a product.

#### Apply GST.

#### Apply discounts.

#### Generate and view the final invoice.

Executes the corresponding function based on the user's input.

Asks the user if they want to continue or exit the program.
