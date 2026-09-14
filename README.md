# SQL Injection Lab 1: Retrieve Hidden Data

## What the Lab Asked
Find hidden products that aren't normally visible on the website.

## What I Did
I found a filter on the website that shows products by category.
I tested if this filter was vulnerable to SQL injection.

## My Attack
In the category URL, I typed: Gifts' OR '1'='1--

## How It Worked
- The single quote (') broke the original filter
- OR '1'='1 added a condition that's always true
- The double dash (--) removed any other code
- Result: Website showed ALL products including hidden ones

## What I Learned
Websites that don't check user input are vulnerable.
An attacker can manipulate SQL queries using quotes and boolean logic.

## Prevention
- Always validate user input
- Use parameterized queries
- Don't concatenate user input into SQL
