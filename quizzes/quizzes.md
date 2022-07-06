## Java 1Z0-819

#### Q1. Given the code fragment:
```java
1  Integer[] ints = {1,2,3,4,5,6,7};
2  var list = Arrays.asList(ints);
3  UnaryOperator<Integer> uo = x -> x * 3;
4  list.replaceAll(uo);
``` 

- [ ] UnaryOperator<Integer> uo = (int x) -> x * 3;
- [ ] UnaryOperator<Integer> uo = x -> { return x*3 );
- [ ] UnaryOperator<Integer> uo = var x -> { x * 3 };
- [x] UnaryOperator<Integer> uo = (var x) -> ( x * 3 );

Which can replace line 3?

**Reasoning:** A question on knowledge of the syntax of lambda expressions and on the limitations in using the var keyword ([local variable type inference](https://docs.oracle.com/en/java/javase/16/language/local-variable-type-inference.html)).

-   ```java 
    UnaryOperator<Integer> uo = (int x) -> x * 3; 
    ```
    This option has a problem with the type of the variable. UnaryOperator\<Integer> uo requires Integer, not int.
-   ```java 
    UnaryOperator<Integer> uo = x -> { return x * 3);
    UnaryOperator<Integer> uo = var x -> { x * 3 };
    ```
    Both options have syntax problems ([lambdaexpressions](https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html)).