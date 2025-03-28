# Secure Code Review Guide

This document outlines how to perform a secure code review focusing on common vulnerabilities and provides examples for both vulnerable and secure implementations.

## 1. Cross-Site Scripting (XSS)

**Vulnerability:**  
Unsanitized user input is directly inserted into HTML, which can allow attackers to inject malicious scripts.

**What to look for:**
- Direct insertion of user input into the output.
- Use of functions like `innerHTML` in JavaScript without proper sanitization.
- Server-side rendering of unsanitized input in templates or views.
