## Definition
Redis is an open-source in-memory database store. Redis acts as a caching layer, or a very fast database 

> Redis is very fast that it can deliver content from its store with single to double digit miliseconds 

Redis is a Key / Value store, supports the following data structures
- Strings
- Sets
- Sorted Sets
- Lists
- Hashes 

### Strings
Redis Strings are the most basic value.
Strings are binary safe, so they contain data such as:
- JPEG image
- Serialized Ruby Objects
String can have a max length of 512 MB

### Lists
Redis lists are ordered collection of strings
List do not ensure unique strings (you can have duplicates)

### Sets
Redis Sets are an unordered collection of strings. Strings are unique within a set, so adding he same string will always only result with one instance. 

### Hashes
Redis Hashes represent a mapping between string fields and string values to represent an object 

Think of it as a collection of key/value pairs like a 
- JSON object
- Ruby Hash
- Python Dictionary