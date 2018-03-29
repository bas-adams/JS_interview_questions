# JS_interview_questions
let mostFrequent = arr => {
  let hashMap = {};
  let count = 1;

  for(let i = 0; i < arr.length; i++){

    if(hashMap.hasOwnProperty(arr[i])){
      hashMap[arr[i]] += 1;
    }else{
      hashMap[arr[i]] = count;
    }
  }//endFor

  const getMaxValue = Math.max.apply(null, Object.values(hashMap)) ;
  const getMax = obj =>{
   return Object.keys(obj).filter( x => {
     return obj[x] == getMaxValue;
   })
  };

  return `The number ${getMax(hashMap)} is ${getMaxValue} times`;
};
mostFrequent([1, 4, 3, 5, 5, 7, 3, 5]);
