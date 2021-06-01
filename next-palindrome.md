# Problem - Next Palindrome
Any number that reads the same way forwards as it does backwards is a palindrome. For instance, `12321` would be considered a palindrome, whereas `123` would not be. 

Write a function that takes in an integer and returns the next palindrome. For instance:

```js
findNextPalindrome(100)
// should return 101
```

and 

```js
findNextPalindrome(101)
// should return 111
```

# Instructions

1. Copy this markdown and paste in your own, private gist
2. In your private gist, fill out the questions below
4. Submit by the due time as instructed in Zoom


## Rewrite the question in your own words:
given a number, find the next number (going up) that is the same number forward and backward.

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
I am going to assume we are not going to worry about nay negative numbers, and our given number will be greater than 0.


## What are your initial thoughts about this problem? (high level design, 2-3 sentences)
my initial thought is i will just have an until loop, starting at the given number going up by one until the number is the same forwards and backwards.

## How would you identify the elements of this problem?

- [ ] Searching of Data
- [ ] Sorting of Data
- [x] Pattern Recognition
- [ ] Build/Navigate a Grid
- [ ] Math
- [ ] Language API knowledge
- [x] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?
I'll use an until loop, but I shouldnt need to use any hashes or arrays.

## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)
First: assign a next variable = 0, and start = given number
Next: take the number we're given and create an until loop
      until next does not equal zero
      increment start by one
      check if its the same forward and backward
        if it is: return the number
        if its not: move on
        

## Write out any implementation code OR link to repl
```
class NextPalindrome
  def initialize(start)
    @start = start
  end

  def next_number
    new_num = @start
    until new_num < 1
      new_num += 1
      return new_num if palindrome?(new_num)
    end
  end

  def palindrome?(num)
    num.to_s == num.to_s.reverse
  end
end
```

## What is the Big O complexity of your solution?
I believe it is O(n), because it just has to do a simple check if its a palindrome for every number until you reach the correct number.
