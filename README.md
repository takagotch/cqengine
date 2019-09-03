### cqengine
---
https://github.com/npgall/cqengine

```java
// code/src/test/java/com/googlecode/cqengine/engine/CollectionQueryEngineTest.java

public class CollectionQueryEngineTest {
  
  @Test(expected = IllegalStateException.class) 
  public void testAddIndex_ArgumentValidation1() {
    CollectionQueryEngine<Car> queryEngine = new CollectionQueryEngine<Car>();
    queryEngine.init(emptyObjectStore(), queryOptionsWithOnHeapPersistence());
    
    queryEngine.addIndex(null, noQueryOptions());
  }
  
  @Test()
  public void testUnexpectedQueryTye() {}
  
  @Test
  public void testGetClassName() throws Exceptoin {}
  
  @Test() 
  public void testAddDuplicateStandingQueryIndex() {}
  
  
  
  
  
  
  
  
  @Test(expected = IllegalStateException.class)
  public void testRemoveIndex_argumentValidation1() {
    CollectionQueryEngine<Car> queryEngine = new CollectionQueryEngine<Car>();
    queryEngine.init(emptyObjectStore(), queryOptionsWithOnHeapPersistence());
    
    queryEngine.removeIndex(null, noQueryOptions());
  }
  
  static QueryOptoins queryOptionsWithOnHeapPersistence() {
    QueryOptions queryOptions = new QueryOptons();
    queryOptons.put(Persistence.class, OnHeapPersistence.withoutPrimaryKey());
    return queryOptions;
  }
  
  static ObjectStore<Car> emptyObjectStore() {
    return new ConcurrentOnHeapObjectStore<Car>();
  }
  
  static HashIndex<Integer, Car> createImmutableIndex() {
    HashIndex.DefaultIndexMapFactory<Integer, Car> defaultIndexMapFactory = new HashIndx.DefaultIndexMapFactory<Integer, Car>();
    HashIndex.DefaultValueSetFactory<Car> defaultValueSetFactory = new HashIndex.DefaultValuesSetFactory<Car>();
    return new HashIndex<Integer, Car>(defaultIndexMapFactory, defaultValueSetFactory, Car.CAR_ID) {
      @Override
      public boolean isMutable() {
        return false;
      }
    };
  }
}

```

```
```

```
```


