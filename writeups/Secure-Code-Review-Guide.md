# Secure Code Review Guide

This document outlines how to perform a secure code review focusing on common vulnerabilities and provides examples for both vulnerable and secure implementations.

## 1. Cross-Site Scripting (XSS)

**Vulnerability:**  
Unsanitized user input is directly inserted into HTML, which can allow attackers to inject malicious scripts.

**What to look for:**
- Direct insertion of user input into the output.
- Use of functions like `innerHTML` in JavaScript without proper sanitization.
- Server-side rendering of unsanitized input in templates or views.

**Examples:**
- **Vulnerable:**
  - Python: [vulnerable-code-samples/python/xss_example.py](../vulnerable-code-samples/python/xss_example.py)
  - JavaScript: [vulnerable-code-samples/javascript/xss_example.html](../vulnerable-code-samples/javascript/xss_example.html)
  - Java (JSP): [vulnerable-code-samples/java/xss_example.jsp](../vulnerable-code-samples/java/xss_example.jsp)
- **Secure:**
  - Python: [secure-code-examples/python/xss_example.py](../secure-code-examples/python/xss_example.py)
  - JavaScript: [secure-code-examples/javascript/xss_example.html](../secure-code-examples/javascript/xss_example.html)
  - Java (JSP): [secure-code-examples/java/xss_example.jsp](../secure-code-examples/java/xss_example.jsp)

## 2. SQL Injection

**Vulnerability:**  
Building SQL queries by concatenating user input can allow attackers to manipulate the database queries.

**What to look for:**
- SQL queries constructed using string concatenation.
- Lack of parameterized queries or prepared statements.

**Examples:**
- **Vulnerable:**
  - Python: [vulnerable-code-samples/python/sql_injection.py](../vulnerable-code-samples/python/sql_injection.py)
  - JavaScript (Node.js): [vulnerable-code-samples/javascript/sql_injection_example.js](../vulnerable-code-samples/javascript/sql_injection_example.js)
  - Java: [vulnerable-code-samples/java/SqlInjectionExample.java](../vulnerable-code-samples/java/SqlInjectionExample.java)
- **Secure:**
  - Python: [secure-code-examples/python/sql_injection.py](../secure-code-examples/python/sql_injection.py)
  - JavaScript (Node.js): [secure-code-examples/javascript/sql_injection_example.js](../secure-code-examples/javascript/sql_injection_example.js)
  - Java: [secure-code-examples/java/SqlInjectionExample.java](../secure-code-examples/java/SqlInjectionExample.java)

## General Secure Code Review Practices

- **Input Validation:**  
  Always validate and sanitize external inputs.

- **Error Handling:**  
  Ensure that errors do not leak sensitive information.

- **Logging:**  
  Confirm that sensitive information is not written to logs.
