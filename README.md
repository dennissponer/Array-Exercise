# Array-Exercise
//your code here
const arrayFlattener = (arr) => {
    const resultArray = [];
    
    for(let i=0; i<arr.length; i++) {
        if(typeof arr[i] === 'number') {
            resultArray.push(arr[i]);
        }
        if(typeof arr[i] === 'object') {
            for(let j=0; j<arr[i].length; j++) {
                resultArray.push(arr[i][j]);
            }
        }
    }
    return resultArray;
}
//uncomment next line one by one, then check the console for results
// console.log(arrayFlattener([1,[2,3],4,5]))

//don't change this line
if (typeof module !== "undefined") {
  module.exports = {
    arrayFlattener,
  };
}
