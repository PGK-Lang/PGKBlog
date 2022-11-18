---
title: Lesson Plan For Sections 8 and 10 (Unit 3)
description: Lesson Plan For Sections 8 and 10 (Unit 3)  
comments: false
permalink: /posts/lesson
layout: post
---

> Referenced from the [APCSP course & exam description by collegeboard](https://apcentral.collegeboard.org/media/pdf/ap-computer-science-principles-course-and-exam-description.pdf)

## Goals
 - Section 8: Iteration
   - 2.A Represent algorithmic processes without using a programming language.
   - 2.B Implement and apply an algorithm.
   - 4.B Determine the result of code segments
 - Section 10: Lists
   - 2.A Utilize such as append and remove methods to mutate lists
   - 2.B Implement and apply an algorithm using iteration
   - 4.B Determine the result of code segments

## Planned Homework/Hacks
- Section 8:
    - Implement an algorithmic process with iteration to manipulate data
        - Includes I/O 
        - Write pseudocode
        - ```python
            # Manipulate data and filter out odd numbers

            data = [1,2,3,4,5,6,7,8,9,10]
            new_data = []

            for num in data:
                if num % 2 == 1:
                    continue
                else:
                    new_data.append(num)


            print(data)
            print(new_data)
            ```
    - Example: 
      - Fibonnaci sequence using iteration by use of a while loop.
      - ```python
            x = 2
            
            # Uses a while loop to iterate through numbers of the fibonacci sequence and stops at the number that which is a factor of 12
            while (True):
                x = x + (x-1)
                print(x)

                if(x % 12 == 0): break
        ```
- Section 10: 
    -  Compare lists & typical variables
       -  Access values by index
       -  Useful for iteration
    -  Can be mutated & modified
       -  ```python
            class_list = ["rohin", "rohin2", "rohin3"]
            
            # removes name from list if false is returned when called
            for name in class_list:
                if not bool(input(name)): class_name.remove(name)
        ```
    -  

