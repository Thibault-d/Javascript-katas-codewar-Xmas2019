# KatasDelivery

## Numbers to Letters
function switcher(x) {
  let output = '', temp;
  let table = ['', 'z', 'y', 'x', 'w', 'v', 'u', 't', 's', 'r', 'q', 'p', 'o', 'n', 'm', 'l', 'k', 'j', 'i', 'h', 'g', 'f', 'e', 'd', 'c', 'b', 'a', '!', '?', ' ']
  for (i = 0; i < x.length; i++) {
    temp = table[x[i]];
    output = output + temp;
  }
  return (output);
}

## Remove First and Last Character
function removeChar(str) {
  let output = "";
  output = str.substring(1, str.length - 1);
  console.log(output);
  return output;
}

## Vowel Count

```javascript 
function getCount(str) {
  let vowelsCount = 0, vowels = "aeiuo";
  for (i = 0; i < str.length; i++) {
    if (vowels.indexOf(str[i]) >= 0) {
      vowelsCount++;
    }
  }
  return vowelsCount;
}
```

## Sum Mixed Array
```javascript 
function sumMix(x) {
  let sum = 0;
  for (i = 0; i < x.length; i++) {
    sum = sum + Number(x[i]);
  }
  return sum;
}
```

## Count of positives / sum of negatives

```javascript 
let table = [0, 2, 3, 0, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14];

function countPositivesSumNegatives(input) {
  let out = [];
  if (input != null && input != [] && input.length > 0) {
    out = [0, 0];
    for (i = 0; i < input.length; i++) {
      if (input[i] > 0) {
        out[0]++;
      } else if (input[i] < 0) {
        out[1] += input[i];
      } else if (input[i] == 0) {
      } else {
        out = [];
      }
    }
  } else {
    out = [];
  }
  return out;
}
countPositivesSumNegatives(table);
```

## Get the mean of an array
```javascript 
function getAverage(marks) {
  let sum = 0;
  for (i = 0; i < marks.length; i++) {
    sum = sum + marks[i];
  }
  sum = sum / i;
  return Math.floor(sum);
}
```

## Find numbers which are divisible by given number
```javascript 
function divisibleBy(numbers, divisor) {
  let rem = 0, ret = [], inc = 0;
  for (i = 0; i < numbers.length; i++) {
    if (numbers[i] % divisor == 0) {
      ret[inc] = numbers[i];
      inc++;
    }
  }
  return ret;
}
```

## List Filtering
```javascript 
function filter_list(l) {
  let ret = [], inc = 0;
  for (i = 0; i < l.length; i++) {
    if (typeof (l[i]) == "number") {
      ret[inc] = l[i];
      inc++;
    }
  }
  return ret;
}
```

## Credit Card Mask
```javascript 
function maskify(cc) {
  let ret = cc.substring(cc.length - 4, cc.length);
  if (cc.length > 4) {
    for (i = 0; i < cc.length - 4; i++) {
      ret = "#" + ret;
    }
  } else {
    ret = cc.substring(cc.length - 4, cc.length);
  }
  return ret;
}
```

## Square Every Digit
```javascript 
function squareDigits(num) {
  let ret = String(num);
  let temp = "";
  for (i = 0; i < ret.length; i++) {
    temp = temp + Number(ret[i] * ret[i]);
  }
  return Number(temp);
}
```

## Flatten
```javascript 
var flatten = function (array) {
  let ret = [];
  let a = 0;
  for (i = 0; i < array.length; i++) {
    for (j = 0; j < array[i].length; j++) {
      ret[a] = array[i][j];
      a++;
    }
    if (a == 0) {
      ret = array;
    }
  }
  console.log(a);
  return ret;
}
```