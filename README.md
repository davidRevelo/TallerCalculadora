# TallerCalculadora
Grupo (Liz, Byron, Paul, Luis, David)
from tkinter import *
#FUNCIONES
def uno(): 
    print('1')
def dos(): 
    print('2')
def tres(): 
    print('3')
def cuatro(): 
    print('4')
def cinco(): 
    print('5')
def seis(): 
    print('6')
def siete(): 
    print('7')
def ocho(): 
    print('8')
def nueve(): 
    print('9')
def diez(): 
    print('0')    
    
    
    
    

tk= Tk()
btn1 = Button(tk, text="1", command=uno)
btn2 = Button(tk, text="2", command=dos)
btn3 = Button(tk, text="3", command=tres)
btn4 = Button(tk, text="4", command=cuatro)
btn5 = Button(tk, text="5", command=cinco)
btn6 = Button(tk, text="6", command=seis)
btn7 = Button(tk, text="7", command=siete)
btn8 = Button(tk, text="8", command=ocho)
btn9 = Button(tk, text="9", command=nueve)
btn0 = Button(tk, text="0", command=diez)

btn1.pack()
btn2.pack()
btn3.pack()
btn4.pack()
btn5.pack()
btn6.pack()
btn7.pack()
btn8.pack()
btn9.pack()
btn0.pack()

tk.mainloop()