# Programming Naming Conventions 📝

A comprehensive guide and quick reference for common programming naming conventions, their formats, and typical use cases.

Programming naming cases are standardized conventions used to combine multiple words into a single identifier without spaces. Choosing the correct naming convention improves code readability, adheres to language-specific style guides,and prevents naming collisions.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Naming Cases](#naming-cases)
  - [1. camelCase](#1-camelcase)
  - [2. PascalCase](#2-pascalcase)
  - [3. snake_case](#3-snake_case)
  - [4. SCREAMING_SNAKE_CASE](#4-screaming_snake_case)
  - [5. kebab-case](#5-kebab-case)
  - [6. dot.case](#6-dotcase)
- [Quick Reference Summary](#quick-reference-summary)

---

## Naming Cases

### 1. `camelCase`
* **Format:** Starts with a lowercase letter; each subsequent word begins with a capital letter.
* **Example:** `myVariableName`, `getUserData`, `isLoggedIn`
* **Common Usage:** 
  * Variables and functions in JavaScript, TypeScript, Java, and C#.
  * Property names in JSON objects.

### 2. `PascalCase` (UpperCamelCase)
* **Format:** Capitalizes the first letter of *every* word, including the first.
* **Example:** `MyVariableName`, `UserProfile`, `ButtonComponent`
* **Common Usage:** 
  * Classes, interfaces, types, and enums in languages like C#, Java, TypeScript, and Python.
  * Component names in UI frameworks like React and Angular.

### 3. `snake_case`
* **Format:** Uses all lowercase letters with underscores (`_`) separating words.
* **Example:** `my_variable_name`, `calculate_total_price`, `user_id`
* **Common Usage:** 
  * Variables and functions in Python, Ruby, and PHP.
  * Database table names and column names.
  * Configuration keys in various environments.

### 4. `SCREAMING_SNAKE_CASE` (CONSTANT_CASE)
* **Format:** Uses all uppercase letters with underscores (`_`) separating words.
* **Example:** `MY_VARIABLE_NAME`, `MAX_CONNECTIONS`, `DEFAULT_TIMEOUT`
* **Common Usage:** 
  * Global constants and configuration constants.
  * Environment variables (e.g., `DATABASE_URL`, `API_KEY`).

### 5. `kebab-case` (dash-case)
* **Format:** Uses all lowercase letters with hyphens (`-`) separating words.
* **Example:** `my-variable-name`, `main-content-container`
* **Common Usage:** 
  * URLs and routing paths (e.g., `/user-profile/settings`).
  * CSS classes and HTML attributes (`class="btn-primary"`).
  * Package and repository names (e.g., npm packages like `lodash-es`).

### 6. `dot.case`
* **Format:** Uses lowercase letters with periods (`.`) separating words.
* **Example:** `my.variable.name`, `app.config.port`
* **Common Usage:** 
  * Configuration file keys (e.g., properties files, YAML, JSON configs).
  * Namespaces and property paths in logging or state management.

---

## ⚡ Quick Reference Summary

| Naming Case | Example Format | Typical Use Cases |
| :--- | :--- | :--- |
| **`camelCase`** | `myVariableName` | JS/TS variables & functions, Java/C# methods |
| **`PascalCase`** | `MyVariableName` | Classes, Interfaces, React/UI Components |
| **`snake_case`** | `my_variable_name` | Python variables, Database columns |
| **`SCREAMING_SNAKE`**| `MY_VARIABLE_NAME` | Global constants, Environment variables |
| **`kebab-case`** | `my-variable-name` | URLs, CSS classes, Package names |
| **`dot.case`** | `my.variable.name` | Configuration files, Namespaces |

---

## 💡 Best Practices
* **Consistency is Key:** Stick to the established convention of the codebase or language style guide you are working with.
* **Avoid Mixing:** Do not mix multiple conventions haphazardly within the same scope unless required by external tools (e.g., mapping camelCase JSON API fields to snake_case database columns).