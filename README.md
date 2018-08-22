# rock-paper-scissor-game
from tkinter import *
root=Tk()
def show_answer():
  p=player1.get()
  c=player2.get()
  if p==c:
   print("draw")
  elif p =='r' and c =='s':
   print('player1 wins')
  elif p =='r' and c =='p':
   print('player2 wins')
  elif p=='p' and c =='s':
   print('player2 wins')
  elif p=='p' and c =='r':
   print('player1 wins')
  elif p=='s' and c=='p':
   print('player1 wins')
  elif p =='s' and c =='r':
   print('player2 wins')
 
   
 #player=input("rock(r), paper(p), scissors(s)? ")

Label(root,text='player1').grid(row=0)
Label(root,text='player2').grid(row=1)

player1=Entry(root)
player2=Entry(root)


player1.grid(row=0,column=1,sticky=E)
player2.grid(row=1,column=1,sticky=E)

Button(root, text='Quit', command=root.destroy).grid(row=4, column=0, sticky=W, pady=4)
Button(root, text='show winner', command=show_answer).grid(row=4, column=1, sticky=W, pady=4)

root.mainloop()



