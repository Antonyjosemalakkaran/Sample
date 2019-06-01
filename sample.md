**CS 100 – COMPUTER PROGRAMMING**

**INDIVIDUAL ASSIGNMENT**



NAME OF THE STUDENT:   ANTONY.J.MALAKKARAN

CLASS:   **S2 CS A**

ROLL NO: 40

DATE OF RESUBMISSION:05/04/18

UNIVERSITY QUESTION PAPER: JULY 2017

UNIVERSITY QUESTION NO:1

**Q:**  **What is a Variable ? How are variables declared in C ?**

A:

- C variable is a named location in a memory where a program can manipulate the data. This location is used to hold the value of the variable.
- The value of the C variable may get change in the program.
- C variable might be belonging to any of the data type like int, float, char etc.

#### **RULES FOR NAMING C VARIABLE:**

1. Variable name must begin with letter or underscore.
2. Variables are case sensitive
3. They can be constructed with digits, letters.
4. No special symbols are allowed other than underscore.

#### **DECLARING &amp; INITIALIZING C VARIABLE:**

- Variables should be declared in the C program before to use.
- Memory space is not allocated for a variable while declaration. It happens only on variable definition.
- Variable initialization means assigning a value to the variable.

| ** Type ** | **Syntax** |
| --- | --- |
| Variable declaration | data\_type variable\_name;
Example: int x, y, z; char flat, ch; |
| Variable initialization | data\_type variable\_name = value;Example: int x = 50, y = 30; char flag = &#39;x&#39;, ch=&#39;l&#39;; |

# **Variable Declaration in C Programming**

# There are two ways of declaring variable in C programming.

1. Primary Type Declaration
2. User Defined Type Declaration

-  **Primary Type Declaration**

The general syntax of declaring a variable primarily is

data\_type var1,var2,...varn;

Here, _var1_, _var2_,..._varn_ are the names of valid variables.

-  **User-Defined Type Declaration**

In C programming, a feature known as &quot;type definition&quot; is available which allows a programmer to define an identifier that represents an existing data type. The user defined identifier can be used later in the program to declare variables. The general syntax of declaring a variable by user-defined type declaration is:

typedef type identifier;

Here, _type_ is an existing data type and identifier is the &quot;new name&quot; given to the data type. Here, the new type is &#39;new&#39; only in name but not the data type.

**Consider an example:**

typedef int age;

typedef float weight;

Here, _age_ represents _int _and _weight _represent _float _which can be used later in the program to declare variables as follows:

age boy1,boy2;

weight b1,b2;

Here, _boy1_ and _boy2_ are declared as as integer data type and _b1_ &amp; _b2_ are declared as floating integer data type.

The main advantage of using user-defined type declaration is that we can create meaningful data type names for increasing the readability of a program.

Another user-defined data type is enumerated data type. The general syntax of enumerated data type is:

enum identifier {value 1,value 2,...value n};

Here,_ identifier_ is a user-defined enumerated data type which can be used to declare variables that can have one of the values enclosed within the braces. The values inside the braces are known as enumeration constants. After this declaration, we can declare variables to be of this &#39;new&#39; type as:

enum identifier v1, v2, ... vn;

The enumerated variables v1, v2, ... vn can only have one of the values value1, value2, ... valuen. The following kinds of declarations are valid:

v1=value5;

v3=value1;

### **User-defined Type Declaration Example:**

enum mnth {January, February, ..., December};

enum mnth day\_st, day\_end;

day\_st = January;

day\_end = December;

if (day\_st == February)

day\_end = November;

**THERE ARE THREE TYPES OF VARIABLES IN C PROGRAM THEY ARE,**

1. Local variable
2. Global variable
3. Environment variable

LOCAL VARIABLE

- The scope of local variables will be within the function only.
- These variables are declared within the function and can&#39;t be accessed outside the function.

EXAMPLE:

#include\&lt;stdio.h\&gt;

void test();

int main()

{

   int m = 22, n = 44;

        // m, n are local variables of main function

        /\*m and n variables are having scope

        within this main function only.

        These are not visible to test funtion.\*/

        /\* If you try to access a and b in this function,

        you will get &#39;a&#39; undeclared and &#39;b&#39; undeclared error \*/

   printf(&quot;\nvalues : m = %d and n = %d&quot;, m, n);

   test();

}

void test()

{

   int a = 50, b = 80;

        // a, b are local variables of test function

        /\*a and b variables are having scope

        within this test function only.

        These are not visible to main function.\*/

        /\* If you try to access m and n in this function,

        you will get &#39;m&#39; undeclared and &#39;n&#39; undeclared

        error \*/

   printf(&quot;\nvalues : a = %d and b = %d&quot;, a, b);

}

GLOBAL VARIABLE

- The scope of global variables will be throughout the program. These variables can be accessed from anywhere in the program.
- This variable is defined outside the main function. So that, this variable is visible to main function and all other sub functions.

EXAMPLE:

#include\&lt;stdio.h\&gt;

void test();int m = 22, n = 44;

int a = 50, b = 80;

int main()

{

   printf(&quot;All variables are accessed from main function&quot;);

   printf(&quot;\nvalues: m=%d:n=%d:a=%d:b=%d&quot;, m,n,a,b);

   test();

}

void test()

{

   printf(&quot;\n\nAll variables are accessed from&quot; \

   &quot; test function&quot;);

   printf(&quot;\nvalues: m=%d:n=%d:a=%d:b=%d&quot;, m,n,a,b);

}

ENVIRONMENT VARIABLE

- Environment variable is a variable that will be available for all C  applications and C programs.
- We can access these variables from anywhere in a C program without declaring and initializing in an application or C program.
- The inbuilt functions which are used to access, modify and set these environment variables are called environment functions.

- There are 3 functions which are used to access, modify and assign an environment variable in C. They are,

1.setenv()
2.getenv()
3. putenv()
