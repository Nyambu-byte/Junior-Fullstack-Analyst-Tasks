1️. Receive request
Parse JSON body

2. Validate required fields
firstName not empty
email not empty
password not empty
If missing → return 400

3. Validate email format
If invalid → return 422

4. Validate password rules
Minimum length
Contains uppercase?
Contains number?
If invalid → return 400

5. Check password = confirmPassword
If not equal → return 400

6. Check if email already exists
Query database:
SELECT * FROM users WHERE email = ?
If exists → return 409

7. Hash password
Use:
bcrypt
Argon2

8. Create user record
Insert into DB:
id
firstName
lastName
email
hashedPassword

9. Return 201 Created
Return userId + status

10. Log action
For auditing
