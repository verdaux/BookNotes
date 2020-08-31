---
created: 2020-08-31T22:06:06+05:30
modified: 2020-08-31T22:07:07+05:30
---

# Remove nulls from a list

Java 7 or lower versions:
When working with Java 7 or lower versions, we can use the below construct to remove all nulls from a List:

Java

@Test
public removeAllNullsFromListWithJava7OrLower() {
 
    List<String> list =
      new ArrayList<>(Arrays.asList("A", null, "B", null));
 
    list.removeAll(Collections.singleton(null));
 
    assertThat(list, hasSize(2));
}