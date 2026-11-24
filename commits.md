
# Git Assignment - Commit History

## 1. Commit History

Output of git log --oneline:

```text
609d729 Update Git learning notes with commit workflow
811f644 Add beginner Git learning notes
3ce265b Add project README
```

## 2. Two Common Beginner Mistakes

### Mistake 1: Forgetting to Stage Changes

Beginners sometimes modify a file but forget to use the git add command before committing.

**Explanation:** Git commits only staged changes. If we forget to stage a modified file, the latest changes will not be included in the commit.

**Solution:** Always use git status and git add before committing.

### Mistake 2: Writing Unclear Commit Messages

Beginners sometimes use messages like "update", "done", or "changes".

**Explanation:** These messages do not explain what was changed in the project.

**Solution:** Always write meaningful messages, such as "Add project README".
