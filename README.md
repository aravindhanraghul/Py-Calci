from tkinter import *

m=Tk()
m.title("Calculator")
operator=" "
textInput=StringVar()
def btnClick(numbers):
    global operator
    operator=operator+str(numbers)
    textInput.set(operator)

def btnClearDisplay():
    global operator
    operator=" "
    textInput.set(operator)

def btnEqualInput():
    global operator
    sumup=str(eval(operator))
    textInput.set(sumup)

def BackSpace(self):
    self.eq=False
    self.current="0"
    self.display(0)
    self.numbers=True

textDis=Entry(m,font=('arial',20,'bold'),textvariable=textInput,bd=30,insertwidth=4,
              bg="Powder Blue",justify='right').grid(columnspan=4)
btn7=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='7',bg="powder Blue",command=lambda :btnClick(7)).grid(row=2,column=0)
btn8=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='8',bg="powder Blue",command=lambda :btnClick(8)).grid(row=2,column=1)
btn9=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='9',bg="powder Blue",command=lambda :btnClick(9)).grid(row=2,column=2)
Addition=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='+',bg="powder Blue",command=lambda :btnClick("+")).grid(row=2,column=3)

btn4=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='4',bg="powder Blue",command=lambda :btnClick(4)).grid(row=3,column=0)
btn5=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='5',bg="powder Blue",command=lambda :btnClick(5)).grid(row=3,column=1)
btn6=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='6',bg="powder Blue",command=lambda :btnClick(6)).grid(row=3,column=2)
Subs=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='-',bg="powder Blue",command=lambda:btnClick("-")).grid(row=3,column=3)

btn3=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='3',bg="powder Blue",command=lambda :btnClick(3)).grid(row=4,column=0)
btn2=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='2',bg="powder Blue",command=lambda :btnClick(2)).grid(row=4,column=1)
btn1=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='1',bg="powder Blue",command=lambda :btnClick(1)).grid(row=4,column=2)
Mult=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='*',bg="powder Blue",command=lambda:btnClick("*")).grid(row=4,column=3)

btn0=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='0',bg="powder Blue",command=lambda :btnClick(0)).grid(row=5,column=0)
btnclear=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text="C",bg="powder Blue",command=btnClearDisplay).grid(row=5,column=1)
btnE=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='=',bg="powder Blue",command=btnEqualInput).grid(row=5,column=2)
Div=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='/',bg="powder Blue",command=lambda:btnClick("/")).grid(row=5,column=3)

backspace=Button(m,padx=16,pady=16,bd=8,fg="black",font=('arial',20,'bold'),text='^',bg="powder Blue",command=lambda:BackSpace("B")).grid(row=6,column=1)
m.mainloop()
