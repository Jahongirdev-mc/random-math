import random as r
from colorama import Fore, init
init(autoreset=True)
print("Dastur:Random matematika")
print("iltimos faqat son kirting agar harf kirtsaz dastur ishlamaydi")
print("o`yinda 5ta xato qilasaz tugaydi")
def math_r():
    n = 0
    yes = 0
    no = 0
    while True:
        a_son = r.randint(1,100)
        b_son = r.randint(1,100)
        orta = r.randint(1,4)
        n = n + 1
        if orta == 1:
            a = '+'
            javob=a_son+b_son
        if orta == 2:
            javob = a_son*b_son
            a = 'x'  
        if orta == 3:
            a = '-'
            javob = a_son-b_son 
        if orta == 4:
            a = '/'
            javob = a_son/b_son
        sen_top = int(input(f"{n}.{a_son} {a} {b_son} ="))
        if sen_top == javob:
            print(Fore.GREEN+"to`gri javob!!!")
            yes = yes+1
        else: 
            no = no+1
            print(Fore.RED+"x (qayta urnib ko`ring)\n ")
            if n==5:
                print("o`yin tugadi")
                break
                
           
            
    return (f"Siz {yes}ta misolni to`gri ishlatiz \n")
print(math_r())            

    
