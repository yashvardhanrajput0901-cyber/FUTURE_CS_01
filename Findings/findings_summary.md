# Findings Summary

---

## 1. Missing Content Security Policy (CSP)

### Severity
Medium

### Description
The application does not implement a Content Security Policy header.

### Impact
This increases exposure to cross-site scripting (XSS) attacks.

### Recommendation
Implement a strict Content Security Policy restricting untrusted script sources.

---

## 2. Missing X-Frame-Options Header

### Severity
Low

### Description
The application does not include the X-Frame-Options header.

### Impact
Attackers may attempt clickjacking attacks.

### Recommendation
Configure:
X-Frame-Options: DENY

---

## 3. Cookie Security Weakness

### Severity
Medium

### Description
Cookies were observed without strong security attributes.

### Impact
Increases risk of session-based attacks.

### Recommendation
Enable:
- HttpOnly
- Secure
- SameSite flags

---

## 4. Information Disclosure

### Severity
Low

### Description
Publicly accessible information was observed through headers and client-side resources.

### Impact
Attackers may leverage disclosed information during reconnaissance.

### Recommendation
Limit unnecessary information exposure.
