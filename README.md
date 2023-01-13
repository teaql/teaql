# TeaQL - The Safe, Simple, Unified query for various data sources.

## Examples

Select All families

```java

Q.family()

```
Select All families and their kids

```java

Q.family().selectKidList()

```

Select families has kids

```java

Q.family().hasKids()

```

Select families has kids boy

```java

Q.family().hasKids(Q.kid().filterByGendarOfBoy())

```

Select families and count kid girls.

```java

Q.family().countKid("kidGirlsCount",Q.kid().filterByGendarOfGirl())

```

Summarize the age of all kids of the families

```
    public Object hello(WechatMessagingUserContext userContext) throws Exception {
        return  Q.family()
		.selectKidList()
                .unselectPlatform()

		.averageAgeOfKidList("averageAgeOfTheFamily",Q.kid())
		.summarizeAgeOfKidList("sumAgeOfTheFamily",Q.kid())
		.countKid("countKidsOfTheFamily",Q.kid())
		.executeForList(userContext);
    }


```


