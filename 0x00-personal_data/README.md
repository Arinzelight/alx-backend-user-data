# 0x00. Personal Data

## Learning Objectives

- Examples of Personally Identifiable Information (PII)
- Implementation of a log filter to obfuscate PII fields
- Password encryption and validation techniques
- Database authentication using environment variables

## Personally Identifiable Information (PII)

Personally Identifiable Information (PII) refers to any data that could potentially identify a specific individual. Examples of PII include but are not limited to:
- Full name
- Social Security number
- Date and place of birth
- Address
- Phone number
- Email address
- Biometric data
- IP address

## Implementing a Log Filter for PII Obfuscation

When logging sensitive information that includes PII, it's crucial to obfuscate or mask such data to prevent unauthorized access. Here are some steps to implement a log filter for PII obfuscation:
1. Identify PII fields in the log data.
2. Implement a filter function to replace PII fields with placeholders or obfuscated values.
3. Apply the filter to log entries containing PII before writing them to the log.

## Password Encryption and Validation

To ensure the security of user passwords, encryption and validation techniques should be implemented. Here's a basic outline:
1. Encrypt passwords using a strong hashing algorithm like bcrypt or Argon2.
2. Store only the hashed passwords in the database.
3. When a user attempts to log in, hash the input password and compare it with the stored hash for authentication.

## Database Authentication Using Environment Variables

Storing sensitive information like database credentials directly in code poses security risks. Instead, use environment variables for database authentication:
1. Set environment variables for database credentials (e.g., DB_HOST, DB_USER, DB_PASSWORD).
2. Access these variables within your application code to establish a secure connection to the database.
3. Ensure that environment variables are kept confidential and are not exposed in version control or shared publicly.

Remember, handling personal data requires strict adherence to data protection regulations such as GDPR (General Data Protection Regulation) and HIPAA (Health Insurance Portability and Accountability Act), depending on the context and jurisdiction.

## Additional Resources

- [OWASP Data Validation Cheat Sheet](https://owasp.org/www-project-cheat-sheets/cheatsheets/Data_Validation_Cheat_Sheet)
- [bcrypt](https://en.wikipedia.org/wiki/Bcrypt)
- [Argon2](https://en.wikipedia.org/wiki/Argon2)
- [OWASP Secure Coding Practices](https://owasp.org/www-project-secure-coding-practices/)
- [GDPR Official Website](https://gdpr.eu/)
- [HIPAA Official Website](https://www.hhs.gov/hipaa/index.html)


