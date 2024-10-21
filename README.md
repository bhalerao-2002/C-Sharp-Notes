# C-Sharp-Notes

## Datatypes
![{D974D263-11FF-4BFA-960D-45FCF64BD7DE}](https://github.com/user-attachments/assets/fd7d976c-b36e-4105-b214-6d47b1933e46)

## Type Casting
![image](https://github.com/user-attachments/assets/8c604b20-a448-4095-9d62-a9c8da712049)

- Converting Methods for Mannual typecasting:
  - string str = Convert.ToString(x);
  - int a = Convert.ToInt32(x);
  - double b = Convert.ToDouble(x);
  - long c = Convert.ToInt64(x);
  - bool st = Convert.ToBoolean(x);
 
## Input / Output

- Output: Console.WriteLine("HI");
- Input: Console.ReadLine()
// it waits for the input from user. But always give it in string datatype. Change it using type casting.

## Math

- Math.Max(a, b);
- Math.Min(a, b);
- Math.Abs(a);
- Math.Sqrt(a);
- Math.Round(a);

## String 
- str.Length
- str.ToUpper();
- str.ToLower();
- Concatenation (a+b);
- String Interpolation
  ```
  string firstName = "John";
  string lastName = "Doe";
  string name = $"My full name is: {firstName} {lastName}";
  Console.WriteLine(name);
  ```
- str.IndexOf('a');
- string abc = og_str.Substing(start_idx, no_of_elems);

## Conditional Statements
- if
- if..else
- else..if
- switch

## Loops
- do while
- while
- for
- foreach (string i in cars){...}

## Array 
- define the variable type with square brackets.
- e.g., string[] str, int[] arr
- int[] arr -> 1D array
- int[,] arr -> 2D array
- int[,,] arr -> 3D array
- Access in 2D array is like arr[0,3]
- Looping in 2D array is like 
```
// Also note that we have to use GetLength() instead of Length to specify how many times the loop should run:

int[,] numbers = { {1, 4, 2}, {3, 6, 8} };

for (int i = 0; i < numbers.GetLength(0); i++) 
{ 
  for (int j = 0; j < numbers.GetLength(1); j++) 
  { 
    Console.WriteLine(numbers[i, j]); 
  } 
} 
```
- Array.Sort(arr_name);

### Usefull functions on array is in System.Linq Namespace
- arr.Max();
- arr.Min();
- arr.Sum();


## Methods
- Methods/Functions only execute if they got called and are always inside the class.
- Parameters and Arguments:
  - Default Parameters
    ```
    static void Main(string country = "hue"){
      Console.WriteLine(country);
    }
    ```
  - Return Parameters
    - If we want to return the values from the function/Method then we have to use the required datatype instead of void in declaration and must include return type inside the function.
  - Named Arguments
      ```
      static void MyMethod(string child1, string child2, string child3) 
      {
        Console.WriteLine("The youngest child is: " + child3);
      }
      
      static void Main(string[] args)
      {
        MyMethod(child3: "John", child1: "Liam", child2: "Liam");
      }
      
      // The youngest child is: John
      ```
- We can do Method Overloading :- Multiple methods can have the smae name with different parameters.

# OOPS in C#

## Basics:
- A class is a template for objects, and an object is an instance of a class.
- 
