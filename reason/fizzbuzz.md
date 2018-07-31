# FizzBuzz

Although I've been using Reason for some time now, I decided that I shouldn't not
only contribute to open source and develop apps, but also try to train my Reason
skills by writing algorithms regularly.

This time, it's famous FizzBuzz.

Funny thing, this is the first time I've used classical loop in Reason. Before, I was using only recursions. 
However, it this case, loop is a better option since code is more concise and readable. Initially, I tried to use recursion instead, but that was just too much of unnecessary code

```reason
let evenlyDivisible = (x, y) => x mod y === 0;

let fizzbuzz = num => {
  let criteria = (evenlyDivisible(num, 3), evenlyDivisible(num, 5));
  switch(criteria){
    | (true, true) => "FizzBuzz"
    | (true, false) =>"Fizz"
    | (false, true) => "Buzz"
    | _ => string_of_int(num)
  };
};

for (i in 1 to 100) {
  Js.log(fizzbuzz(i))
};
```
