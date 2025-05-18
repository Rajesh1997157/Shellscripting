# Shellscripting
#!/bin/bash

# Script to add two numbers

# Prompt user for the first number
echo "Enter the first number: "
read num1

# Prompt user for the second number
echo "Enter the second number: "
read num2

# Check if inputs are valid numbers
if [[ ! $num1 =~ ^[0-9]+(\.[0-9]+)?$ || ! $num2 =~ ^[0-9]+(\.[0-9]+)?$ ]]; then
    echo "Error: Please enter valid numbers."
    exit 1
fi

# Calculate the sum
sum=$(echo "$num1 + $num2" | bc)

# Display the result
echo "The sum of $num1 and $num2 is: $sum"
