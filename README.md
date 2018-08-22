# rock-paper-scissor-game
from tkinter import *
root=Tk()
def show_answer():
  p=player.get()
  c=computer.get()
  if p==c:
   print("draw")
  elif p =='r' and c =='s':
   print('player wins')
  elif p =='r' and c =='p':
   print('computer wins')
  elif p=='p' and c =='s':
   print('computer wins')
  elif p=='p' and c =='r':
   print('player wins')
  elif p=='s' and c=='p':
   print('player wins')
  elif p =='s' and c =='r':
   print('computer wins')
 
   
 #player=input("rock(r), paper(p), scissors(s)? ")

Label(root,text='player').grid(row=0)
Label(root,text='computer').grid(row=1)
Label(root,text='winner').grid(row=2)

player=Entry(root)
computer=Entry(root)
blank=Entry(root)


player.grid(row=0,column=1,sticky=E)
computer.grid(row=1,column=1,sticky=E)
blank.grid(row=2,column=1,sticky=E)

Button(root, text='Quit', command=root.destroy).grid(row=4, column=0, sticky=W, pady=4)
Button(root, text='show winner', command=blank).grid(row=4, column=1, sticky=W, pady=4)

root.mainloop()



