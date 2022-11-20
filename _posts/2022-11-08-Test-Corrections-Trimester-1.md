## 2014 Practice Exam MCQ Test Corrections ##
* Question 3:
  *  Original Answer: E. A method that is made private means that other classes will not be able to call it.
  *  Correct Answer: B. An accessor method lets other objects access the value of instance variables without actually changing them. The accessor method should be public.
* Question 8:
  * Original Answer: B. Choice II is not the only program that will compile without error.
  * Correct Answer C. Choice I successfully create a new object Student and assigns it to variable a of type Student using a no parameter constructor. Choice II uses a two-parameter constuctor with parameters String and int in order to successfully a create a new object Student and assign it to variable b of type Student.
* Question 17:
   * Original Answer: B. Since the size of the given array is immutable, when the program is run, no values are actually removed from the array.
   * Correct Answer: C. In the first iteration of the program, arr[3] is assigned the value[4]. In each iteration, the current value corresponding to the current index is copied to the element to the left.
 * Question 18:
    * Original Answer: C. The statement given will result in an error, since the indices for myList range from 0 to myList.size() - 1, not 1 to myList.size().
    *  Correct Answer: B. The indices for myList range from 0 to myList.size() - 1, and since Math.random() randomly generates a random float point number between 0 and 1, excluding 1, this range will be satisfied. With the int type cast, an integer index value between 0 and myList.size() - 1, inclusive, will be generated.
* Question 19:
   * Original Answer: E. The opposite of !(a != b) is (a != b), due to the precense of a logic operator. With De Morgan's Law, the logic operator && becomes || and vice versa. The opposite of (b > 7) is (b <= 7).
   * Correct Answer: B. De Morgan's Law states that !(a && b) is equal to !a || !b. After negating the first expression, we get (!(a != b)) || !(b > 7). After negative the second expression, we get (a != b) || (b <= 7).
* Question 22:
   * Original Answer: C. Objects of a subclass inherit the methods of the super class. This means that the AudioBook object can call the toString method from the Book class.
   * Correct Answer: B. Because the books array has been declared of type Book, all objects saved in books are consided the Book object regardless of their actual type. As such, any methods that are called on elements of books must be declared Book. This means that in order to call the pagesPerMinute() method on Book[0], we need to use typecasting to allow the compiler to know that the object saved in the books array at this index is actually an AudioBook object.
* Question 23:
   * Original Answer: D. This would've been the result if the loop condition was k > 1 instead of k > 0. In other words, this would've been the output if the loop incremented one less.
   * Correct Answer: B. The loop basically looks at the element of the array at a specific index, checking if it starts with "b". If it does, then it is inserted near beginning of the array.
* Question 28:
   * Original Answer: B. If the value of n is 2 or less in the original call of the method mystery, then the loop will be skipped and x will be 1 at //Point C.
   * Correct Answer: E. The while loop implemented only interates while n is greater than 2, and //Point B is in the body of the while loop prior to any change in the value n. During this time, n will always be greater than 2.
* Question 30:
   * Original Answer: B. This would've been the result if the first substring call was word.substring(howFar, word.length()).
   * Correct Answer: C. The substring method basically returns a substring beginning at the first parameter and ending at the second parameter - 1. The result of word.substring(howFar + 1, word.length()) is "iler". The result of word.substring(0, howFar) is "com". All in all, the method will return "ilercom".
* Question 33:
   * Original Answer: C. This would be the correct answer if the boolean condition was changed from || to &&. However, since k is never incremented, || will  always be true since k will always be less than 4.
   * Correct Answer: E. Since k is never changed in the body of the while loop, it will always have a value 1 and thus less than 4. This means the boolean expression || for the while loop will always evaluate to true, and therefore lead to an infinite loop.
* Question 34:
   * Original Answer: D. Choice III uses the default constructor Point to assign center to a new Point with x and y both equal to 0. However, it attempts to update x and y, which are both private instance variables in Point, leading to a compile time error since x and y are not able to be accessed directly in the class Circle.
   * Correct Answer: B. Choice II successfully creates a new Point with x assigned to value b and y assigned to value b using the two-parameter Point constructor.
* Question 39:
   * Original Answer: E. Although the return value of recur(9) is 18, this call is made within another recursive call, which means that it is not the true final return value.
   * Correct Answer: D. The inital call recur(27) has a return value of recur(recur(9)). The inner call recur(9) returns 18, which means the outer call becomes recur(18). The call recur(18) returns recur(recur(6)). The inner call recur(6) returns 12, which means the outer call becomes recur(12). The call recur(12) returns recur(recur(4)). The inner call recur(4) returns 8, which means the outer call becomes recur(8). The call recur(8) returns 16, which is the final return value of the initial call recur(27).
* Question 40:
   * Original Answer: A. This would've been the result if System.out.println(temp); was before the recursive call to whatsItDo(temp); When the recursive call is executed, the current sequence of statements are paused.
   * Correct Answer: C. The call whatsItDo("WATCH") first assigns a substring of "WATCH" starting at 0 and ending at 3, which is "WATC", to the local variable temp. The next call sets local temp to "WAT", the call after that sets local temp to "WA", and so on. The call whatsItDo("W") reaches the base case. The call becomes whatsItDo("WA"), which prints out the value of its local variable temp, which is "W". The next call becomes whatsItDo("WAT"), which prints out "WA", the call after that beomces whatsItDo("WATC"), which prints out "WAT", and the final call whatsItDo("WATCH") prints out "WATC". After this call, all of the recursive calls in the program are complete.