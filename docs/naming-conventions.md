# Programming Naming Conventions

Naming conventions are rules used to name variables, functions, classes, and constants consistently. They improve code readability and maintainability.

## 1. camelCase

The first word starts with a lowercase letter, and each following word starts with an uppercase letter.

**Example:**
```javascript
let studentName = "Mohit";

function getUserDetails() {
    return studentName;
}
```

**Common use:** JavaScript variables and functions.

## 2. PascalCase

Every word starts with an uppercase letter.

**Example:**
```javascript
class StudentDetails {
    constructor(name) {
        this.name = name;
    }
}
```

**Common use:** Class names and React component names.

## 3. snake_case

All words are lowercase and separated by underscores.

**Example:**
```python
student_name = "Mohit"

def get_user_details():
    return student_name
```

**Common use:** Python variables and functions.

## 4. kebab-case

All words are lowercase and separated by hyphens.

**Examples:**
```text
student-profile
navigation-bar
```

**Common use:** CSS class names and URLs.

## 5. CONSTANT_CASE

All letters are uppercase, and words are separated by underscores.

**Example:**
```python
MAX_RETRY_LIMIT = 3
API_BASE_URL = "https://example.com"
```

**Common use:** Constants in Python and other programming languages.

## Comparison Table

| Convention | Example | Common Use |
|---|---|---|
| camelCase | `studentName` | JavaScript variables |
| PascalCase | `StudentDetails` | Classes and React components |
| snake_case | `student_name` | Python variables and functions |
| kebab-case | `student-profile` | CSS classes and URLs |
| CONSTANT_CASE | `MAX_RETRY_LIMIT` | Constants |

## Best Practices

- Use descriptive and meaningful names.
- Follow the conventions of the programming language.
- Maintain consistency throughout the project.
- Avoid unnecessary abbreviations.
- Follow existing project guidelines when contributing to a repository.

## Conclusion

Using consistent naming conventions makes code easier to read, understand, debug, and maintain.