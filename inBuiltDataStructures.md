# Map
## CRUD Operations
|                      | Syntax                                           | Example                                     |
|----------------------|--------------------------------------------------|---------------------------------------------|
| Create               | let map = new Map()                              | let mapping = new Map();                    |
| Update - Add/ Modify | map.set(key,value)                               | mapping.set("key",1);                       |
|                      | Add array map.set([[key1,value1],[key2,value2]]) | mapping.set([["2",2],["3",3],["4",4]]);     |
|                      | Add object map.set(Object.entries(obj));         | mapping.set(Object.entries({one:1,two:2})); |
| Read                 | map.get(key)                                     | mapping.get("key");                         |
| Delete               | map.delete(key)                                  | mapping.delete("key");                      |
|                      | map.clear()                                      | mapping.clear()                             |

## Common Operations
|                         | Syntax                           | Example                                    |
|-------------------------|----------------------------------|--------------------------------------------|
| Size                    | map.size                         | map.set(1,1);map.set(2,”two”); map.size//2 |
| Check if element exists | map.has(key)                     | map.has(“key”);                            |
| Iteration               | For..of, forEach                 |                                            |
|                         | map.keys() //returns iterable    | map.keys()//{1,2}                          |
|                         | map.values()// returns iterable  | map.values()//{1,”two”}                    |
|                         | map.entries()// returns iterable | map.entries()//{1 => 1, 2 => "two"}        |
