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

# Array Iteration Methods
| Syntax                                                                                                   | Example                                                                          |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| arrName.forEach(callback[, this]) // calls a function for each array element but returns undefined       | let arr = [1,2,3]; arr.forEach(item=>console.log(item));                         |
| arrName.map(callback[, initialvalue]) // returns a new manipulated array                                 | let arr = [1,2,3,4,5]; arr.map(item=>item*item); `//[1,4,9]`                     |                           |
| arrName.keys() // returns a new array iterator object with array indices                                 | for(let key of arr){ console.log(key)}; `// 0 1 2`                               |
| arrName.values() // returns a new array iterator object with array values                                | for(let value of arr.values()){console.log(value)}; `//1 2 3`                    |
| arrName.entries() // // returns a new array iterator object with array indices and values                | for(let [index,value] of arr.entries()){console.log(index,value)}; `0 1 1 2 2 3` |
| arrName.find(callback[, this]) // returns first value that satisfies condition                           | arr.find(item=>item>1);`//2`                                                     |
| arrName.filter(callback[, this]) // returns an array that satisfies condition                            | arr.filter(item=>item>1);`//[2,3]`                                               |
| arrName.every(callback[, this]) // returns true if all elements in the array satisfy the condition       | arr.some(item=>item>1);`//true`                                                  |
| arrName.some(callback[, this]) // returns true if atleast one element in the array satisfy the condition | arr.every(item=>item>1);`//false`                                                |                                                                                                                 

# Other Array Transformation/Mutator methods
| Syntax                                                                                       | Example                               |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| arr.sort() // returns sorted array                                                           | [1,3,2].sort(); //`[1,2,3]`             |
| arr.reverse // returns reversed array                                                        | [1,2,3].reverse(); //`[3,2,1]`          |
| arr.split(separator) // splits string to array                                               | "2-3-4".split('-'); //`["2", "3", "4"] `|
| arr.join(separator) // reverse of split - joins array elements as a string                   | [1,2,3].join("-"); //`"1-2-3"`          |
| arr.reduce((accumulator,item,index,array) =>{},initial) // reduces array to one single value | [1,2,3].reduce((x,i)=>x+i,0); `//6`     |

# Other Array methods/Properties
| Syntax                                                                                                 | Example                                                     |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| arr.length // returns length of the array instance                                                     | [1,2,3].length; // `3`                                        |
| arr.toString() // returns comma separated string                                                       | [1,2,3].toString(); // `"1,2,3"`                              |
| arr.splice(start,end) // returns shallow copy in a new array -  unlike splice, does not mutate array   | [1,2,3].slice(0,1); // `[1]`                                  |
| arr.concat(val1,val2[,...valN]) // concatenates values to array when Symbol.isConcatSpreadable is true | [1,2,3].concat(4,5); // `[1, 2, 3, 4, 5]`                     |
| arr.indexOf(value) //returns first index of search element, else -1                                    | [1,2,3].indexOf(2); // `2`                                    |
| arr.includes(value) // returns boolean for searched result                                             | [1,2,3].includes(2); // `true`                                |
| arr.find(callback[, this]) //returns first element that satisfies condition                            | [1,2,3].find(x=> x>1); // `2`                                 |
| arr.filter(callback[, this]) //returns the array that satisfies condition                              | [1,2,3].filter(x=> x>1); // `[2, 3]`                          |
| Array.isArray(arr); // Global object method - checks if value is of type array                         | Array.isArray({a:1}); // `false`                              |
| let arr=[val1,val2]; let [x,y]=arr // Array destructuring - unpack array as variables                  | let arr =["a","b"]; let [x,y]=arr; console.log(x,y); // `a b` |
| let [name1,name2, ...rest]= [val1,val2,..valN] //...Rest operator assigns values after … as an array   | let [x,y,...rest]=[1,2,3,4,5]; console.log(rest[0]); //`3`    |

# Common functionalities
| Operation                               | Syntax/Example                                                            |
|-----------------------------------------|---------------------------------------------------------------------------|
| Remove duplicates from array            | arr.filter((a,b)=>arr.indexOf(a)===b)                                     |
| Sort Integer Array                      | arr.sort((a,b)=>b-a);                                                     |
| Swap variables with array destructuring | let a='Apple', b='Banana'; [a,b]=[b,a]; console.log(a,b); // `Banana Apple` |
