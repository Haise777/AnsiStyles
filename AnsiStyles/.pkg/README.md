AnsiStyles
====

Lightweight, simple library that provides an easy and intuitive way for adding color to your console applications, allowing you to add multiple different colors and styles to the same string variable.  
Comes with 256 colors and 4 font styles for both background and foreground.  
  

![Static Badge](https://img.shields.io/badge/.NET-6.0+-%233502b8?style=flat-square) ![NuGet Version](https://img.shields.io/nuget/v/AnsiStyles?style=flat-square&logo=nuget&color=%23007bc2) ![NuGet Downloads](https://img.shields.io/nuget/dt/AnsiStyles?style=flat-square&logo=nuget&color=%230064c2) ![GitHub License](https://img.shields.io/github/license/Haise777/OPZBot?style=flat-square&color=%23a38802)  
  
  
Usage
----

Here's a simple code demonstrating all you need to know about the intended use case of this library.
```csharp
var rs = StringStyle.Reset;
var fc = StringStyle.Foreground;
var prpl = fc[129];

string text = $"This is {prpl}purple{rs} and this is {fc[196]}red{rs}";
Console.WriteLine(text); //Will print out 'text' with purple and red colored

//Can also use some ANSI code for styling 
var boBlue = fc[21].Bold().Outline();
Console.WriteLine(fc[70].Faint() + "some text" + $"{boBlue} bold outlined blue{rs}");

//You can also concat it with regular strings
var text2 = fc.Yellow + "This is yellow " + rs + prpl + "and this is purple";
Console.WriteLine(text2);
Console.WriteLine("Look, i'm still purple!");

Console.WriteLine(rs);                //Remember to always apply reset to the end of the strings
Console.WriteLine("i'm normal now!"); //Or you can just print the reset out, else the applied color/style
                                      //will keep bleading in subsequent prints until it finds a reset

//All of the above but for the background of the string
var bc = StringStyle.Background;
Console.WriteLine(bc.White + fc.Black + "Black text with White highlighting" + rs);
    
fc.ColorTest(); //prints out all the available colors codes
bc.ColorTest();
```

Contributing
----
### Feel free to contribute
- Just fork and clone the repository
- Then commit and pull request only for the `dev` branch.

Support
----
- If you encouter a bug or would like to request a feature, [please submit an issue](https://github.com/Haise777/AnsiStyles/issues/new).
- For any other question that is not related to bugs or feature, feel free to contact me.

---
*AnsiStyles is released under [BSD 3-Clause license](https://opensource.org/license/bsd-3-clause/)*

> *Contact me*\
> *Email:* [gashimabucoro@proton.me](mailto:gashimabucoro@proton.me) &nbsp;&middot;&nbsp;
> *Discord:* [@.haise_san](https://discord.com/users/374337303897702401)

