# Discount Calculator 

This is a simple Python program that calculates the final price of an item after applying a discount.  
The discount is only applied if the discount percentage is **20% or higher**.  

---

## Features
- Takes the original price as input.
- Takes the discount percentage as input.
- Applies the discount only if it is **≥ 20%**.
- Displays the final price after discount, or the original price if no discount is applied.

---

## Code Example
```python
def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

original_price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

final_price = calculate_discount(original_price, discount_percent)

if final_price < original_price:
    print(f"The final price after applying the discount is: {final_price:.2f}")
else:
    print(f"No discount applied. The original price is: {original_price:.2f}")
