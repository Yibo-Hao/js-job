 ## 用递归算法实现，数组长度为5且元素的随机数在2-32间不重复的值
 ```
 let arr = [];
function re(arr) {
function getRandomInt(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min)) + min; //不含最大值，含最小值
}
  let num = getRandomInt(2,32);
  if (arr.indexOf(num) < 0) {
    arr.push(num);
    console.log(arr.length);
  } else {
    re(arr);
  }
  if (arr.length === 5) {
    return arr;
  } else {
    re(arr);
  }
  
}
 ```
 1. Math.random 实现的随机数处于0到1之间
 2. Math.ceil 和 Math.floor 的对称使用
 3. 递归要先考虑好终止条件
 4. 实现两个数之间的随机数

