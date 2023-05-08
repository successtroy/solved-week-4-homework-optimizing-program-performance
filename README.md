Download Link: https://assignmentchef.com/product/solved-week-4-homework-optimizing-program-performance
<br>
<p class="ui header product-top-header" title="Week 4 Homework—Optimizing Program Performance Solution">A programmer must write correct code that is clear and concise. There are also circumstances in which a programmer must write fast and efficient code. Processing video frames in real time must be fast. We will talk about ways to optimize code.

Given the following code, perform these operations to optimize the code. See Chapter 5 in the book for more details on code optimization. Please use comments to document all optimizations you have made to the code.

1.      Using switch instead of if

2.      Eliminating length calls out of the loop test

3.      Put the most used variables first when initializing variables

4.      Use prefix operations rather than postfix operations

5.      Loop unrolling—increase the number of elements computed in each iteration of a loop (i.e. instead of processing arrays separately, if you have two arrays of the same length, process them in parallel)

6.      Any other improvements you want to make

#include &lt;iostream

#include &lt;vector

#include &lt;string

using namespace std;

#include &lt;iostream

#include &lt;vector

#include &lt;string

using namespace std;

int main()

{

//This program stores the items purchased at the grocery store. The price vector stores the prices for each item purchased.

//The product name vector stores the products purchased and the category vector stores which category the item falls under.

//Frozen foods have a 10% discount, snacks has a 5% discount, and produce has a 15% discount.

//The total amount of items purchased should be calculated with a 7% tax rate.

double sum;

double tax,totalAmount;

vector&lt;double price;

vector&lt;string productName;

vector&lt;char category;

price.push_back(4.5);

price.push_back(10);

price.push_back(1.25);

price.push_back(2.75);

price.push_back(9.50);

productName.push_back(“ice cream”); //Frozen food

productName.push_back(“pizza”);  //Frozen food

productName.push_back(“apples”); //Produce

productName.push_back(“cheesy poofs”); //Snacks

productName.push_back(“bananas”); //Produce

category.push_back(‘F’);

category.push_back(‘F’);

category.push_back(‘P’);

category.push_back(‘S’);

category.push_back(‘P’);

if (category[0]==’F’)

{

price[0]=price[0]*.9;

}

else if (category[0]==’S’)

{

price[0]=price[0]*.95;

}

else

{

price[0]=price[0]*.85;

}

if (category[1]==’F’)

{

price[1]=price[1]*.9;

}

else if (category[1]==’S’)

{

price[1]=price[1]*.95;

}

else

{

price[1]=price[1]*.85;

}

if (category[2]==’F’)

{

price[2]=price[2]*.9;

}

else if (category[2]==’S’)

{

price[2]=price[2]*.95;

}

else

{

price[2]=price[2]*.85;

}

if (category[3]==’F’)

{

price[3]=price[3]*.9;

}

else if (category[3]==’S’)

{

price[3]=price[3]*.95;

}

else

{

price[3]=price[3]*.85;

}

if (category[4]==’F’)

{

price[4]=price[4]*.9;

}

else if (category[4]==’S’)

{

price[4]=price[4]*.95;

}

else

{

price[4]=price[4]*.85;

}

sum=price[0]+price[1]+price[2]+price[3]+price[4];

for(int i=0;i&lt;price.size();i++)

{

cout&lt;&lt;“The price for item “&lt;&lt;(i+1)&lt;&lt;” is “&lt;&lt;price[i]&lt;&lt;endl;

tax=sum*.07;

totalAmount = sum+tax;

}

for(int i=0;i&lt;productName.size();i++)

{

cout&lt;&lt;“The product name for item “&lt;&lt;(i+1)&lt;&lt;” is “&lt;&lt;productName[i]&lt;&lt;endl;

}

cout&lt;&lt;“The total price is: “&lt;&lt;totalAmount&lt;&lt;endl;

cin.ignore();

return 0;

}

5/5 - (3 votes)