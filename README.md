# Enigma's codestyle
These are brief guidelines to follow when you are writing or contributing on any Enigma's projects, to keep or sanity and to grow a concise and reliable legacy code. Enjoy it!

## Index

- [Commits]()
- [HTML]()
- [Template Engines]()
- [CSS]()
- [CSS Pre Processors]()

### Commits
To keep contributions easier across the globe, all of our commit messages, pull request titles, comments and issues discussions must be in english.

Before any commit in project, please check if exist an issue to that feature or fix you are commiting, and if true, link your commit through the use of `#` in your commit message.

Also, we need some kind of short labels on each commit message, it makes easier to identify the purpose of any commit. Our labels are divided into:

- **Fix**: When your commit fix any identified bug.
- **Feature**: When your commit introduces a new feature to the project.
- **Redo**: When you refactor anything to be better or run smoothier.

```javascript
// Good
commit -m "Feature: New navigation dropdown menu #302"

// Bad
commit -m "New navigation dropdown menu"
```
