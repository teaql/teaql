# TeaQL - A Safe, Simple, Unified Generative based versatile query library for various data sources .


## Feature

* One query do all with connected data
* Graph theory based query
* Fine grained columns and filters
* Different data in a single query

## This is how ChatGPT explain our query


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

Q.family().hasKids(Q.kid().whosGenderIsBoy())

```

Select families and count kid girls.

```java

Q.family().countKids("kidGirlsCount",Q.kid().whosGenderIsGirl())

```

Summarize the age of all kids of the families

```java
    public Object hello(WechatMessagingUserContext userContext) throws Exception {
        return  Q.family()
		.selectKidList()
		.averageAgeOfKids(Q.kid())
		.summarizeAgeOfKids(Q.kid())
		.countKids(Q.kid())
		.executeForList(userContext);
    }


```


