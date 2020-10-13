# CRUD Operations
|                            | Syntax                                                                                    | Example                                                             |
|----------------------------|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Create                     | let obj = new Object() // Object constructor syntax let obj = {} // Object literal syntax | let user = new Object();  let user= {a:1,b:2};                      |
| Read                       | obj[key]                                                                                  | user['a'] //`1`                                                     |
| Update                     |                                                                                           |                                                                     |
| Replace                    | obj[key]=value                                                                            | user[‘a’]=5; user["multi key"]=4; //`{a: 5, b: 2}`                  |
|                            | obj.key=value                                                                             | user.a=7; //`{a: 7, b: 2}`                                          |
| Add                        | obj[key]=value                                                                            | user.c=3; user["multi key"]=4; //`{a: 7, b: 2, c: 3, multi key: 4}` |
| Delete                     |                                                                                           |                                                                     |
| Delete object property     | delete obj[key]                                                                           | delete user.a; //`{b: 2, c: 3, multi key: 4}`                       |
| Delete/Reset entire object | Garbage collector deletes object when not referenced                                      |                                                                     |

# Object Iteration/ Copy
|                            | Syntax                                                                                                         | Example                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Copy                       | let obj2=obj1 //copied by reference #                                                                          | let obj1={a:1,b:{x:1}}; let obj2=obj1; obj2.a=2; console.log(obj1); //`{a: 2, b: {x:1}}`               |
|                            | let obj2=Object.assign({},obj1) //shallow copy - only primitives are copied Let obj2= {...obj1} //shallow copy | let obj3=Object.assign({},obj1); obj3.a=7,obj3.b.x=7; console.log(obj1); //`{a: 5, b: {x:7}`           |
|                            | let obj2= JSON.parse(JSON.stringify(obj1)) //deep copy                                                         | let obj4=JSON.parse(JSON.stringify(obj1)); obj4.a=6,obj4.b.x=6; console.log(obj1); //`{a: 5, b: {x:7}` |
| Iteration                  | For key in object //iterating over keys                                                                        | let obj={a:1,b:2}; for(key in obj)console.log(key);// `a b`                                            |
|                            | If key in object //checking if key exists                                                                      | if('a' in obj) console.log("yes"); // `yes`                                                            |
|                            | Object.keys(obj)                                                                                               | Object.keys(obj); //`["a", "b"]`                                                                       |
|                            | Object.values(obj)                                                                                             | Object.values(obj); //`[1, 2]`                                                                         |
|                            | Object.entries(obj)                                                                                            | Object.entries(obj); //`[[“a”,1],[“b”,2]]`                                                             |
| Delete/Reset entire object | Garbage collector deletes object when not referenced                                                           |                                                                                                        |
