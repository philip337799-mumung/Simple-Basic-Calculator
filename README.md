# Simple-Basic-Calculator
Simple-Basic Calculator by coding with C++.

#include <iostream> 
#include <string> 
#include <cmath>

using namespace std;
 
struct calculator{
   double firstNum = 0.0, secondNum = 0.0, ans = 0.0, condition = 0;
   string opSymbol = "";
   string initiation = "";
   
 };
 
int main(){
   int i = 0; 
   calculator c1;
   cout<<"Hey, Welcome 🤗"<<endl;
   
   bool validOperation = true;
   
   while(c1.condition < i+1){
   cout<<"For start running Enter: 'start'"<<endl
       <<"For Outing Enter: 'out'"<<endl;
   cout<<"Type Here: ";  
   cin>>c1.initiation;
   
       if (c1.initiation == "start"){
       
           cout<<"\n"<<"Enter First-Num: ";
           cin>>c1.firstNum;
           cout<<"\n"<<"Enter your Operator +,-,*,/,**: ";
           cin>>c1.opSymbol;
           cout<<"\n"<<"Enter Second-Num: ";
           cin>>c1.secondNum;
   
           if (c1.opSymbol == "+"){
              c1.ans = c1.firstNum + c1.secondNum;
           }
           else if (c1.opSymbol == "-"){
              c1.ans = c1.firstNum - c1.secondNum;
           }
           else if (c1.opSymbol == "*"){
              c1.ans = c1.firstNum * c1.secondNum;
           }
           else if (c1.opSymbol == "/"){
              if(c1.secondNum == 0){
              cout<<"\nError: Division by 0 is not allowed!";
              validOperation = false; 
              }
              else{
                  cout<<"Not available!";
              }
                  c1.ans = c1.firstNum / c1.secondNum;
                  
           }
           else if (c1.opSymbol == "**"){
              c1.ans = pow(c1.firstNum, c1.secondNum);
           }
           else{
              cout<<"\n"<<"This type is not support";
           }
           c1.condition += i; 
       cout<<"\n"<<"Ans: "<<c1.ans<<"\n"<<endl;    
      
       }
       else if(c1.initiation == "out"){
           c1.condition == i-1;
           break;
       }
       else{
           cout<<"Can't read this commend. Pls try again!"<<endl<<endl;
       }    
   }
   
   
return 0;}
