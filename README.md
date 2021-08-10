# babycrypt
![image](https://user-images.githubusercontent.com/75444239/128935870-a387e98c-edd5-4fa3-a3ec-9db20415a90c.png)


the problem

![image](https://user-images.githubusercontent.com/75444239/128936615-34d0a69b-9baf-48d8-8a95-dc9bb93aa22f.png)

it's clear that the problem base on the factorisation of N.

let's find now  an easy solution.

after connecting to server we get:


e = 65537
n = 9205850565099355009233119992333308509057926987587516553442010262770434065524651458723071213422539739783091104957937112504373819793996033829929775503108243
c = 7373290721518384012603108696715714033444163435512092120442505886297149465422635100860419886468382605598579995038885045596223387641682763096919583716818416

hint = 571338771748514167423682983583747408415015678000205027955504564266299803503


in order to solve the problem we will use fermat theorem:

we have:  


N %(Q-1)= hint 
             
N-hint=K*(Q-1)


let's use ferma theorem with                      

s**(Q-1)=1+K'*Q
                                                  
                                                  
s**(K*(Q-1))=1+K"*Q
       
s**(K*(Q-1))-1=K"*Q

                                                   


                                                   


