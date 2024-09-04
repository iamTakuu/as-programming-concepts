Okay so to explain this section, we're gonna build a **Calculator** mini program using functions and procedures (aka methods). As far as I am concerned you don't have to do a lot of of complex stuff in terms of structured programming, but this [[#Practical]] should help a bit. *Please do your own extra work*.

Now on a very basic overview, procedures and functions achieve the same core principals. They are merely small bits of code/instructions that can and will be reused in different parts of your program. According to some random stack overflow post, you can *differentiate* between the two on the following principles:

> *A **function** returns a value and a **procedure** just executes commands.*
> *The name **function** comes from math. It is used to calculate a value based on input.*
> *A **procedure** **is** **a** set of command which can be executed in order.*
> *In most programming languages, even **functions** can have a set of commands. Hence the **difference** **is** only in the returning a value part.*

By utilising these two, you can write cleaner, isolated code which is easier to read, debug, and modify in the long run. Every programmer should master how to abstract their programs appropriately. 
## Practical

So the problem we wanna solve has been solved a million times and well no point going over all the lil formalities. We want a program that will *add, subtract, multiply and divide* off two given numbers.

### Procedure Approach

So with this approach we won't pass any values to our "subprograms" or procedures. They will work with global values and perform operations based of the users selected choice.

***NB**: I wouldn't recommend this approach at all because storing values [globally](https://www.geeksforgeeks.org/local-and-global-variables/) then modifying them elsewhere will always cause headaches.*

```cs
public static void Main(string[] args)  
{  
    // Simply call in main. 
    // We can easily reuse it too 
    Add(4, 5); // 9  
    Add(1, 2); // 3 
    Add(-8, 2); // -6  
}  
// Methods do not need to have parameters, but  
// in this scenario it makes sense. So it takes in 'a' and 'b'  
// Notice how it handles everything internally.  
private static void Add(int a, int b)  
{  
    float answer = a + b;  
    Console.WriteLine(answer);  
}
```

This approach is super clean and quite easily to follow through with, but it does create some issues. What happens if we need to combine different operations...like a function, eg: $(a+b) * 2$ 

## Functional Approach

When programming with functions, we can expect a value, this value can then be used for other things within another function entirely! We can essentially transform and combine data :D

```cs
public static void Main(string[] args)  
{  
    //Simply call in main.  
    //As per the example: (a+b)*2    var a = 1.5f;  
    var b = 1.5f;  
    float answer = Multiply(Add(a,b),2);  
    Console.WriteLine(answer);  
  
}  
//Functions on the other hand need parameters.  
//They will ALWAYS return a value...  
//This allows for some handy "functionality"  
private static float Add(float a, float b)  
{  
    // Returning a float with the answer.  
    // We chose float because it allows for more precise operations 
    return a + b; 
}  
// Multiply function.  
private static float Multiply(float a, float b)  
{  
    return a * b;  
}
```

### Conclusion

Idk. Lol. But this stuff is the core fundamental nature of most programming stuff. It gets super complex and all that jazz, but this helps. Anyway here's your "homework":

> **Now that you can make simple functions, add a way for your "Main" function to call different functions based on a users input, ie: 1 - Add, 2 - Subtract, 3 - Multiply, etc.**

You're gonna have to learn how to utilise [[Conditionals]]. Give [this](https://www.geeksforgeeks.org/conditional-statements-in-programming/) a look too.