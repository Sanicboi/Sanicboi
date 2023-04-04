### This is an assignment only and will be deleted soon.
# Programming languages.
Nowadays there are lots of programming languages and programming in general became very popular. But why are there so many and  which one to choose? Today I will try to explain it.
# The basics: programming paradigms and types of languages
## How do languages work?
A programming language is a language with its own keywords and operators whic is translated into binary instructions. There are two main types of languages: compiled and interpreted. A compiled language is first compiled into an executable file (.exe) and then run. An interpreted language is translated during runtime (aka Just In Time compiled). Then the machine reads and executes instructions.
## Low-level vs high-level
Languages can interact with hardware at different abstraction levels. The higher the abstraction the higher the level. For example, hello world in Assembly:
```
  global _main
    extern  _GetStdHandle@4
    extern  _WriteFile@20
    extern  _ExitProcess@4

    section .text
_main:
    ; DWORD  bytes;    
    mov     ebp, esp
    sub     esp, 4

    ; hStdOut = GetstdHandle( STD_OUTPUT_HANDLE)
    push    -11
    call    _GetStdHandle@4
    mov     ebx, eax    

    ; WriteFile( hstdOut, message, length(message), &bytes, 0);
    push    0
    lea     eax, [ebp-4]
    push    eax
    push    (message_end - message)
    push    message
    push    ebx
    call    _WriteFile@20

    ; ExitProcess(0)
    push    0
    call    _ExitProcess@4

    ; never here
    hlt
message:
    db      'Hello, World', 10
message_end:
```
In c++:
```
#include <iostream>
using namespace std;

int main() {
  cout << "hello world" << endl;
  return 0;
}
```
In C#: 
```
namespace Helloworld {
  class Hello {
    public static void main (string[] args) {
      System.Console.Writeln("Hello world");
    }
  }
}
```
In JavaScript: 
```
console.log('Hello world');
```
In php:
```
<?php
$echo "Hello world"
?>
```
But amount of lines of code does not make your language low or high level. For example in C# it is just boilerplate code that gives the length.
## Paradigms
There are two main paradigms: object-oriented and fucntional. Object-oriented languages are more common among developers while functional are more common among scientists.
### Object-Oriented programming paradigm
Here are some examples in c++:
```
#include <iostream>
#include <string>
using namespace std;

class Animal {
  public:
    Animal(string name) {
      this->name = name;
    }
    const void sayName() {
      cout << this->name << endl;
    }
  private:
    string name; 
}

class Dog : public Animal {
  public:
    Dog(string name, int age): Animal(name), age(age);
    void bark() {
      cout << "Woof" << endl;
    }
  private:
    int age;
}

int main() {
  Animal animal("Pet");
  animal.sayName(); // "Pet"
  Dog dog("Puppy", 4);
  dog.sayName(); // "Puppy"
  dog.bark(); // "Woof"
  return 0;
}
```
As you can see, we\`ve created two classes, one of which inherits another one. This paradigm is especially useful in games, 3d, etc, because it is easier to represent everything as an object of some class. Languages: c++, c#, java, javascript, php, python, lua, objective-c, swift, go, ruby and so on.
### Functional
No examples here. Functional programming is used in maths, because it represents functions as a dependency of some kind/ Languages: Matlab, erlang, elixir, scala, etc.
# Individual examples and usage.
## JavaScript
Hello world in JS:
```
console.log('hello world');
```
Usage: web apps, native and desktop apps, servers, automation and games.
## php
Hello world in php:
```
<?php
$echo "hello world"
?>
```
Usage: web apps, servers.
## c++
Hello world in c++:
```
#include <iostream>
using namespace std;

int main() {
  cout << "hello world" << endl;
  return 0;
}
```
Usage: web servers, native and desktop apps, games, 3d, machines, engineering, servers, OS development and so on.
## C#
```
namespace Helloworld {
  class Hello {
    public static void main (string[] args) {
      System.Console.Writeln("Hello world");
    }
  }
}
```
Usage: web servers, games, 3d, windows/desktop apps.
# Ending.
These are just the ones that I know. There are a lot of languages in different industries so that you can use them. 
