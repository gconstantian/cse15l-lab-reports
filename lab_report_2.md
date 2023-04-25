# Lab Report 2

Hello!! Welcome to the second part of the CSE15l journey. Here we are going to learn how to setup a local server and debug different methods!

## StringServer

Here is the code I wrote to create a local server that adds new lines of text each time you enter /add-message?s=<String of your chose>
  

![Image](StringerServer.jpg.png)

**Screen Shot 1**

![Image](Lab3SS1.jpg.png)
  
 The method that was called for this to function was handleRequest
  
  * this worked by the method seeing that the url contained /add
  
  * next it split the url after the = sign and proceeded to make that an object called newMessage
  
  * newMessage includes the string and a new line
  
  * the newMessage is added to an empty string called message
  
  * this is finally returned so we get all of the strings each time we run the url
  
  
**Screen Shot 2**

![Image](Lab3SS2.jpg.png)
  
The method that was called for this to function was handleRequest
  
  * this worked by the method seeing that the url contained /add
  
  * next it split the url after the = sign and proceeded to make that an object called newMessage
  
  * newMessage includes the string and a new line
  
  * the newMessage is added to an empty string called message
  
  * this is finally returned so we get all of the strings each time we run the url
  
  ## Debuggin
  
Below is code that would produce a bug
  
  ```
import java.util.ArrayList;
import java.util.List;

interface StringChecker { boolean checkString(String s); }

class check implements StringChecker{
  public boolean checkString(String s){
    if (s.equals("apple")){
      return false;
    }
    else{
      return true;
    }
  }
}
class ListExamples {

  // Returns a new list that has all the elements of the input list for which
  // the StringChecker returns true, and not the elements that return false, in
  // the same order they appeared in the input list;
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(s);
      }
    }
    return result;
  }
```

