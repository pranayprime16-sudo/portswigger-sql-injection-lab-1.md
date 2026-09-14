# portswigger-sql-injection-lab-1.md
# PortSwigger SQL Injection Lab 1: Retrieve Hidden Data  ## Vulnerability Type SQL Injection (SQLi)  ## Lab Difficulty Easy  ## Objective Retrieve hidden data from the database by manipulating SQL query  ## Vulnerability Found The `category` parameter in the URL is vulnerable to SQL injection.  ## Attack Payload


## How It Works
1. `'` - Closes the original string
2. `OR` - Adds new condition
3. `1'='1` - Always true (returns all data)
4. `--` - Comments out rest of query

## Result
✅ Lab Completed - All products shown including hidden ones

## Key Learning
- Always validate user input
- Never concatenate user input directly into SQL queries
- Use parameterized queries instead

## Prevention
- Use prepared statements
- Input validation
- Least privilege database access
