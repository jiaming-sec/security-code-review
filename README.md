# 🔐 Security Code Review

This repository contains examples, checklists, and writeups for conducting secure code reviews across multiple languages.

## 🔍 Example Use Cases

- Training junior developers and interns
- Running internal security bootcamps
- Creating Capture The Flag (CTF) challenges
- Practicing secure coding interviews

## 🛠️ Tech Focus

- **Languages:** Python, JavaScript, Java
- **Focus Areas:** Input validation, authentication, session management, access control, cryptography, logging, error handling

## 🧰 Tool Suggestions

- [Semgrep](https://semgrep.dev)
- [Bandit](https://github.com/PyCQA/bandit)
- [SonarQube](https://www.sonarqube.org)
- [FindSecBugs](https://find-sec-bugs.github.io)

## 💡 Resources

Based on the [OWASP Secure Coding Practices](https://owasp.org/www-project-secure-coding-practices-quick-reference-guide/) and [OWASP Code Review Guide](https://owasp.org/www-project-code-review/).

# ✅ OWASP Secure Code Review Checklist

This checklist is designed to guide manual secure code reviews and is aligned with OWASP recommendations.

## 🔐 Authentication

- [ ] Are strong password policies enforced?
- [ ] Is MFA (Multi-Factor Authentication) supported?
- [ ] Are credentials stored securely (e.g., hashed & salted)?

## 🔒 Authorization

- [ ] Are role-based access controls implemented?
- [ ] Is sensitive functionality protected from unauthorized users?
