# Commits Guide ✨

A standardized way to write clear, meaningful Git commit messages.  
Improves collaboration, simplifies project management, and automates changelog generation.

---

## Why Use Standard Commits? 🚀
- **Better Communication**: Write commit messages that everyone (and machines!) can understand.
- **Project Clarity**: Track changes by type (e.g., features, fixes, docs) and scope (e.g., component, module).
- **Automated Workflows**: Enable semantic versioning and auto-generated changelogs.
- **Team Alignment**: Reduce ambiguity in collaborative environments.

---

## Getting Started 🛠️

### Basic Workflow
1. **Stage Changes**  
   `git add <files>` or `git add .` (to stage all changes).
2. **Commit with Message**  
   `git commit -m "type(scope): description"`  
   Example:  
   `git commit -m "feat(auth): add password reset endpoint"`
3. **Push to Remote**  
   `git push origin <branch-name>`

---

## Commit Structure 📝
```plaintext
type(scope): description  # Required
<BLANK LINE>
body                       # Optional
<BLANK LINE>
footer                     # Optional (e.g., for breaking changes)
```

### Key Components
- **Type**: Purpose of the change (e.g., `feat`, `fix`, `docs`).  
- **Scope** (Optional): Module/component affected (e.g., `api`, `button`).  
- **Description**: Concise summary in imperative tense ("add" vs "added").  
- **Body/Footer**: For detailed explanations, breaking changes, or issue links.

---

## Commit Types 🔍
| Type       | Use Case                                  | Example                          |
|------------|-------------------------------------------|----------------------------------|
| `feat`     | New feature                               | `feat(profile): add dark mode`  |
| `fix`      | Bug resolution                            | `fix(login): handle 404 errors` |
| `docs`     | Documentation updates                     | `docs: update API guidelines`   |
| `style`    | Code formatting/readability               | `style: format CSS indentation` |
| `refactor` | Code restructuring (no new features/fixes)| `refactor: simplify auth logic` |
| `perf`     | Performance improvements                  | `perf(db): optimize queries`    |
| `test`     | Test-related changes                      | `test: add login unit tests`    |
| `build`    | Build system/config changes               | `build: update webpack config`  |
| `ci`       | CI/CD pipeline updates                    | `ci: fix GitHub Actions workflow` |
| `revert`   | Undo a previous commit                    | `revert: remove experimental API` |
| `design`   | UI/UX changes                             | `design(button): update hover effect` |
| `eod`      | Backup work-in-progress code at EOD       | `eod: WIP user dashboard layout` |

---

## Best Practices 🌟
1. **Use Imperative Mood**  
   Write "fix" instead of "fixed" or "fixes".
2. **Keep It Short**  
   Limit the subject line to 50 characters. Use the body for details.
3. **Reference Issues**  
   Include Jira tickets or GitHub issues:  
   `git commit -m "feat: user profile [PROJ-42]"`  
4. **Breaking Changes**  
   Add `!` after the type/scope and explain in the footer:  
   `feat(api)!: remove deprecated endpoints`  
5. **Multi-Line Commits**  
   Use `git commit` without `-m` to open an editor for longer messages.

---

## EOD (End-of-Day) Commits 🌙  
Use the `eod` type to back up work-in-progress code to the remote branch:  
```bash
git commit -m "eod: WIP user dashboard layout [PROJ-15]"
git push origin <branch-name>
```

---

## Integration with Jira/Tickets 🎫
Include the ticket ID + title directly:  
```bash
git commit -m "[PROJ-123] fix(payment): resolve currency rounding error"
```

---

## Pro Tips 💡
- **Automate Enforcement**  
  Use tools like [Commitlint](https://commitlint.js.org/) and [Husky](https://typicode.github.io/husky/) to validate messages.

---

## Repository Name
**commit-style-cheatsheet**  
**Dev**: Hussain Hanif  

Feel free to contribute or suggest improvements! 🚀
