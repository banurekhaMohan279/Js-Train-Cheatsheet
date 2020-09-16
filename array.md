# Array - CRUD Operations
|                           | Syntax                                                 | Example                                                                                                                            |
|---------------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Create                    | 
|                           | arrName = [] // Array literal/shorthand                | let fruits = ['Apple',{name:'Mango'},'Orange',function(){alert('Pineapple')}];                                                     |
|                           | arrName = new Array() // Array constructor             | let arr =  new Array();                                                                                                            |
| Read                      | 
|                            | arrName[index]                                         | fruits[0];`//Apple`                                                                                                                  |
|                           | arrName[index].objKey // Access object                 | fruits[1].name; `// Mango`                                                                                                           |                                                                                                 |
| Update                    |                                                        |                                                                                                                                    |
| Replace                   | arrName[index]=value                                   | fruits[2]='Guava'; `//['Apple',{name:'Mango'},'Guava',function(){alert('Pineapple')}]`                                             |
|                           | arrName.splice(start,end,value)                        | fruits.splice(0,1,'Mosambi'); `//['Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')}]`                                  |
| Add                       | arrName[index]=value                                   | fruits[4]='Orange'; `//['Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange']`                                   |
|                           | arrName.push(value)// Add last element                 | fruits.push('Grapes'); `//['Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange','Grapes']`                       |
|                           | arrName.unshift(value)// Add first element             | fruits.unshift('Banana'); `//['Banana','Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange','Grapes']`        |
|                           | arrName.splice(start,0,value)// add to specific index  | fruits.splice(1,0,'Apple'); `//['Banana','Apple','Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange','Grapes']` |
| Delete                    |                                                        |                                                                                                                                    |
| Delete array elements     | delete arrName[index]                                  | delete fruits[0]; `// [empty,'Apple','Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange','Grapes']`             |
|                           | arrName.pop() // delete last element                   | fruits.pop(); `// [empty,'Apple','Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange']`                          |
|                           | arrName.shift() // delete first element                | fruits.shift(); `// ['Apple','Mosambi',{name:'Mango'},'Guava',function(){alert('Pineapple')},'Orange']`                              |
|                           | arrName.splice(start,end)// delete specific element(s) | fruits.splice(4,1); `// ['Apple','Mosambi',{name:'Mango'},'Guava','Orange'] `                                                        |
|                           | arrName.length=length // truncates array               | fruits.length=2; `// ['Apple','Mosambi'];`                                                                                           |
| Delete/Reset entire array | arrName.length=0                                       | fruits.length=0; `// []`                                                                                                             |
|                           | arrName=[]                                             | fruits=[];                                                                                                                         |
|                           | arrName.splice(start,arrayLength)                      | fruits.splice(0,fruits.length);`                                                                                                    |{alert('Pineapple')},'Orange']                              	|
|                               	

# Array Iteration
| Syntax                                                                                                   | Example                                                                          |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| arrName.forEach(callback[, this]) // calls a function for each array element but returns undefined       | let arr = [1,2,3]; arr.forEach(item=>console.log(item));                         |
| arrName.map(callback[, initialvalue]) // returns a new manipulated array                                 | let arr = [1,2,3,4,5]; arr.map(item=>item*item); `//[1,4,9]`                     |
| for(let item of arrName)                                                                                 | for(let item of [1,2,3]){console.log(item)} `// 1 2 3`                           |
| arrName.keys() // returns a new array iterator object with array indices                                 | for(let key of arr){ console.log(key)}; `// 0 1 2`                               |
| arrName.values() // returns a new array iterator object with array values                                | for(let value of arr.values()){console.log(value)}; `//1 2 3`                    |
| arrName.entries() // // returns a new array iterator object with array indices and values                | for(let [index,value] of arr.entries()){console.log(index,value)}; `0 1 1 2 2 3` |
| arrName.find(callback[, this]) // returns first value that satisfies condition                           | arr.find(item=>item>1);`//2`                                                     |
| arrName.filter(callback[, this]) // returns an array that satisfies condition                            | arr.filter(item=>item>1);`//[2,3]`                                               |
| arrName.every(callback[, this]) // returns true if all elements in the array satisfy the condition       | arr.some(item=>item>1);`//true`                                                  |
| arrName.some(callback[, this]) // returns true if atleast one element in the array satisfy the condition | arr.every(item=>item>1);`//false`                                                |
|                                                                                                          | arrName.unshift(value)// Add first element                                       |
