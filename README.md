# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

var numList = [Int] ()

for index in 1...150 {
    numList.append(index)
}
print(numList)

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

var exclusiveNumList = [Int] ()
for i in 142 ..< 159 {
    exclusiveNumList.append(i)
}
exclusiveNumList = Array(exclusiveNumList.dropFirst(1))
print(exclusiveNumList)

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

var evenNumList = [Int] ()
for e in 15...80 {
    if e % 2 == 0 {
        evenNumList.append(e)
    }
}
print(evenNumList)

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

var oddNumList = [Int] ()
for o in 19...51 {
    if o % 2 != 0 {
        oddNumList.append(o)
    }
}
print(oddNumList)

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

var endsInFive = [Int] ()
for five in 1...100 {
    if five % 5 == 0 && five % 10 != 0 {
        endsInFive.append(five)
    }
}
endsInFive = Array(endsInFive.dropFirst(1))
print(endsInFive)

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

var endsInSeven = [Int] ()
for seven in 1...40 {
    if seven % 7 == 0 {
        endsInSeven.append(seven)
    }
}
print(endsInSeven)

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

var divisibleByThree = [Int] ()
for threeMultiple in 20...150 {
    if threeMultiple % 3 == 0 {
        divisibleByThree.append(threeMultiple)
    }
}
print(divisibleByThree)

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`


var multipleOfTwoThree = [Int] ()
for divByTwoThree in 20...150 {
    if divByTwoThree % 2 == 0 && divByTwoThree % 3 == 0 {
        multipleOfTwoThree.append(divByTwoThree)
    }
}
print(multipleOfTwoThree)

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

var endsWithFour = [Int] ()
for four in 20...150 {
    if four % 10 == 4 {
        endsWithFour.append(four)
    }
}
print(endsWithFour)

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

var specificNums = [Int] ()
for c in 20...150 {
    switch c {    
            case 31, 35, 40...60:
                specificNums.append(c)
            default:
                continue
    }
}
print(specificNums)

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Infinite loop because i is already greater than 3 and continually gets bigger with each loop
// Does not ever create an exit condition where i > 3 returns as false
// Essentially is a while true loop, which will always run
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i < 9) {
    i += 1
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i <= 1004) {
    i += 1
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i <= 1004) {
    if i % 2 == 0 {
        print(i)
    }
    i += 1
}
```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10

// while loop performs the actions in the block while the condition is true
// repeat-while loop performs the actions in the block until the condition is false
// outputs will still be the same because the end condition for both is when i > 10
// both perform the actions until i becomes 11

```

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

// break exits out of the entire control flow statement
// continue stops the actions of block for the current interation and resumes for the next iteration
// Ex. continue for when you want to skip the next actions in the block but continue the beginning of the loop with the next iteration
// Ex. break when you do not want to do the loop anymore for any more iterations


***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[]1
[]2
[]3
[]8
[]9
[]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[]1
[]2
[]3

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
"x = 1, y = 1"
"x = 2, y = 1"
"x = 3, y = 1"

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

for x in 0...10 {
    for y in 0...10 {
        print("(\(x),\(y))", separator: "", terminator: "  ")
    }
    print("")
}

***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

for x in 0...10 {
    for y in 0...10 {
        if x - y >= 5 || y - x >= 5{
            print("(\(x),\(y))", separator: "", terminator: "  ")
        }
    }
}

***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```
var N: Int = 1
for root in 1...N {
    print(root * root)
}

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
var N: Int = 5
var segment: String = ""
var starsPerLine = 1

for line in 1...M{
    while starsPerLine <= M {
        segment += "*"
        starsPerLine += 1
    }
    print(segment)
}

