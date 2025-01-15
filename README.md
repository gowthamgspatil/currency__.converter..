# currency__.converter..

This script is a currency conversion program written in Python. It takes an amount in one currency, converts it into another currency, and displays the result.


### **1. `get_amount()` Function**

- **Purpose**: To validate and get the amount to be converted.
- **Process**:
  - The user is prompted to enter an amount.
  - The input is converted to a float.
  - If the amount is not a positive number, a `ValueError` is raised.
  - If the input is valid, it is returned. Otherwise, the user is prompted again.
- **Why a loop**: Ensures the user enters a valid numeric value greater than 0.

---

### **2. `get_currency(label)` Function**

- **Purpose**: To validate and get the source or target currency.
- **Parameters**:
  - `label`: A string that indicates whether it's the source or target currency being requested.
- **Process**:
  - The user is asked to input a currency code (USD, EUR, CAD).
  - The input is converted to uppercase for consistency.
  - If the input is not in the list of allowed currencies (`currencies` tuple), the user is prompted again.

---

### **3. `convert(amount, source_currency, target_currency)` Function**

- **Purpose**: To calculate the converted amount between the source and target currencies.
- **Parameters**:
  - `amount`: The numeric value to convert.
  - `source_currency`: The currency of the amount.
  - `target_currency`: The desired currency after conversion.
- **Process**:
  - A dictionary `exchange_rates` stores the conversion rates between currencies.
  - If the `source_currency` and `target_currency` are the same, the function returns the original amount.
  - Otherwise, the function uses the exchange rate to calculate the converted amount:  
    \( \text{converted amount} = \text{amount} \times \text{exchange rate} \).

---

### **4. `main()` Function**

- **Purpose**: The main workflow of the program.
- **Process**:
  - Calls `get_amount()` to get a valid amount.
  - Calls `get_currency()` twice to get the source and target currencies.
  - Calls `convert()` to calculate the converted amount.
  - Displays the result to the user in a formatted string showing two decimal places.

---

### **5. The `if __name__ == "__main__":` Block**

- Ensures the `main()` function is only executed when the script is run directly, not when it's imported as a module in another script.

