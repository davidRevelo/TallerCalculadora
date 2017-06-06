# TallerCalculadora
Grupo (Liz, Byron, Paul, Luis, David)
from tkinter import *
"""

from Tkinter import*


ventana=Tk()
ventana.title("CALCULADORA CIENTIFICA")
ventana.configure(bg = 'beige')# define el color de la ventana

frame=Frame(ventana)
frame.grid(column=0,row=4,padx=(30,30),pady=(30,30))
frame.columnconfigure(0,weight=1)
frame.rowconfigure(0,weight=1)

Label(ventana,text="CALCULADORA").grid(column=0,row=3)

def botones(numeros):
    global valor
    valor=valor+str(numeros)
    valores.set(valor)

def operaciones():
    global valor
    operacion=str(eval(valor))
    valores.set(operacion)
    valor=""

def borrar():
    global valor
    valor=""
    valores.set('0')
    
valor=""
valores=StringVar()
pantalla=Entry(frame,width=22,textvariable=valores,justify='right')
pantalla.grid(column=1,row=1,columnspan=5)
valores.set('0')


b1=Button(frame,text='1',width=3,command=lambda:botones(1))
b1.grid(column=1,row=4)
b2=Button(frame,text='2',width=3,command=lambda:botones(2))
b2.grid(column=2,row=4)
b3=Button(frame,text='3',width=3,command=lambda:botones(3))
b3.grid(column=3,row=4)
b4=Button(frame,text='4',width=3,command=lambda:botones(4))
b4.grid(column=1,row=3)
b5=Button(frame,text='5',width=3,command=lambda:botones(5))
b5.grid(column=2,row=3)
b6=Button(frame,text='6',width=3,command=lambda:botones(6))
b6.grid(column=3,row=3)
b7 =Button(frame,text='7',width=3,command=lambda:botones(7))
b7.grid(column=1,row=2)
b8 =Button(frame,text='8',width=3,command=lambda:botones(8))
b8.grid(column=2,row=2)
borra=Button(frame,text='DEL',width=3,command=borrar)
borra.grid(column=5,row=2)
b9 =Button(frame,text='9',width=3,command=lambda:botones(9))
b9.grid(column=3,row=2)
b0=Button(frame,text='0',width=3,command=lambda:botones(0))
b0.grid(column=1,row=5)

suma=Button(frame,text='+',width=3,command=lambda:botones("+"))
suma.grid(column=5,row=4)

resta=Button(frame,text='-',width=3,command=lambda:botones("-"))
resta.grid(column=4,row=4)

igual=Button(frame,text='=',width=12,command=operaciones)
igual.grid(column=3,row=6,columnspan = 3)

divi=Button(frame,text='/',width=3,command=lambda:botones("/"))
divi.grid(column=5,row=3)

multi=Button(frame,text='*',width=3,command=lambda:botones("*"))
multi.grid(column=4,row=3)

decimal=Button(frame,text='.',width=3,command=lambda:botones('.'))
decimal.grid(column=2,row=5)

elevar=Button(frame,text='^',width=3,command=lambda:botones('**'))
elevar.grid(column=4,row=2)

seno=Button(frame,text='sin',width=3,command=lambda:botones('sin'))
seno.grid(column=4,row=5)

coseno=Button(frame,text='cos',width=3,command=lambda:botones('cos'))
coseno.grid(column=5,row=5)

tangente=Button(frame,text='tan',width=3,command=lambda:botones('tan'))
tangente.grid(column=3,row=5)
ventana.mainloop()


