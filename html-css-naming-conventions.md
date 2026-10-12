# HTML, CSS, and JavaScript Naming Conventions: The Complete Guide

In software development and web engineering, naming conventions establish a predictable, standardized pattern for identifiers such as variables, functions, classes, components, selectors, and constants. 

This guide provides an exhaustive reference for the core casing conventions: **camelCase**, **PascalCase**, **snake_case**, **kebab-case**, and **CONSTANT_CASE** (also known as **UPPER_SNAKE_CASE** or **SCREAMING_SNAKE_CASE**). It explores how they apply across HTML, CSS, JavaScript, Python, and SQL, details the technical mechanics behind why specific languages favor specific styles, and highlights practical best practices and common pitfalls.

---

## Table of Contents

1. [Introduction to Naming Conventions](#1-introduction-to-naming-conventions)
2. [Why Naming Conventions Matter](#2-why-naming-conventions-matter)
3. [Naming Cases Comparison Table](#3-naming-cases-comparison-table)
4. [The Five Core Naming Cases](#4-the-five-core-naming-cases)
   - [4.1 camelCase](#41-camelcase)
   - [4.2 PascalCase](#42-pascalcase)
   - [4.3 snake_case](#43-snake_case)
   - [4.4 kebab-case](#44-kebab-case)
   - [4.5 CONSTANT_CASE (UPPER_SNAKE_CASE / SCREAMING_SNAKE_CASE)](#45-constant_case-upper_snake_case--screaming_snake_case)
5. [Understanding HTML & CSS Selectors and Custom Properties](#5-understanding-html--css-selectors-and-custom-properties)
6. [Differences Between HTML/CSS and JavaScript Naming](#6-differences-between-htmlcss-and-javascript-naming)
7. [Integrated Real-World Examples](#7-integrated-real-world-examples)
   - [7.1 HTML Implementation (`index.html`)](#71-html-implementation-indexhtml)
   - [7.2 CSS Implementation (`styles.css`)](#72-css-implementation-stylescss)
   - [7.3 JavaScript Implementation (`app.js`)](#73-javascript-implementation-appjs)
   - [7.4 Expected Output](#74-expected-output)
8. [Common Beginner Mistakes and How to Fix Them](#8-common-beginner-mistakes-and-how-to-fix-them)
9. [Best Practices for Long-Term Consistency](#9-best-practices-for-long-term-consistency)
10. [Quick-Reference Summary Table](#10-quick-reference-summary-table)

---

## 1. Introduction to Naming Conventions

### What Is a Naming Convention?

A **naming convention** is an agreed-upon set of rules and guidelines for choosing the character sequences used to identify variables, types, functions, files, styling selectors, and other entities in source code and markup.

### Conventions vs. Syntax Rules

It is vital to distinguish between a **convention** and a **syntax rule**:

* **Syntax Rules (Hard Rules):** Imposed by the programming language's compiler or interpreter. Violating a syntax rule causes a compile-time or runtime error. For example, in JavaScript, an identifier cannot start with a digit (`let 1user = "Ada";` is illegal) and cannot contain hyphens (`let user-name = "Ada";` is parsed as subtraction, causing a syntax or reference error).
* **Naming Conventions (Soft Rules):** Agreed upon by the community, language authors, or project maintainers. Violating a convention rarely crashes the program, but it harms readability and breaks ecosystem tooling. For example, writing `let User_Name = "Ada";` in JavaScript is valid syntax, but it violates JavaScript community conventions.

Naming conventions exist to bridge human cognition with machine execution, creating predictability across disparate modules, libraries, and languages.

---

## 2. Why Naming Conventions Matter

Establishing and adhering to naming conventions provides several concrete benefits:

1. **Enhanced Readability and Comprehension:** Code is read far more often than it is written. Predictable casings allow developers to instantly recognize whether an identifier is a class constructor, a private variable, a component, or a global constant without reading its implementation.
2. **Reduced Cognitive Load:** When team members agree on naming rules, time is not wasted debating whether an API endpoint, CSS class, or variable should use underscores or hyphens.
3. **Prevention of Silent Bugs:** In frameworks like React, casing dictates functionality: `<button />` renders a standard HTML button, whereas `<Button />` instantiates a custom React component. In CSS, class selectors are case-sensitive depending on the document mode.
4. **Tooling and Linter Interoperability:** Modern development environments rely on automated tools (ESLint, Prettier, Stylelint, TypeScript). Inconsistent casing triggers lint warnings, breaks automated code refactoring, and degrades IDE autocomplete suggestions.
5. **Seamless Cross-Language Interoperability:** A full-stack application often connects HTML/CSS templates, JavaScript/TypeScript frontends, Python or Node backends, and SQL relational databases. Knowing the standard conventions for each layer minimizes translation friction.

---

## 3. Naming Cases Comparison Table

The following table summarizes the five primary casing styles:

| Case Style | Common Name(s) | Word Separator | Capitalization Rule | Typical Use Cases | Quick Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **camelCase** | Lower camel case, dromedaryCase | None (casing transition) | First word lowercase; all subsequent words capitalized | JavaScript/TypeScript variables, functions, methods, object properties, JSX attributes | `userProfileCard` |
| **PascalCase** | Upper camel case, StudlyCaps | None (casing transition) | Every word capitalized (including the first word) | Classes (JS/TS/Python), React/Vue/Svelte components, TypeScript types/interfaces | `UserProfileCard` |
| **snake_case** | Pothole case, underscore_case | Underscore (`_`) | All lowercase characters separated by underscores | Python variables and functions, SQL tables and columns, REST API response keys | `user_profile_card` |
| **kebab-case** | Dash-case, spinal-case, lisp-case | Hyphen (`-`) | All lowercase characters separated by hyphens | HTML classes, HTML IDs, HTML `data-*` attributes, CSS selectors, CSS custom properties, URL slugs | `user-profile-card` |
| **CONSTANT_CASE** / **UPPER_SNAKE_CASE** | SCREAMING_SNAKE_CASE, Constant Case, Macro Case | Underscore (`_`) | All uppercase characters separated by underscores | Application constants, configuration settings, environment variables | `USER_PROFILE_CARD` |

---

## 4. The Five Core Naming Cases

### 4.1 camelCase

#### Definition & Mechanism
`camelCase` concatenates multiple words without spaces, punctuation, or hyphens. The very first word is entirely lowercase, while the initial letter of every subsequent word is capitalized. The visual peaks created by the uppercase letters resemble the humps of a camel.

#### Naming Rules
1. The first letter must be lowercase (e.g., `user`, not `User`).
2. Subsequent words must begin with a capital letter (e.g., `userAccount`).
3. No spaces, underscores, or hyphens may be used.
4. Digits can be used, but cannot start the identifier.
5. Acronyms are typically normalized (e.g., `fetchHttpData` or `fetchXmlRequest` rather than `fetchHTTPData`).

#### Five Clear Examples
1. `userName`
2. `getUserProfile`
3. `isAuthenticated`
4. `shoppingCartTotal`
5. `handleFormSubmit`

#### Where It Is Commonly Used
* **JavaScript / TypeScript:** Variables (`let`, `const`, `var`), functions, class methods, object properties.
* **JSX / React:** Component props and event handler attributes (e.g., `className`, `onClick`, `tabIndex`, `autoFocus`).
* **Java, C#, Swift:** Variables, methods, and parameters.

#### Code Snippets & Language Examples

```javascript
// Variable declarations
let currentCartTotal = 149.99;
const isUserLoggedIn = true;

// Object literal properties
const userProfile = {
  firstName: "Alex",
  lastName: "Morgan",
  accountStatus: "active",
  
  // Method definition
  calculateDiscount(loyaltyPoints) {
    return loyaltyPoints * 0.05;
  }
};

// Function declaration
function fetchOrderHistory(userId, maxResults) {
  return `/api/users/${userId}/orders?limit=${maxResults}`;
}
```

In React and JSX, attributes must use camelCase to mirror the JavaScript DOM properties rather than raw HTML attribute names:

```javascript
// React / JSX Example
function PrimaryButton(props) {
  return (
    <button
      className="btn-primary"
      onClick={props.onUserClick}
      aria-label="Submit Form"
      tabIndex={0}
    >
      {props.buttonText}
    </button>
  );
}
```

#### Correct vs. Incorrect Examples

| Status | Identifier | Explanation |
| :--- | :--- | :--- |
| **Correct** | `totalScore` | First word lowercase, second capitalized. |
| **Incorrect** | `TotalScore` | Starts with uppercase; this is PascalCase. |
| **Incorrect** | `total_score` | Uses underscore; this is snake_case. |
| **Incorrect** | `total-score` | Uses hyphen; in JavaScript, this is interpreted as `total minus score`. |
| **Incorrect** | `totalscore` | Words run together; poor readability. |

#### Common Beginner Mistakes
* **Using hyphens:** Writing `let user-id = 5;` causes a JavaScript `SyntaxError` or `ReferenceError` because `-` is the subtraction operator.
* **Capitalizing the first letter:** Naming a standard variable or function `function GetUser()` confuses developers into thinking it is a constructor or React component.
* **Inconsistent acronym casing:** Mixing styles like `parseJSONString` and `parseJsonString` within the same codebase. Pick one rule (e.g., treating acronyms as standard words: `parseJsonString`) and apply it consistently.

---

### 4.2 PascalCase

#### Definition & Mechanism
`PascalCase` (named after the Pascal programming language) concatenates words without spaces or punctuation, capitalizing the first letter of **every** word, including the first word.

#### Naming Rules
1. Every word begins with an uppercase letter.
2. All other letters in each word are lowercase.
3. No spaces, hyphens, or underscores are permitted.
4. Acronyms are either fully capitalized or treated as single words (e.g., `HttpServer` or `HTTPServer`).

#### Five Clear Examples
1. `UserProfileCard`
2. `NavigationMenu`
3. `ShoppingCart`
4. `PaymentProcessor`
5. `DatabaseConnectionPool`

#### Where It Is Commonly Used
* **React / React Native:** Component names (functional and class-based).
* **JavaScript / TypeScript:** Class declarations, TypeScript `type` aliases, `interface` definitions, and `enum` names.
* **C# / .NET:** Class names, namespace names, and public method names.
* **Python:** Class declarations (per PEP 8 guidelines).

#### Code Snippets & Language Examples

```javascript
// JavaScript Class
class ShoppingCart {
  constructor(ownerId) {
    this.ownerId = ownerId;
    this.items = [];
  }

  addItem(item) {
    this.items.push(item);
  }
}

const customerCart = new ShoppingCart("usr_981");
```

```javascript
// React Component (Functional)
function NavigationBar({ brandTitle, userSession }) {
  return (
    <header className="main-navigation">
      <h1 className="brand-logo">{brandTitle}</h1>
      <span className="session-status">{userSession.status}</span>
    </header>
  );
}
```

> [!IMPORTANT]
> **Why React Requires PascalCase for Components:**
> In JSX, the React compiler distinguishes built-in HTML elements from custom components based on the casing of the first letter:
> * `<header>` is compiled to `React.createElement('header')` (an HTML DOM tag).
> * `<Header>` is compiled to `React.createElement(Header)` (a reference to a custom JavaScript function or class).
> If you name a custom component `function userAvatar()`, JSX will treat `<userAvatar />` as an unknown HTML element rather than executing your component.

#### Correct vs. Incorrect Examples

| Status | Identifier | Explanation |
| :--- | :--- | :--- |
| **Correct** | `UserProfile` | Both words capitalized. |
| **Incorrect** | `userProfile` | First word lowercase; this is camelCase. |
| **Incorrect** | `User_Profile` | Contains an underscore; violates PascalCase rules. |
| **Incorrect** | `USERPROFILE` | All caps; violates PascalCase and looks like a constant. |

#### Common Beginner Mistakes
* **Naming React components in camelCase:** Defining `function productCard()` and writing `<productCard />` produces an empty or broken DOM output.
* **Using PascalCase for instance variables:** Writing `const NewUser = new User();` instead of `const newUser = new User();` leads developers to treat `NewUser` as a class rather than an object instance.

---

### 4.3 snake_case

#### Definition & Mechanism
`snake_case` separates words using a single underscore character (`_`). All characters are lowercase. The text remains horizontal and flat, resembling a snake crawling along the baseline.

#### Naming Rules
1. All letters must be lowercase.
2. Words are separated by exactly one underscore (`_`).
3. No uppercase characters or hyphens are permitted.
4. Leading or trailing underscores typically denote special conventions (e.g., Python private members or dunder methods) and should not be used for regular variable names.

#### Five Clear Examples
1. `user_id`
2. `created_at`
3. `order_total_amount`
4. `calculate_tax`
5. `is_authenticated`

#### Where It Is Commonly Used
* **Python:** Variable names, function names, module names, and method names (mandated by PEP 8).
* **SQL:** Database table names, column names, view names, and stored procedure identifiers.
* **REST APIs:** JSON keys in many backend frameworks (Django REST Framework, Ruby on Rails, Flask).
* **Rust & C:** Standard function and variable naming conventions.

#### Code Snippets & Language Examples

```python
# Python variable and function declarations (PEP 8)
def calculate_shipping_cost(package_weight_kg: float, is_express_delivery: bool) -> float:
    base_rate = 5.50
    weight_multiplier = 1.25
    express_surcharge = 10.00
    
    total_cost = base_rate + (package_weight_kg * weight_multiplier)
    
    if is_express_delivery:
        total_cost += express_surcharge
        
    return total_cost

# Usage
customer_package_weight = 4.2
final_shipping_fee = calculate_shipping_cost(customer_package_weight, True)
print(f"Shipping fee: ${final_shipping_fee:.2f}")
```

```sql
-- Relational Database Schema (SQL)
CREATE TABLE customer_orders (
    order_id INT PRIMARY KEY AUTO_INCREMENT,
    customer_id INT NOT NULL,
    order_status VARCHAR(50) NOT NULL,
    shipping_address TEXT NOT NULL,
    total_amount DECIMAL(10, 2) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    CONSTRAINT fk_customer FOREIGN KEY (customer_id) REFERENCES customers(id)
);
```

#### Correct vs. Incorrect Examples

| Status | Identifier | Explanation |
| :--- | :--- | :--- |
| **Correct** | `shipping_rate` | All lowercase, words separated by an underscore. |
| **Incorrect** | `shippingRate` | camelCase; violates Python PEP 8 conventions for functions and variables. |
| **Incorrect** | `Shipping_Rate` | Pascal_Snake_Case; mixed casings should be avoided. |
| **Incorrect** | `shipping-rate` | kebab-case; causes syntax errors in Python and SQL (treated as subtraction). |
| **Incorrect** | `shipping__rate` | Double underscores denote special language mechanics or ORM filters. |

#### Common Beginner Mistakes
* **Using hyphens in Python or SQL:** Writing `SELECT customer-id FROM orders` or `item-count = 10` causes syntax errors because `-` is parsed as arithmetic subtraction.
* **Accidental double underscores in Python:** Writing `__variable__` triggers Python's special name mangling and dunder attribute protocols, which are reserved for language internals (like `__init__` or `__str__`).

---

### 4.4 kebab-case

#### Definition & Mechanism
`kebab-case` separates words with a hyphen (`-`). All letters are lowercase. The visual line passing horizontally through the center of the words resembles food items pierced by a kebab skewer.

#### Naming Rules
1. All letters must be lowercase.
2. Words are separated by a single hyphen (`-`).
3. No spaces, underscores, or uppercase letters are permitted.
4. CSS custom properties (variables) begin with a double hyphen prefix (e.g., `--brand-primary`).

#### Five Clear Examples
1. `site-header`
2. `btn-primary`
3. `card-body-text`
4. `--main-accent-color`
5. `data-user-role`

#### Where It Is Commonly Used
* **HTML:** Class names, ID names, custom data attributes (`data-*`), custom element tags (`<user-profile-badge>`).
* **CSS:** Class selectors (`.btn-primary`), ID selectors (`#site-header`), CSS custom properties (`--primary-color`), and standard CSS properties (`font-size`, `background-color`, `border-radius`).
* **URLs & URIs:** Clean website URLs and REST slugs (e.g., `https://example.com/posts/getting-started-with-css`).
* **Package Names:** `package.json` package names (e.g., `react-router-dom`, `body-parser`).

#### Code Snippets & Language Examples

```html
<!-- HTML structure utilizing kebab-case -->
<section id="hero-banner" class="hero-section dark-theme" data-analytics-category="homepage-hero">
  <div class="hero-content-wrapper">
    <h1 class="hero-title">Welcome to Our Platform</h1>
    <p class="hero-description">Discover tools engineered for modern developers.</p>
    <button type="button" class="btn btn-call-to-action" data-action-trigger="signup-modal">
      Get Started
    </button>
  </div>
</section>
```

```css
/* CSS stylesheet styling the kebab-case selectors */
:root {
  --primary-accent-color: #2563eb;
  --secondary-bg-color: #1e293b;
  --base-spacing-unit: 1rem;
}

#hero-banner {
  background-color: var(--secondary-bg-color);
  padding: calc(var(--base-spacing-unit) * 2);
}

.hero-section.dark-theme {
  color: #ffffff;
}

.hero-content-wrapper {
  max-width: 1200px;
  margin: 0 auto;
}

.btn-call-to-action {
  background-color: var(--primary-accent-color);
  border: none;
  border-radius: 4px;
  padding: 0.75rem 1.5rem;
  color: #ffffff;
  cursor: pointer;
}
```

#### Correct vs. Incorrect Examples

| Status | Identifier | Explanation |
| :--- | :--- | :--- |
| **Correct** | `nav-item-active` | Lowercase characters cleanly separated by hyphens. |
| **Incorrect** | `navItemActive` | camelCase; while legal in HTML/CSS, it is non-standard and error-prone. |
| **Incorrect** | `nav_item_active` | snake_case; non-idiomatic for HTML/CSS classes. |
| **Incorrect** | `Nav-Item-Active` | Mixed uppercase letters in CSS can cause selector matching issues. |

#### Common Beginner Mistakes
* **Using dot notation in JavaScript for kebab-case attributes:** Trying to access `element.dataset.user-role` causes a syntax error. JavaScript maps kebab-case dataset attributes to camelCase: `element.dataset.userRole`.
* **Writing JavaScript identifiers in kebab-case:** Writing `const card-title = document.querySelector('.card-title');` will fail immediately with `SyntaxError: Unexpected token '-'`.

---

### 4.5 CONSTANT_CASE (UPPER_SNAKE_CASE / SCREAMING_SNAKE_CASE)

#### Definition & Mechanism
`CONSTANT_CASE` (also known as `UPPER_SNAKE_CASE`, `SCREAMING_SNAKE_CASE`, or `MACRO_CASE`) formats text entirely in uppercase letters with words separated by an underscore (`_`). In software engineering utilities (such as npm's `change-case` library and standard linter configurations), this pattern is officially termed **Constant Case**.

The naming convention signals to developers that an identifier holds an author-time, immutable, or globally static configuration value whose value should remain constant throughout program execution.

#### Naming Rules
1. Every letter must be uppercase.
2. Words are separated by exactly one underscore (`_`).
3. Digits are permitted but cannot start the identifier (e.g., `OAUTH2_CLIENT_ID`).
4. No lowercase characters or hyphens are permitted.
5. Acronyms remain fully capitalized without internal separators (e.g., `HTTP_STATUS_OK`, `JSON_PAYLOAD_LIMIT`).

#### Five Clear Examples
1. `API_BASE_URL`
2. `MAX_RETRY_ATTEMPTS`
3. `DEFAULT_TIMEOUT_MS`
4. `DATABASE_PORT`
5. `AUTH_SECRET_KEY`

#### When to Use CONSTANT_CASE vs. Regular camelCase `const`
One of the most frequent points of confusion in JavaScript and TypeScript is distinguishing between a variable declared with `const` and an identifier formatted in `CONSTANT_CASE`:

* **Use CONSTANT_CASE for Author-Time, Static Values:**
  Values that are known before the program runs and never change during execution (e.g., mathematical constants, fixed timeouts, API hostnames, predefined error codes, action types, or status dictionaries).
* **Use camelCase for Runtime `const` Variables:**
  Variables declared with `const` that store values computed at runtime, function parameters, or DOM node references (e.g., `const userAge = calculateAge(dob);`, `const submitBtn = document.querySelector("#btn-submit");`). These are non-reassignable bindings, but they represent dynamic execution state rather than global constants.

#### Where It Is Commonly Used
* **JavaScript / TypeScript:** Global configuration constants, frozen enum-like dictionaries (`Object.freeze()`), state management action types (e.g., Redux action strings), and TypeScript literal types.
* **Node.js & Backend Services:** Environment variable mappings (`process.env.PORT`), server settings.
* **Python:** Module-level constants (as prescribed by PEP 8).
* **Environment Files (`.env`):** Configuration keys, database secrets, and runtime flags.
* **C / C++:** Preprocessor macros and constants (`#define BUFFER_SIZE 1024`).

#### Code Snippets & Language Examples

```javascript
// 1. Author-Time Global Configuration Constants
const API_BASE_URL = "https://api.example.com/v1";
const MAX_LOGIN_ATTEMPTS = 5;
const SESSION_TIMEOUT_MS = 15 * 60 * 1000; // 15 minutes

// 2. Frozen Constant Dictionary / Enum Pattern
const HTTP_STATUS = Object.freeze({
  OK: 200,
  CREATED: 201,
  BAD_REQUEST: 400,
  UNAUTHORIZED: 401,
  NOT_FOUND: 404,
  INTERNAL_SERVER_ERROR: 500
});

// 3. Redux / State Machine Action Types
const ACTION_TYPES = Object.freeze({
  USER_LOGIN_REQUEST: "USER_LOGIN_REQUEST",
  USER_LOGIN_SUCCESS: "USER_LOGIN_SUCCESS",
  USER_LOGIN_FAILURE: "USER_LOGIN_FAILURE"
});

// Runtime function demonstrating camelCase variables alongside CONSTANT_CASE
function connectToService(endpointPath, currentRetries = 0) {
  // camelCase for runtime local calculation
  const targetUrl = `${API_BASE_URL}/${endpointPath}`;

  if (currentRetries >= MAX_LOGIN_ATTEMPTS) {
    throw new Error(`Exceeded maximum retry limit of ${MAX_LOGIN_ATTEMPTS}`);
  }

  return fetch(targetUrl);
}
```

```python
# Python Module Constants (PEP 8)
import os

DATABASE_HOST = os.getenv("DB_HOST", "localhost")
DATABASE_PORT = int(os.getenv("DB_PORT", 5432))
CACHE_TTL_SECONDS = 3600
MAX_UPLOAD_SIZE_BYTES = 10 * 1024 * 1024  # 10 MB

def get_connection_uri() -> str:
    # Function parameters and local variables use snake_case
    return f"postgresql://{DATABASE_HOST}:{DATABASE_PORT}/app_production"
```

```text
# Environment Configuration File (.env)
NODE_ENV=production
PORT=8080
JWT_EXPIRATION_HOURS=24
S3_BUCKET_NAME=production-user-uploads
```

> [!WARNING]
> **Crucial Technical Clarification: Casing Does Not Create Immutability!**
> Casing is purely a visual convention. Naming an identifier in `CONSTANT_CASE` does **not** make it immutable by itself:
> * In **JavaScript**, declaring `let MAX_USERS = 100;` still allows reassignment (`MAX_USERS = 200;`). To prevent reassignment, you must use the `const` keyword. Furthermore, `const CONFIG = { host: "localhost" };` protects only the variable reference; the object's properties remain mutable unless protected with `Object.freeze(CONFIG)`.
> * In **Python**, constants do not exist at the language runtime level. A variable named `MAX_USERS = 100` can be reassigned anywhere. The casing serves purely as an explicit contractual warning to developers: *"Do not reassign this value."*

#### Correct vs. Incorrect Examples

| Status | Identifier | Explanation |
| :--- | :--- | :--- |
| **Correct** | `MAX_FILE_SIZE_BYTES` | All uppercase letters separated by underscores. |
| **Correct** | `DEFAULT_THEME_COLOR` | Clean separation of words using underscores. |
| **Incorrect** | `max_file_size_bytes` | snake_case; indicates a normal mutable variable. |
| **Incorrect** | `MAX-FILE-SIZE-BYTES` | Uses hyphens; invalid syntax in JavaScript and Python. |
| **Incorrect** | `MAXFILESIZE` | Words run together without underscores; difficult to read. |

#### Common Mistakes Beginners Should Avoid
* **Overusing CONSTANT_CASE for local `const` variables:** Using `CONSTANT_CASE` for every variable declared with `const` (such as `const CURRENT_USER = getUser();`) clutters code and confuses team members. Reserve `CONSTANT_CASE` for global, static, author-time values.
* **Assuming `const` guarantees deep immutability:** Writing `const SETTINGS = { darkTheme: true };` and mutating `SETTINGS.darkTheme = false;` is valid JavaScript. If deep immutability is required, wrap the object with `Object.freeze()`.
* **Using hyphens instead of underscores:** Writing `MAX-SIZE = 10` causes syntax errors because `-` is interpreted as subtraction.

---

## 5. Understanding HTML & CSS Selectors and Custom Properties

CSS provides distinct mechanisms for selecting markup elements and managing reusable values. Understanding how naming conventions interface with these selectors is essential for writing clean stylesheets.

```text
+-------------------------------------------------------------------------+
|                               CSS SELECTORS                             |
+------------------------------------+------------------------------------+
|         CLASS SELECTOR (.)         |          ID SELECTOR (#)           |
+------------------------------------+------------------------------------+
|  * Reusable on many elements       |  * Unique to one element per page  |
|  * Syntax: .kebab-case-name        |  * Syntax: #kebab-case-name        |
|  * Moderate specificity (0, 0, 1)  |  * High specificity (0, 1, 0)      |
+------------------------------------+------------------------------------+
|                      CSS CUSTOM PROPERTIES (--*)                        |
+-------------------------------------------------------------------------+
|  * User-defined cascading variables (e.g., --primary-color: #2563eb;)   |
|  * Prefixed with double hyphen (--), consumed via var(--name)           |
|  * Completely distinct from native CSS properties (color, display, etc.)|
+-------------------------------------------------------------------------+
```

### 1. HTML Class Selectors (`.`)
* **Purpose:** Targeted, reusable styling. Multiple elements on the same page can share the same class, and an individual element can possess multiple classes.
* **Syntax in CSS:** Preceded by a period (`.`): `.card-container`, `.nav-link`, `.is-active`.
* **Convention:** Standard practice in HTML and CSS is `kebab-case`.
* **Example:**
  ```html
  <div class="alert-box alert-warning">Warning: Check your input.</div>
  ```
  ```css
  .alert-box {
    padding: 1rem;
    border-radius: 4px;
  }
  .alert-warning {
    background-color: #fef3c7;
    color: #92400e;
  }
  ```

### 2. HTML ID Selectors (`#`)
* **Purpose:** Selecting a single, unique element on a page. An ID must appear only once within an HTML document. IDs are also used as fragment identifiers for page scrolling anchors (`#contact-us`).
* **Syntax in CSS:** Preceded by a hash symbol (`#`): `#main-header`, `#checkout-form`.
* **Convention:** Like classes, IDs traditionally use `kebab-case`.
* **Specificity Warning:** ID selectors have higher specificity than class selectors. Relying heavily on IDs for styling can make rules difficult to override. Use classes for styling and reserve IDs for DOM anchors and specific JavaScript element references.

### 3. CSS Custom Properties (`--*`) vs. Ordinary CSS Properties
* **Native (Ordinary) CSS Properties:** Standard, built-in rendering properties defined by the W3C CSS specifications (e.g., `background-color`, `font-size`, `display`, `margin-top`). They only accept predefined values or standard units.
* **CSS Custom Properties (Variables):** User-defined variables that can store arbitrary CSS values (colors, dimensions, fonts, calculations). 
* **Syntax:** Must be prefixed with two hyphens (`--`) and declared using `kebab-case` (e.g., `--brand-primary: #3b82f6;`). They are retrieved using the `var()` function (e.g., `color: var(--brand-primary);`).
* **Inheritance:** Custom properties cascade through the DOM tree, meaning child elements inherit the values defined on ancestors or the `:root` pseudo-class.

```css
:root {
  /* CSS Custom Properties (Variables) */
  --font-family-base: "Inter", sans-serif;
  --spacing-medium: 1.5rem;
  --border-radius-card: 8px;
}

.profile-card {
  /* Using standard properties alongside custom properties */
  font-family: var(--font-family-base);
  padding: var(--spacing-medium);
  border-radius: var(--border-radius-card);
  border: 1px solid #e2e8f0; /* Ordinary CSS property with literal value */
}
```

---

## 6. Differences Between HTML/CSS and JavaScript Naming

Switching between frontend markup and programming logic introduces critical naming shifts that every web developer must navigate.

### 1. Why JavaScript Cannot Use Hyphens
In HTML and CSS, hyphens are standard separators:
```css
.card-item { margin-top: 10px; }
```
However, in JavaScript, the hyphen character (`-`) is the arithmetic subtraction operator. If JavaScript permitted hyphens in identifier names, the interpreter would encounter syntactic ambiguity:

```javascript
// Ambiguity illustration:
let first-name = "Jordan";
// Does this mean declaring a variable named "first-name"?
// Or evaluating the expression: (first) minus (name)?
```

Because of this lexical rule, JavaScript identifiers (variable names, function names, and class names) **cannot contain hyphens**. Instead, JavaScript relies on **camelCase** and **PascalCase**.

### 2. HTML `data-*` Attributes to JavaScript `dataset`
HTML elements can store custom metadata via `data-*` attributes written in `kebab-case`. When accessing these attributes through JavaScript's DOM API, the browser automatically translates `kebab-case` into `camelCase` on the `element.dataset` object:

```html
<!-- HTML (kebab-case) -->
<div id="product-card" data-product-id="4092" data-in-stock="true" data-discount-rate="15">
  Wireless Headphones
</div>
```

```javascript
// JavaScript DOM Access (camelCase)
const productElement = document.getElementById("product-card");

// The browser automatically maps the keys:
console.log(productElement.dataset.productId);    // "4092"
console.log(productElement.dataset.inStock);      // "true"
console.log(productElement.dataset.discountRate); // "15"

// Modifying data attributes in JavaScript:
productElement.dataset.discountRate = "20"; 
// Automatically updates DOM attribute: data-discount-rate="20"
```

### 3. HTML Attributes vs. JSX Properties in React
Because JSX is a syntax extension that compiles directly into JavaScript, it cannot use standard HTML keywords that clash with JavaScript reserved words. JSX maps them to `camelCase` equivalents:

| HTML Attribute (kebab-case / lowercase) | React JSX Property (camelCase) | Technical Reason |
| :--- | :--- | :--- |
| `class` | `className` | `class` is a reserved keyword in JavaScript for defining classes. |
| `for` | `htmlFor` | `for` is a reserved keyword in JavaScript for loops (`for (let i = 0...)`). |
| `onclick` | `onClick` | JSX event handlers follow camelCase function references. |
| `tabindex` | `tabIndex` | Standardizes DOM property casing. |
| `autocomplete` | `autoComplete` | Standardizes DOM property casing. |
| `style="font-size: 16px;"` | `style={{ fontSize: "16px" }}` | Inline styles in JSX are JavaScript objects using camelCase keys. |

---

## 7. Integrated Real-World Examples

To illustrate how these conventions work in harmony within an application, review the following complete, executable components across HTML, CSS, and JavaScript.

### 7.1 HTML Implementation (`index.html`)

This file demonstrates standard `kebab-case` for classes, IDs, and data attributes:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Developer Portfolio Card</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <main id="app-container" class="page-container">
    <article 
      id="profile-card-widget" 
      class="card-widget user-highlight" 
      data-user-id="dev_449"
      data-account-status="verified"
      data-available-for-hire="true"
    >
      <header class="card-header">
        <h2 id="user-display-name" class="user-name">Sarah Connor</h2>
        <span class="status-badge active-status">Online</span>
      </header>

      <div class="card-body">
        <p class="user-bio">
          Full-Stack Software Engineer specializing in scalable web architectures and accessible UIs.
        </p>
        <div class="metrics-grid">
          <div class="metric-item">
            <span class="metric-value">42</span>
            <span class="metric-label">Repositories</span>
          </div>
          <div class="metric-item">
            <span class="metric-value">1.8k</span>
            <span class="metric-label">Contributions</span>
          </div>
        </div>
      </div>

      <footer class="card-footer">
        <button 
          type="button" 
          id="btn-contact-developer" 
          class="btn btn-action-primary"
          data-action-type="open-contact-modal"
        >
          Contact Developer
        </button>
      </footer>
    </article>
  </main>

  <script src="app.js"></script>
</body>
</html>
```

### 7.2 CSS Implementation (`styles.css`)

This stylesheet uses `kebab-case` throughout for class selectors, ID selectors, CSS custom properties, and native properties:

```css
/* CSS Custom Properties (Variables) */
:root {
  --primary-brand-color: #4f46e5;
  --primary-brand-hover: #4338ca;
  --surface-bg-color: #ffffff;
  --page-bg-color: #f3f4f6;
  --text-primary-color: #111827;
  --text-muted-color: #4b5563;
  --badge-success-bg: #dcfce7;
  --badge-success-text: #15803d;
  --card-border-radius: 12px;
  --standard-transition: all 0.2s ease-in-out;
}

/* Page Layout */
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  background-color: var(--page-bg-color);
  color: var(--text-primary-color);
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

#app-container {
  width: 100%;
  max-width: 480px;
  padding: 1.5rem;
}

/* Card Widget (Classes in kebab-case) */
.card-widget {
  background-color: var(--surface-bg-color);
  border-radius: var(--card-border-radius);
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
  padding: 1.5rem;
  border: 1px solid #e5e7eb;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.user-name {
  margin: 0;
  font-size: 1.5rem;
  font-weight: 700;
}

.status-badge {
  font-size: 0.75rem;
  font-weight: 600;
  padding: 0.25rem 0.75rem;
  border-radius: 9999px;
}

.status-badge.active-status {
  background-color: var(--badge-success-bg);
  color: var(--badge-success-text);
}

.card-body .user-bio {
  color: var(--text-muted-color);
  line-height: 1.5;
  margin: 0 0 1.5rem 0;
}

/* Metrics Grid */
.metrics-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.metric-item {
  background-color: #f9fafb;
  border-radius: 8px;
  padding: 0.75rem;
  text-align: center;
}

.metric-value {
  display: block;
  font-size: 1.25rem;
  font-weight: 700;
}

.metric-label {
  display: block;
  font-size: 0.75rem;
  color: var(--text-muted-color);
}

/* Action Buttons */
.btn {
  width: 100%;
  border: none;
  font-size: 0.875rem;
  font-weight: 600;
  padding: 0.75rem 1rem;
  border-radius: 6px;
  cursor: pointer;
  transition: var(--standard-transition);
}

.btn-action-primary {
  background-color: var(--primary-brand-color);
  color: #ffffff;
}

.btn-action-primary:hover {
  background-color: var(--primary-brand-hover);
}
```

### 7.3 JavaScript Implementation (`app.js`)

This script combines **`UPPER_SNAKE_CASE`** (constants), **`PascalCase`** (classes), and **`camelCase`** (variables, functions, methods, and dataset properties) to interact with the DOM:

```javascript
// -------------------------------------------------------------
// 1. UPPER_SNAKE_CASE: Application Constants & Configuration
// -------------------------------------------------------------
const NOTIFICATION_DISMISS_DELAY_MS = 3000;
const API_TELEMETRY_ENDPOINT = "https://analytics.example.com/events";
const DEFAULT_ACCOUNT_TIER = "FREE_TIER";

// -------------------------------------------------------------
// 2. PascalCase: Class Definition
// -------------------------------------------------------------
class UserCardManager {
  constructor(cardElementId) {
    // camelCase: Instance properties
    this.cardElement = document.getElementById(cardElementId);
    this.contactButton = this.cardElement?.querySelector("#btn-contact-developer");
    this.clickCount = 0;
  }

  // camelCase: Method definition
  initialize() {
    if (!this.cardElement || !this.contactButton) {
      console.error("Initialization failed: DOM elements not found.");
      return;
    }

    this.extractDatasetAttributes();
    this.attachEventListeners();
    console.log("UserCardManager initialized successfully.");
  }

  // camelCase: Method reading HTML kebab-case data-* attributes
  extractDatasetAttributes() {
    // HTML data-user-id -> JS dataset.userId (camelCase)
    const userId = this.cardElement.dataset.userId;
    // HTML data-account-status -> JS dataset.accountStatus (camelCase)
    const accountStatus = this.cardElement.dataset.accountStatus;
    // HTML data-available-for-hire -> JS dataset.availableForHire (camelCase)
    const isAvailableForHire = this.cardElement.dataset.availableForHire === "true";

    console.log(`User Profile Loaded: ID=${userId}, Status=${accountStatus}, Available=${isAvailableForHire}`);
  }

  // camelCase: Event handling method
  attachEventListeners() {
    this.contactButton.addEventListener("click", (event) => {
      this.handleContactButtonClick(event);
    });
  }

  // camelCase: Callback handler
  handleContactButtonClick(event) {
    this.clickCount += 1;
    const actionType = event.target.dataset.actionType; // data-action-type

    console.log(`Action dispatched: [${actionType}], Total clicks: ${this.clickCount}`);
    this.displayNotification("Thank you for reaching out! Response pending.");
  }

  // camelCase: UI update function
  displayNotification(messageText) {
    const originalButtonText = this.contactButton.textContent;
    this.contactButton.textContent = messageText;
    this.contactButton.disabled = true;

    setTimeout(() => {
      this.contactButton.textContent = originalButtonText;
      this.contactButton.disabled = false;
    }, NOTIFICATION_DISMISS_DELAY_MS);
  }
}

// -------------------------------------------------------------
// 3. Execution: camelCase variables and PascalCase instantiations
// -------------------------------------------------------------
document.addEventListener("DOMContentLoaded", () => {
  const profileWidget = new UserCardManager("profile-card-widget");
  profileWidget.initialize();
});
```

### 7.4 Expected Output

When the above HTML, CSS, and JavaScript run in a browser:

1. **Initial Page Load:**
   The browser console logs the parsed dataset attributes:
   ```text
   User Profile Loaded: ID=dev_449, Status=verified, Available=true
   UserCardManager initialized successfully.
   ```
2. **User Click Interaction:**
   When the user clicks the `"Contact Developer"` button:
   ```text
   Action dispatched: [open-contact-modal], Total clicks: 1
   ```
   The button text changes to `"Thank you for reaching out! Response pending."` for 3,000 milliseconds (configured by `NOTIFICATION_DISMISS_DELAY_MS`), after which it returns to `"Contact Developer"`.

---

## 8. Common Beginner Mistakes and How to Fix Them

Review these common pitfalls and their corrections:

### Mistake 1: Hyphens in JavaScript Variable Names
```javascript
// ❌ WRONG: SyntaxError: Unexpected token '-'
let user-name = "Alex";

// ✅ CORRECT: Use camelCase for variables
let userName = "Alex";
```
*Why it fails:* The JavaScript engine parses `-` as subtraction, attempting to calculate `user minus name`.

---

### Mistake 2: Using Lowercase for React Components
```javascript
// ❌ WRONG: Treated as an unknown HTML element
function userBadge(props) {
  return <div className="badge">{props.label}</div>;
}

// In JSX:
<userBadge label="Admin" /> // Rendered directly into DOM as <userbadge label="Admin"></userbadge>

// ✅ CORRECT: Use PascalCase for custom components
function UserBadge(props) {
  return <div className="badge">{props.label}</div>;
}

// In JSX:
<UserBadge label="Admin" />
```
*Why it fails:* React and JSX inspect the first character. Lowercase tags are treated as native HTML elements.

---

### Mistake 3: Accessing `dataset` Using `kebab-case`
```javascript
// Given markup: <div id="card" data-user-role="editor"></div>
const card = document.getElementById("card");

// ❌ WRONG: Undefined or SyntaxError
console.log(card.dataset.user-role); 

// ✅ CORRECT: The browser automatically camelCases data-* keys
console.log(card.dataset.userRole); // Output: "editor"
```
*Why it fails:* The HTML specification converts `data-*` hyphen-separated names into camelCase object properties under the `dataset` DOM interface.

---

### Mistake 4: Assuming CONSTANT_CASE Variables Cannot Be Mutated
```javascript
// ❌ WRONG: Assuming casing alone creates a read-only variable
let MAX_USERS = 100;
MAX_USERS = 200; // Successfully re-assigned without error!

// ❌ WRONG: Assuming const creates deep immutability for objects
const APP_CONFIG = { timeout: 5000 };
APP_CONFIG.timeout = 10000; // Successfully mutated!

// ✅ CORRECT: Combine const with Object.freeze() for true immutability
const APP_CONFIG = Object.freeze({ timeout: 5000 });
// APP_CONFIG.timeout = 10000; // Throws error in strict mode or fails silently
```
*Why it fails:* Casing is merely a developer convention. Immutability requires language mechanisms like `const` and `Object.freeze()`.

---

### Mistake 5: Using `class` and `onclick` Inside React JSX
```javascript
// ❌ WRONG: class is a reserved JS word; onclick is not the JSX event handler
function ActionButton() {
  return <button class="btn" onclick={handleClick}>Save</button>;
}

// ✅ CORRECT: Use className and onClick
function ActionButton() {
  return <button className="btn" onClick={handleClick}>Save</button>;
}
```
*Why it fails:* JSX compiles directly into `React.createElement()` JavaScript calls. `class` is reserved syntax in JavaScript for defining classes, so JSX uses `className`.

---

### Mistake 6: Using Hyphens in SQL Identifiers Without Escaping
```sql
-- ❌ WRONG: Syntax error in SQL query
SELECT user-name FROM customer-table;

-- ✅ CORRECT: Use snake_case in SQL
SELECT user_name FROM customer_table;
```
*Why it fails:* In SQL, `-` is the subtraction operator. If an unquoted column name contains hyphens, the database evaluates it as an arithmetic expression.

---

### Mistake 7: Overusing CONSTANT_CASE for Local Runtime Variables Declared with `const`
```javascript
// ❌ WRONG: Misusing CONSTANT_CASE for dynamic runtime results
function processUserRegistration(userData) {
  const USER_ID = generateUniqueId();           // Local runtime calculation
  const FILTERED_ROLES = userData.roles.trim(); // Temporary local variable
  return { id: USER_ID, roles: FILTERED_ROLES };
}

// ✅ CORRECT: Use camelCase for local const variables, reserve CONSTANT_CASE for author-time constants
const DEFAULT_USER_ROLE = "GUEST"; // Global author-time constant

function processUserRegistration(userData) {
  const userId = generateUniqueId();
  const filteredRoles = userData.roles.trim() || DEFAULT_USER_ROLE;
  return { id: userId, roles: filteredRoles };
}
```
*Why it fails:* Declaring a variable with `const` in JavaScript simply means its identifier binding cannot be reassigned. Modern style guides (including Google and Airbnb) mandate `camelCase` for runtime computed values, reserving `CONSTANT_CASE` strictly for static author-time constants and module configurations.

---

## 9. Best Practices for Long-Term Consistency

To maintain clean and scalable codebases, follow these development guidelines:

### 1. Establish Project-Wide Style Guides
Document your casing rules in a `CONTRIBUTING.md` or team handbook. Ensure everyone agrees on conventions before writing code:
* Frontend markup and styling: `kebab-case`.
* JavaScript application logic: `camelCase` for values, `PascalCase` for classes/components, `CONSTANT_CASE` for global configurations and constants.
* Backend APIs and relational databases: `snake_case`.

### 2. Automate Linting and Formatting
Do not rely solely on manual code reviews to enforce conventions. Configure automated linting tools in your continuous integration (CI) pipeline:
* **ESLint:** Enforce naming rules with `@typescript-eslint/naming-convention` or `camelcase` rules.
* **Stylelint:** Enforce `kebab-case` for CSS class and ID selectors using `selector-class-pattern` and `custom-property-pattern`.
* **Prettier:** Automate code layout and syntax normalization across your team.

### 3. Consider Established CSS Methodologies (BEM)
In complex CSS projects, `kebab-case` is often structured using methodologies such as **BEM (Block, Element, Modifier)** to prevent specificity conflicts:
* **Block:** Standalone entity (`.profile-card`).
* **Element:** Part of a block tied to its context (`.profile-card__avatar`).
* **Modifier:** Flag that changes style or behavior (`.profile-card--highlighted`).

### 4. Optimize for Intent and Clarity
Never sacrifice descriptive naming for brevity. Avoid single-letter identifiers (except standard loop counters like `i` or coordinate points `x, y`). A descriptive name like `isUserAuthenticated` is far superior to `auth` or `isOk`.

---

## 10. Quick-Reference Summary Table

Keep this revision matrix handy when switching between languages and tech stacks:

| Casing Style | Exact Syntax Pattern | Where to Use | Where NOT to Use | Concrete Example |
| :--- | :--- | :--- | :--- | :--- |
| **camelCase** | `lowerUpperUpper` | • JS variables, functions, methods<br>• JS object keys<br>• JSX attributes (`className`, `onClick`)<br>• Java, C#, Swift methods | • HTML classes or CSS selectors<br>• Python functions (PEP 8)<br>• React components | `calculateDiscountRate()` |
| **PascalCase** | `UpperUpperUpper` | • React / Vue / Svelte components<br>• JavaScript / TypeScript classes<br>• TypeScript interfaces and types<br>• Python classes (PEP 8) | • Standard JS functions or variables<br>• HTML classes or CSS selectors<br>• SQL column names | `OrderProcessingService` |
| **snake_case** | `lower_lower_lower` | • Python variables and functions<br>• SQL tables, columns, constraints<br>• REST API JSON responses<br>• Rust / C functions | • JavaScript variables and functions<br>• CSS class selectors<br>• React component names | `order_processing_service` |
| **kebab-case** | `lower-lower-lower` | • HTML classes and IDs<br>• CSS selectors and properties<br>• CSS custom properties (`--var`)<br>• HTML `data-*` attributes<br>• URL paths and slugs | • JavaScript variable or function names (causes syntax error)<br>• Python variables<br>• SQL column names | `order-processing-service` |
| **CONSTANT_CASE** / **UPPER_SNAKE_CASE** | `UPPER_UPPER_UPPER` | • Static, global constants<br>• Application configuration values<br>• Environment variables (`.env`)<br>• Redux action types | • Local, mutable variables<br>• Function names or method names<br>• HTML / CSS selectors | `MAX_RETRY_ATTEMPTS` |
