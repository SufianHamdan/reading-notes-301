# Class 03 Summary :

### lists & keys:

* map() ----> loop on the array and return output array with the same length of the input array.(the same number of values in the input array).

* To loop through an array and display each value we can use map().
by doing this (arr.map(item =>{console.log(item);})

* In the list item, each list needs a unique key(id).

* The key purpose is to specify the changing or adding or removing items in the array.by giving it a unique id.

**********************************************************************************************************************

### Spread Operator :

* Spread Operator is syntax use 3 dots to expand repeated object to arguments in list, add items to an array, combining arrays or objects.

* 1. "Copy array"
2. "seperate array to small arguments".
3. "use math function"
4. "add item to list"

* const array1=['a','b','c']

const array2=['m','n','o']

const array3=[...array1, ...array2]

array3 ---> ['a','b','c','m','n','o']

*************************************************************************************************

* let numArr =[2,4,8]

   let newNum = 6

   numArr =[...numArr, newNum]

* output -----> numArr = [2,4,8,6]

**************************************************************************************************
* let student ={
    name:'Sukina',
    age:31
};

let studentStudy ={
    study:'Engineering',
    place:'LTUC'
};

let studentInfo = {
    ...student,
    ...studentStudy
};

 * the output ------> studentInfo ={
     name:'Sukina',
    age:31,
    study:'Engineering',
    place:'LTUC'
 }

****************************************************

* First step to pass functions between components :
  create function 
where the status will change 

* The increment function take object or which we want to change , call map method to loop inside object name and increment the count inside the object which passed.
then return the object.and then update the state object.

* To pass a method from a parent to Child :
increment =(this.increment)

inside the personal object.



* child component can invoke a method :

this.props.increment (this.props.name);

****************************************************************************************************

