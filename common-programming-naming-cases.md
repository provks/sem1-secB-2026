# Common Programming Naming Cases

* A quick guide to writing clean, readable code.*

Good code is not just about making a program work. It is also about making it easy for other people to understand. Naming conventions help programmers give variables, functions, classes, and constants a consistent style.

## 01. camelCase — The Connected Style

The first word begins with a lowercase letter, while every following word begins with an uppercase letter.

**Examples:** `studentName`, `totalMarks`, `calculatePrice`

**Common use:** Variables and functions in JavaScript.

## 02. PascalCase — The Capital Start

Every word begins with an uppercase letter, including the first one.

**Examples:** `StudentProfile`, `BankAccount`, `OnlineShoppingCart`

**Common use:** Classes and components.

## 03. snake_case — The Underscore Style

All letters are lowercase, and an underscore separates each word.

**Examples:** `student_name`, `total_marks`, `calculate_price`

**Common use:** Variables and functions in Python.

## 04. SCREAMING_SNAKE_CASE — The Constant Style

All letters are uppercase, with underscores separating words.

**Examples:** `MAX_ATTEMPTS`, `PASSING_MARKS`, `TAX_RATE`

**Common use:** Constants and fixed configuration values.

## 05. kebab-case — The Hyphen Style

All letters are lowercase, and a hyphen separates each word.

**Examples:** `student-profile`, `online-store`, `course-details`

**Common use:** URLs, CSS class names, and file names.

---

## One Idea, Five Styles

Imagine you are building a student management system. The same concept can be written in five different naming styles.

| Style | Example |
|---|---|
| camelCase | `studentDetails` |
| PascalCase | `StudentDetails` |
| snake_case | `student_details` |
| SCREAMING_SNAKE_CASE | `STUDENT_DETAILS` |
| kebab-case | `student-details` |

## Naming Mistakes to Avoid

- `studentname` — difficult to scan when names contain multiple words.
- `Student_name` — mixes naming styles unnecessarily.
- `student-details` — invalid as a regular variable name in languages such as C++ and JavaScript.
- `TOTALmarks` — inconsistent capitalization.

## The Golden Rule

**A good name explains the purpose of the code without requiring extra comments.**

Choose meaningful words, follow the conventions of your programming language, and keep your naming style consistent.

*Remember: clean naming is a small habit that makes a big difference in software development.*