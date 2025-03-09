# Standard Git Commit Message Format

A **standard Git commit message format** helps maintain clarity and consistency in a project. A widely used convention is the **Conventional Commits** format.

## **1. Standard Git Commit Format**

```plaintext
<type>(<scope>): <short description>

[Optional] <Detailed explanation of the changes>

[Optional] Closes #<issue-number> or References #<issue-number>
```

---

## **2. Commit Message Types (Standard Keywords)**

| Type         | Description                                                  |
| ------------ | ------------------------------------------------------------ |
| **feat**     | A new feature                                                |
| **fix**      | A bug fix                                                    |
| **chore**    | Maintenance tasks (e.g., refactoring, updates)               |
| **docs**     | Documentation changes                                        |
| **style**    | Formatting changes (whitespace, linting, missing semicolons) |
| **refactor** | Code restructuring without changing behavior                 |
| **perf**     | Performance improvements                                     |
| **test**     | Adding or updating tests                                     |
| **ci**       | Changes to CI/CD configurations                              |
| **build**    | Changes to the build system or dependencies                  |

---

## **3. Commit Scope (Optional)**

The **scope** specifies the part of the project affected by the change, like:

- `auth`
- `models`
- `views`
- `database`
- `api`
- `ui`
- `tests`

---

## **4. Example Commit Messages**

### ✅ **Good Examples**

```sh
git commit -m "feat(auth): add phone number login for students"
```

```sh
git commit -m "fix(database): resolve UUID validation error"
```

```sh
git commit -m "docs(readme): update setup instructions"
```

```sh
git commit -m "refactor(api): optimize image watermarking function"
```

```sh
git commit -m "chore(deps): update Django to 5.1"
```

```sh
git commit -m "test(auth): add unit tests for phone login"
```

```sh
git commit -m "ci(github-actions): add automated testing workflow"
```

---

## **5. Commit Messages for Multiple Changes**

If you have multiple related changes, you can provide a **detailed explanation**:

```plaintext
feat(users): add UUID-based authentication

- Replaced integer IDs with UUIDs for better security.
- Updated user model, serializers, and views accordingly.
- Updated database migration to support UUID primary keys.

Closes #42
```

Commit with:

```sh
git commit -m "feat(users): add UUID-based authentication" -m "- Replaced integer IDs with UUIDs for better security. - Updated user model, serializers, and views accordingly. - Updated database migration to support UUID primary keys."
```

---

## **6. Push the Commit**

After committing, push your changes:

```sh
git push origin main
```

or if you're on another branch:

```sh
git push origin <branch-name>
```

---

This format keeps your commit history clean, readable, and easy to track. 🚀

