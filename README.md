# babycrypt
![image](https://user-images.githubusercontent.com/75444239/128935870-a387e98c-edd5-4fa3-a3ec-9db20415a90c.png)

**the problem

![image](https://user-images.githubusercontent.com/75444239/128936615-34d0a69b-9baf-48d8-8a95-dc9bb93aa22f.png)

it's clear that the problem base on the factorisation of N.

let's find now  an easy solution

after connecting to server we get:


e = 65537
n = 9205850565099355009233119992333308509057926987587516553442010262770434065524651458723071213422539739783091104957937112504373819793996033829929775503108243
c = 7373290721518384012603108696715714033444163435512092120442505886297149465422635100860419886468382605598579995038885045596223387641682763096919583716818416

hint = 571338771748514167423682983583747408415015678000205027955504564266299803503


in order to solve this problem we will use Fermat's theorem:

we have:  


N %(Q-1)= hint 
             
N-hint=K*(Q-1)


let's use Fermat's theorem with                      

s**(Q-1)=1+K'*Q
                                                  
                                                  
s**(K*(Q-1))=1+K"*Q
       
s**(K*(Q-1))-1=K"*Q

or we have

K*(Q-1)=N-hint

so we will have

s**(N-hint)-1=K"*Q



we will pick now two small  number for s, and we get:

a=2**(N-hint)-1=K"*Q

b=3**(N-hint)-1=K""*Q

all we have to do is to calculate the gcd of a and b to find :Q*gcd(Q",Q""):

but  we have a small problem , we can't calculate the gcd  because N-hint is a big number so we will limit the domain by using modulo of N and we get:

Q*gcd(Q",Q"")=gcd(a%N,b%N)

finally we factorise Q*gcd(Q",Q"") to obtain Q 

hear my implementation code:

![image](https://user-images.githubusercontent.com/75444239/128941220-0fc95415-7cc2-4137-83fd-94866ebfe9bd.png)







                                                   


                                                   


