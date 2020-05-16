# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**
```swift
for i in 1...150 {
  print(i)
}
```

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**
```swift

for i in 142...159 where i > 142 && i < 159 {
  print(i)
}
```

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**
```swift
for i in 15...80 where i % 2 == 0 {
    print(i)
  }
```

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**
```swift
for i in 19...51 where i % 2 != 0 {
    print(i)
  }
```

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**
```swift
for i in 1...100 where if i % 5 == 0 && i % 10 != 0 {
    print(i)
  }
```
***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**
```swift
for i in 1...40 where i % 5 == 0 && i % 10 != 0 {
  print(i + 2)
}
```
***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`
```swift
for i in 20...150 where i % 3 == 0 {
  print(i)
}
```
***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`
```swift
for i in 20...150 where i % 2 == 0 && i % 3 == 0 {
  print(i)
}
```

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`
```swift
for i in 20...150 where i % 5 == 0 && i % 10 != 0 {
  print(i - 1)
}
```
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`
```swift
for i in 20...150 {
  if i == 31 || i == 35 ||  i > 40 && i < 60 {
    print(i)
  }
}

```
***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
It will keep running indefinitely because i will always be greater than 3.
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
    }
}

//re-written code below
while (i >= 3) {
  i += 1
  if i > 9 {
    break
  }
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}

//re-written code below
var i = 5
var runtime = 0

while (i > 3) {
  i += 1
  runtime += 1
  
  if runtime == 1000 {
    break
  }
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}

//re-written code below
var i = 5
var runtime = 0

while (i > 3) {
  i += 1
  runtime += 1
  
  if runtime == 1000 {
    break
  }
  
  if i % 2 == 0 {
    print(i)
  }
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
```
```
The two loops give the same output because they are both loops with the same conditions so they'll start at one and end at ten. And they have the same increments.
```
# Bonus =)

***
## Question 1

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.
```
The break statement ends execution of an entire control flow statement immediately. The break statement can be used inside a switch or loop statement when you want to terminate the execution of the switch or loop statement earlier than would otherwise be the case.

The continue statement tells a loop to stop what it is doing and start again at the beginning of the next iteration through the loop. It says “I am done with the current loop iteration” without leaving the loop altogether.
```
Example
```swift
var shields = 5
var blastersOverheating = false
var blasterFireCount = 0
var spaceDemonsDestroyed = 0

while shields > 0 {

    if spaceDemonsDestroyed == 500 {
        print("You beat the game!")
        break
    }

    if blastersOverheating {
        print("Blasters are overheated! Cooldown initiated.")
        sleep(5)
        print("Blasters ready to fire")
        sleep(1)
        blastersOverheating = false
        blasterFireCount = 0
        continue
    }

    if blasterFireCount > 100 {
        blastersOverheating = true
        continue
    }

    // Fire blasters!
    print("Fire blasters!")
    blasterFireCount += 1
    spaceDemonsDestroyed += 1
}
```

***
## Question 2

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```
Solution
```
1, 2, 3, 8, 9, 10
```

***
## Question 3

Without using Xcode, what will the loop below print?

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```
Solution
```
1, 2, 3
```

***
## Question 4

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
Solution
```
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

when y == 2 it'll skip y = 2 and y = 3 steps and continue outerloop
```

***
## Question 5

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.
```swift
//write code below 

for x in 0...10 {
  for y in 0...10 {
    print("\(x),\(y)")
  }
}
```

***
## Question 6

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

```swift 
// write code below
for x in 0...10 {
  for y in 0...10 {
  
    if x - y >= 5 || y - x >= 5 {
    
      print("(\(x), \(y))")
    }
  }
}
```
***
## Question 7

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

// write code below
var n = 1

while n < 6 {
  print(n * n)
  n += 1
}
```

***
## Question 8

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

```swift
// write code below
var n = 3

for _ in 1...n {
  for _ in 1...n {
    print("*", separator: "", terminator: " ")
}
  print(" ")
}
```
