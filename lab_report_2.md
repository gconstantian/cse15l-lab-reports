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
      return true;
    }
    else{
      return false;
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
  
  If I were to test
  
  ```
  import java.util.ArrayList;
import java.util.List;
import static org.junit.Assert.*;
import org.junit.*;
public class ListTests {
    @Test public void filter(){
        List<String> input1 = new ArrayList<>();
        input1.add("apple");
        input1.add("banana");
        input1.add("pear");
        //ListExamples.filter(input1, new check());
        assertEquals(List.of("banana", "pear"), ListExamples.filter(input1, new check()));
    }
  ```
  
  I would get a bug because we want all the elemnts that are not apple, but the code above only chooses elements that are apple
  
  If we debug the code to 
  
  ```
  public boolean checkString(String s){
    if (s.equals("apple")){
      return false;
    }
    else{
      return true;
    }
  ```
  
  Then we would get the correct output and our test of putting all elements that do not equal apple into a list would work.
  
  ## Reflection
  
  Something I learned in the last two weeks is that it is incredibly easy to make my own local website and I can do just about anything on it. Creating and using URLs has been incredibly intimidating for me and by going through the lab I realized that it is not bad to do. The user interface is also super interesting and I look forward to learning more about how to make the website itself more interactable instead of just the URL.

