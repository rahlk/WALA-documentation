We first create a language specific type reference for our language. 

In `com.ibm.wala.cast.golang/src/main/java/com/ibm/wala/cast/golang`  create a package called `types` and create a class called `GolangTypes.java`. 

Here we'll first create a [[ClassLoaderReference]] called (say) `goLoader` which is defines the meta-information that identifies a [[class loader]]. This is effectively a "name" for a [[class loader]]. 

Next we implement all the primitive types for golang (see this [link](https://go101.org/article/type-system-overview.html)). For example, the implemention for a golang `struct` type will be:

```java
public static final TypeReference Struct = TypeReference.findOrCreate(goLoader, "LStruct");
```

Above, we observe:
1. A variable `Struct` of type [[TypeReference]]. 
