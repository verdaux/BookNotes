---
created: 2020-08-19T08:12:34+05:30
modified: 2020-08-19T08:20:38+05:30
type: Checklist
---

# Exception part II

- [ ] The compiler checks for everything except RuntimeExceptions
- [ ] If you throw an exception you must declare using throws in method declaration
- [ ] If you call a method that declares throws, one way to satisfy the compiler is to wrap the call in try/catch
- [ ] Exceptions that are NOT subclasses of RuntimeException are checked for by the compiler. So they're called checked exceptions
- [ ] Runtime exceptions are NOT checked so they're called unchecked exceptions
- [ ] You can throw, catch, declare a runtime exception but you don't have to and compiler won't check