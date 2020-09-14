---
created: 2020-09-14T11:18:43+05:30
modified: 2020-09-14T11:24:18+05:30
type: Checklist
---

# When objects serialize

- [ ] Objects on the heap have a state
- [ ] State = value of instance variable
- [ ] Value helps distinguish one instance of a class from another
- [ ] Deflate the object and save bytes into a file
- [ ] FOS fos = new FOS("file.ser")
- [ ] OOS oos = new OOS(fos)
- [ ] oos.writeObject(myFoo)