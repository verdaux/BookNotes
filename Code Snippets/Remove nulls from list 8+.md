---
created: 2020-08-31T22:08:24+05:30
modified: 2022-09-06T23:50:25+05:30
type: Checklist
---

# Remove nulls from list 8+

Java 8 or higher versions:
The approach for removing nulls from a Java List for Java 8 or higher versions is pretty intuitive and elegant:

@Test
public removeAllNullsFromListWithJava8() {
 
    List<String> list =
      new ArrayList<>(Arrays.asList("A", null, "B", null));
 
    list.removeIf(Objects::isNull);
 
    assertThat(list, hasSize(2));
}
We can simply use the removeIf() construct to remove all null values.

If we don’t want to alter the existing list and rather return a new list with all non-null values, we can have:

Java

@Test
public removeAllNullsFromListWithJava8() {
 
    List<String> list =
      new ArrayList<>(Arrays.asList("A", null, "B", null));
 
    List<String> newList = list.stream().filter(Objects::nonNull)
      .collect(Collectors.toList());
 
    assertThat(list, hasSize(4));
    assertThat(newList, hasSize(2));
}
