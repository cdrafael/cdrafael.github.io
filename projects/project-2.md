---
layout: project
type: project
image: images/Scheme.png
title: Shaka Scheme
permalink: projects/shakasscheme
# All dates must be YYYY-MM-DD format!
date: 2017-01-08
labels:
  - C++
  - GoogleTest
  - GitHub
  - Scheme
summary: The UH Manoa Transpiler Project's Scheme interpreter. I was part of the Parsings/IO Team.
---

<img class="ui medium right floated rounded image" src="../images/googletest.png">

The Shaka Scheme is a scheme to c++ converter. The full Shaka Scheme team consisted of students forming two different teams. The Parsings/IO team and Core Systems team. Parsings/IO took care of the input and output cases for the project. They analyzed whatever came into our interpreter and decided what it was. Parsings/IO focused a lot on the syntax analysis and the organization of the user input. The main source code was tackled by the Core Systems team. They were responsible for data structure and things such as functions and environments. We used GoogleTest to test our code. An image of google test code can be seen on the right I was only part of this project for one semester. the very first semester. However, this project has been going on 3 semesters so far. Many things have changed from when I was in the project.

In this project, I was part of the Parsing/IO team. My main role was to parse in numbers. I dealt with integers, rationals, decimals, etc. I used classes made from the Core Systems team to take whatever number was inpuyted and identified it to the corresponding class such as integer, rational, etc. The code for integer can be seen below. As said before, I have not been with the project for two semesters so this code may be outdated or edited by someone else. At the end of the time I was a part of the project, we were able to do very simple scheme to c++ interpreting.
```
template <typename T>
bool number_integer(
   InputStream&    in,
   NodePtr         root,
   T&              interm
   ) {
	bool accept = false;
	shaka::Token token = in.peek();
	
	if(token.type == Token::Type::NUMBER) {
		
      	  	in.get();
        	interm += token.str;
        	accept = true;
    	}	

	if(checkLimit(token.str) == false) {
		accept = false;
		throw std::out_of_range("Number entered is too large");
	}

  	if (accept == true) {

		root -> push_child(
        	shaka::Number(std::stoi(token.str)));
    	}
   	return accept;
}
```
The code above is a function I made for the parser to take in integers. It is a function that returns a boolean, true if the given input is an integer and false if it is not. We had a tokenizer, which would parse in a number and return what type it was, either NUMBER, CHAR, etc. We would use the tokenizer to figure out what the input was, if it was a number, then we would continue in the function.The function would then check if the number was too large, as in bitwise too large. If both these parameters were passed, the input would be pushed onto a root as a child and saved for the rest of the code to use. 


Source: <a href="https://github.com/uhmanoa-transpiler-project/shaka-scheme"><i class="large github icon"></i>UH Manoa Transpiler Project</a>
