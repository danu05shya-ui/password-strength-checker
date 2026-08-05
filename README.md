# 🔐 Password Strength Checker

A real-time password strength auditor built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies, runs entirely in the browser.

**[Live Demo](#)** *(add your GitHub Pages link here once enabled)*

## Features

- **Live strength scoring** (0–100) with a Very Weak → Very Strong scale
- **Entropy calculation** in bits, based on character pool size and password length
- **Crack-time estimation** under two attack models: offline (10 billion guesses/sec) and online/throttled (100 guesses/sec)
- **Common password detection** — flags known leaked/breached passwords instantly
- **Pattern detection** — catches repeated characters (`aaa`) and predictable sequences (`123`, `qwerty`)
- **Criteria checklist** for length, uppercase, lowercase, numbers, and special characters
- Fully local — no data ever leaves the browser

## How it works

1. **Criteria checks**: regex tests confirm the presence of uppercase, lowercase, digits, and symbols, and a minimum length of 8 characters.
2. **Entropy math**: `entropy = password length × log2(character pool size)`. This is why length matters more than complexity alone — every extra character multiplies the number of possible combinations.
3. **Penalty layer**: even a password that passes every regex check can be objectively weak if it's a known leaked password or a predictable sequence, so both are checked and penalized separately from the entropy score.

## Tech stack

Pure HTML/CSS/JavaScript — open `password_strength_checker.html` directly in any browser to run it.

## Usage

```bash
git clone https://github.com/yourusername/password-strength-checker.git
cd password-strength-checker
open password_strength_checker.html
```

---
Built as part of the SkillCraft Technology internship.
