"""
# TallerCalculadora
Grupo (Liz, Byron, Paul, Luis, David)
from tkinter import *
"""

from tkinter import*
import math

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
    
def sin():
    global valor
    valor = float (valor)
    valor = str(math.sin (valor))
    valores.set(valor)
    

def cos():
    global valor
    valor = float (valor)    
    valor = str(math.cos (valor)) 
    valores.set(valor)

def tan():
    global valor
    valor = float (valor)    
    valor = str(math.tan (valor)) 
    valores.set(valor)

def sec():
    global valor
    valor = float (valor)    
    valor = str(1/(math.cos (valor)))
    valores.set(valor)
    

def csc():
    global valor
    valor = float (valor)
    valor = str(1/(math.sin (valor)))
    valores.set(valor)

def cot():
    global valor
    valor = float (valor)    
    valor = str(1/(math.tan (valor)))
    valores.set(valor)
    
ventana=Tk()
ventana.title("CALCULADORA CIENTIFICA")
ventana.configure(bg = 'gray')

frame=Frame(ventana)
frame.grid(column=0,row=4,padx=(90,90),pady=(90,90))
frame.columnconfigure(0,weight=1)
frame.rowconfigure(0,weight=1)

Label(ventana,fg="black", font= ("arial", 17,"bold"),text="CALCULADORA").grid(column=0,row=3)


valor=""
valores=StringVar()
pantalla=Entry(frame,fg="black", font= ("arial", 15,"bold"),width=50,textvariable=valores,justify='right')
pantalla.grid(column=1,row=1,columnspan=5)
valores.set('0')


b1=Button(frame,fg="green", font= ("arial", 12,"bold"),text='1',width=10,command=lambda:botones(1))
b1.grid(column=1,row=4)
b2=Button(frame,fg="green", font= ("arial", 12,"bold"),text='2',width=10,command=lambda:botones(2))
b2.grid(column=2,row=4)
b3=Button(frame,fg="green", font= ("arial", 12,"bold"),text='3',width=10,command=lambda:botones(3))
b3.grid(column=3,row=4)
b4=Button(frame,fg="green", font= ("arial", 12,"bold"),text='4',width=10,command=lambda:botones(4))
b4.grid(column=1,row=3)
b5=Button(frame,fg="green", font= ("arial", 12,"bold"),text='5',width=10,command=lambda:botones(5))
b5.grid(column=2,row=3)
b6=Button(frame,fg="green", font= ("arial", 12,"bold"),text='6',width=10,command=lambda:botones(6))
b6.grid(column=3,row=3)
b7 =Button(frame,fg="green", font= ("arial", 12,"bold"),text='7',width=10,command=lambda:botones(7))
b7.grid(column=1,row=2)
b8 =Button(frame,fg="green", font= ("arial", 12,"bold"),text='8',width=10,command=lambda:botones(8))
b8.grid(column=2,row=2)
borra=Button(frame,fg="green", font= ("arial", 12,"bold"),text='DEL',width=10,command=borrar)
borra.grid(column=5,row=2)
b9 =Button(frame,fg="green", font= ("arial", 12,"bold"),text='9',width=10,command=lambda:botones(9))
b9.grid(column=3,row=2)
b0=Button(frame,fg="green", font= ("arial", 12,"bold"),text='0',width=10,command=lambda:botones(0))
b0.grid(column=1,row=5)

suma=Button(frame,fg="green", font= ("arial", 12,"bold"),text='+',width=10,command=lambda:botones("+"))
suma.grid(column=5,row=4)

resta=Button(frame,fg="green", font= ("arial", 12,"bold"),text='-',width=10,command=lambda:botones("-"))
resta.grid(column=4,row=4)

igual=Button(frame,fg="black", font= ("arial", 12,"bold"),text='=',width=32,command=operaciones)
igual.grid(column=3,row=5,columnspan = 3)

divi=Button(frame,fg="green", font= ("arial", 12,"bold"),text='/',width=10,command=lambda:botones("/"))
divi.grid(column=5,row=3)

multi=Button(frame,fg="green", font= ("arial", 12,"bold"),text='*',width=10,command=lambda:botones("*"))
multi.grid(column=4,row=3)

decimal=Button(frame,fg="green", font= ("arial", 12,"bold"),text='.',width=10,command=lambda:botones('.'))
decimal.grid(column=2,row=5)

elevar=Button(frame,fg="green", font= ("arial", 12,"bold"),text='^',width=10,command=lambda:botones('**'))
elevar.grid(column=4,row=2)

seno=Button(frame,fg="blue", font= ("arial", 12,"bold"),text='sin',width=10,command=sin)
seno.grid(column=3,row=6)

coseno=Button(frame,fg="blue", font= ("arial", 12,"bold"),text='cos',width=10,command=cos)
coseno.grid(column=4,row=6)

tangente=Button(frame,fg="blue", font= ("arial", 12,"bold"),text='tan',width=10,command=tan)
tangente.grid(column=2,row=6)

sec=Button(frame,fg="blue", font= ("arial", 12,"bold"),text='sec',width=10,command=sec)
sec.grid(column=3,row=7)

csc=Button(frame,fg="blue", font= ("arial", 12,"bold"),text='csc',width=10,command=csc)
csc.grid(column=4,row=7)

cot=Button(frame,fg="blue", font= ("arial", 12,"bold"),text='cot',width=10,command=cot)
cot.grid(column=2,row=7)


ventana.mainloop()

