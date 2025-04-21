# LevelDBStudy

This repo is for studying the source code of level DB

## CodeBase
* **leveldb/options.h**
``` 
#include "leveldb/export.h
namespace leveldb {
    class Cache;
}
```
-- Though the `cache.h` is not included, still forward declaration can work, as long as I only use `Cache *` or `Cache &`. The compiler only needs to know the Cache is a class.  
-- If the `cache.h` is included, the forward declaration is not needed.   
-- Also, the forward declaration should match the same namespace.
* **leveldb/cache.h**
abstract class is virtual = 0. This is like interface.
