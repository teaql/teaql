# TeaQL
The easiest query for various data sources.

## Examples

Select All families

```java

Q.family()

```


Select families has kids

```java

Q.family().hasKids()

```

Select families has kids boy

```java

Q.family().hasKids(Q.kid().filterByGendarOfBoy())

```
