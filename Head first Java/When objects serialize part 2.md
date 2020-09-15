---
created: 2020-09-15T10:15:07+05:30
modified: 2020-09-15T10:22:01+05:30
type: Checklist
---

# When objects serialize part 2

- [ ] If parent object is serialized all sub/child objects also serialize
- [ ] Serialization saves entire object graph
- [ ] If you want your class to be serializable, implement serializable
- [ ] Either the entire object graph is serialized correctly or serialization fails
- [ ] Mark an instance variable as transient if it can't (or shouldn't) be saved