# Game2048

Title :- Project on Game 2048

1.  Introduction
Game 2048 is a single-player sliding block puzzle game designed by Italian web developer Gabriele Cirulli. The game's objective is to slide numbered tiles on a grid to combine them and create a tile with the number 2048. However, one can continue to play the game after reaching the goal, creating tiles with larger numbers.
2048 is sliding block puzzle game developed by Gabriele Cirulli. It’s a game played on a 4x4 grid with tiles numbered 2n where ‘n’ represents a natural number. The objective of the game is to combine tiles of the same number to eventually form the number 2048. The user can move in the four cardinal directions and after every move a new tile is generated randomly in the grid which is either numbered 2 or 4 with a probability of about .10. A move is legal if at least one tile can be slid into an empty spot or if the tiles can be combined in the chosen direction. The game ends when the user does not have any legal moves left. One cannot help but ask the question, since the game is based on mathematics, whether moves can be optimised to improve our score by applying different concepts of mathematics.

2.  Game 2048 Details
•	The game is played on a gray 4x4 grid, with each cell of the grid containing a tile with a number on it.
•	The numbers on the tiles are powers of two: 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096 and so on.
•	At the start of the game, two tiles are placed randomly on the grid, with each tile showing "2" or "4".
•	The player can swipe their finger on the screen in one of the four directions (up, down, left, or right), causing all the tiles on the grid to slide in that direction until they meet an obstacle (another tile or the edge of the grid).
•	When two tiles with the same number collide while sliding, they merge into a tile with the total value of the two tiles that collided.
•	A new tile will appear on the grid in a randomly selected empty cell after each move. The new tile will always have a value of "2" or "4".
•	The game is won when a tile with a value of 2048 appears on the grid.
•	The game is lost if there are no legal moves left on the grid (i.e., no empty cells and no adjacent tiles with the same value).

3. Tools
Jupyter Notebook :-  Project Jupyter is a non-profit, open-source project, born out of the IPython Project in 2014 as it evolved to support interactive data science and scientific computing across all programming languages. Jupyter will always be 100% open-source software, free for all to use and released under the liberal terms of the modified BSD license.
Jupyter is developed in the open on GitHub, through the consensus of the Jupyter community. For more information on our governance, please see our governance documentation.
All online and in-person interactions and communications directly related to the project are covered by the Jupyter Code of Conduct. This Code of Conduct sets expectations to enable a diverse community of users and contributors to participate in the project with respect and safety.
Chrome Browser :-  Just make chrome as a default browser and launch the jupyter . It will work In windows 10, you will be redirected to  jupyter notebook as usual. A new jupyter notebook tab should open in Google Chrome now.

4. Librarys Used
Python :- Python is a popular programming language. It was created by Guido van Rossum, and released in 1991.
It is used for:
•	web development (server-side),
•	software development,
•	mathematics,
•	system scripting.
What can Python do?
•	Python can be used on a server to create web applications.
•	Python can be used alongside software to create workflows.
•	Python can connect to database systems. It can also read and modify files.
•	Python can be used to handle big data and perform complex mathematics.
•	Python can be used for rapid prototyping, or for production-ready software development.
Why Python?
•	Python works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc).
•	Python has a simple syntax similar to the English language.
•	Python has syntax that allows developers to write programs with fewer lines than some other programming languages.
•	Python runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick.
•	Python can be treated in a procedural way, an object-oriented way or a functional way.
Good to know
•	The most recent major version of Python is Python 3, which we shall be using in this tutorial. However, Python 2, although not being updated with anything other than security updates, is still quite popular.
•	In this tutorial Python will be written in a text editor. It is possible to write Python in an Integrated Development Environment, such as Thonny, Pycharm, Netbeans or Eclipse which are particularly useful when managing larger collections of Python files.
Python Syntax compared to other programming languages
•	Python was designed for readability, and has some similarities to the English language with influence from mathematics.
•	Python uses new lines to complete a command, as opposed to other programming languages which often use semicolons or parentheses.
•	Python relies on indentation, using whitespace, to define scope; such as the scope of loops, functions and classes. Other programming languages often use curly-brackets for this purpose.

Tkinter library :-  Python interface to Tk
The tkinter package (“Tk interface”) is the standard Python interface to the Tcl/Tk GUI toolkit. Both Tk and tkinter are available on most Unix platforms, including macOS, as well as on Windows systems.
Running python -m tkinter from the command line should open a window demonstrating a simple Tk interface, letting you know that tkinter is properly installed on your system, and also showing what version of Tcl/Tk is installed, so you can read the Tcl/Tk documentation specific to that version.
Tkinter supports a range of Tcl/Tk versions, built either with or without thread support. The official Python binary release bundles Tcl/Tk 8.6 threaded. See the source code for the _tkinter module for more information about supported versions.
Tkinter is not a thin wrapper, but adds a fair amount of its own logic to make the experience more pythonic. This documentation will concentrate on these additions and changes, and refer to the official Tcl/Tk documentation for details that are unchanged.

Random Library :- 
This module implements pseudo-random number generators for various distributions.
For integers, there is uniform selection from a range. For sequences, there is uniform selection of a random element, a function to generate a random permutation of a list in-place, and a function for random sampling without replacement.
On the real line, there are functions to compute uniform, normal (Gaussian), lognormal, negative exponential, gamma, and beta distributions. For generating distributions of angles, the von Mises distribution is available.
Almost all module functions depend on the basic function random(), which generates a random float uniformly in the half-open range 0.0 <= X < 1.0. Python uses the Mersenne Twister as the core generator. It produces 53-bit precision floats and has a period of 2**19937-1. The underlying implementation in C is both fast and threadsafe. The Mersenne Twister is one of the most extensively tested random number generators in existence. However, being completely deterministic, it is not suitable for all purposes, and is completely unsuitable for cryptographic purposes.
The functions supplied by this module are actually bound methods of a hidden instance of the random.Random class. You can instantiate your own instances of Random to get generators that don’t share state.
Class Random can also be subclassed if you want to use a different basic generator of your own devising: see the documentation on that class for more details.
The random module also provides the SystemRandom class which uses the system function os.urandom() to generate random numbers from sources provided by the operating system.

5. Coding
from tkinter import *
from tkinter import messagebox
import random

class Board:
    bg_color={

        '2': '#eee4da',
        '4': '#ede0c8',
        '8': '#edc850',
        '16': '#edc53f',
        '32': '#f67c5f',
        '64': '#f65e3b',
        '128': '#edcf72',
        '256': '#edcc61',
        '512': '#f2b179',
        '1024': '#f59563',
        '2048': '#edc22e',
    }
    color={
         '2': '#776e65',
        '4': '#f9f6f2',
        '8': '#f9f6f2',
        '16': '#f9f6f2',
        '32': '#f9f6f2',
        '64': '#f9f6f2',
        '128': '#f9f6f2',
        '256': '#f9f6f2',
        '512': '#776e65',
        '1024': '#f9f6f2',
        '2048': '#f9f6f2',
    }

    def __init__(self):
        self.n=4
        self.window=Tk()
        self.window.title('ProjectGurukul 2048 Game')
        self.gameArea=Frame(self.window,bg= 'azure3')
        self.board=[]
        self.gridCell=[[0]*4 for i in range(4)]
        self.compress=False
        self.merge=False
        self.moved=False
        self.score=0

        for i in range(4):
            rows=[]
            for j in range(4):
                l=Label(self.gameArea,text='',bg='azure4',
                font=('arial',22,'bold'),width=4,height=2)
                l.grid(row=i,column=j,padx=7,pady=7)

                rows.append(l);
            self.board.append(rows)
        self.gameArea.grid()

    def reverse(self):
        for ind in range(4):
            i=0
            j=3
            while(i<j):
                self.gridCell[ind][i],self.gridCell[ind][j]=self.gridCell[ind][j],self.gridCell[ind][i]
                i+=1
                j-=1

    def transpose(self):
        self.gridCell=[list(t)for t in zip(*self.gridCell)]

    def compressGrid(self):
        self.compress=False
        temp=[[0] *4 for i in range(4)]
        for i in range(4):
            cnt=0
            for j in range(4):
                if self.gridCell[i][j]!=0:
                    temp[i][cnt]=self.gridCell[i][j]
                    if cnt!=j:
                        self.compress=True
                    cnt+=1
        self.gridCell=temp

    def mergeGrid(self):
        self.merge=False
        for i in range(4):
            for j in range(4 - 1):
                if self.gridCell[i][j] == self.gridCell[i][j + 1] and self.gridCell[i][j] != 0:
                    self.gridCell[i][j] *= 2
                    self.gridCell[i][j + 1] = 0
                    self.score += self.gridCell[i][j]
                    self.merge = True

    def random_cell(self):
        cells=[]
        for i in range(4):
            for j in range(4):
                if self.gridCell[i][j] == 0:
                    cells.append((i, j))
        curr=random.choice(cells)
        i=curr[0]
        j=curr[1]
        self.gridCell[i][j]=2
    
    def can_merge(self):
        for i in range(4):
            for j in range(3):
                if self.gridCell[i][j] == self.gridCell[i][j+1]:
                    return True
        
        for i in range(3):
            for j in range(4):
                if self.gridCell[i+1][j] == self.gridCell[i][j]:
                    return True
        return False

    def paintGrid(self):
        for i in range(4):
            for j in range(4):
                if self.gridCell[i][j]==0:
                    self.board[i][j].config(text='',bg='azure4')
                else:
                    self.board[i][j].config(text=str(self.gridCell[i][j]),
                    bg=self.bg_color.get(str(self.gridCell[i][j])),
                    fg=self.color.get(str(self.gridCell[i][j])))

class Game:
    def __init__(self,gamepanel):
        self.gamepanel=gamepanel
        self.end=False
        self.won=False

    def start(self):
        self.gamepanel.random_cell()
        self.gamepanel.random_cell()
        self.gamepanel.paintGrid()
        self.gamepanel.window.bind('<Key>', self.link_keys)
        self.gamepanel.window.mainloop()
    
    def link_keys(self,event):
        if self.end or self.won:
            return

        self.gamepanel.compress = False
        self.gamepanel.merge = False
        self.gamepanel.moved = False

        presed_key=event.keysym

        if presed_key=='Up':
            self.gamepanel.transpose()
            self.gamepanel.compressGrid()
            self.gamepanel.mergeGrid()
            self.gamepanel.moved = self.gamepanel.compress or self.gamepanel.merge
            self.gamepanel.compressGrid()
            self.gamepanel.transpose()

        elif presed_key=='Down':
            self.gamepanel.transpose()
            self.gamepanel.reverse()
            self.gamepanel.compressGrid()
            self.gamepanel.mergeGrid()
            self.gamepanel.moved = self.gamepanel.compress or self.gamepanel.merge
            self.gamepanel.compressGrid()
            self.gamepanel.reverse()
            self.gamepanel.transpose()

        elif presed_key=='Left':
            self.gamepanel.compressGrid()
            self.gamepanel.mergeGrid()
            self.gamepanel.moved = self.gamepanel.compress or self.gamepanel.merge
            self.gamepanel.compressGrid()

        elif presed_key=='Right':
            self.gamepanel.reverse()
            self.gamepanel.compressGrid()
            self.gamepanel.mergeGrid()
            self.gamepanel.moved = self.gamepanel.compress or self.gamepanel.merge
            self.gamepanel.compressGrid()
            self.gamepanel.reverse()
        else:
            pass

        self.gamepanel.paintGrid()
        print(self.gamepanel.score)

        flag=0
        for i in range(4):
            for j in range(4):
                if(self.gamepanel.gridCell[i][j]==2048):
                    flag=1
                    break

        if(flag==1): #found 2048
            self.won=True
            messagebox.showinfo('2048', message='You Wonnn!!')
            print("won")
            return

        for i in range(4):
            for j in range(4):
                if self.gamepanel.gridCell[i][j]==0:
                    flag=1
                    break

        if not (flag or self.gamepanel.can_merge()):
            self.end=True
            messagebox.showinfo('2048','Game Over!!!')
            print("Over")

        if self.gamepanel.moved:
            self.gamepanel.random_cell()
        
        self.gamepanel.paintGrid()
    

gamepanel =Board()
game2048 = Game( gamepanel)
game2048.start()
 
6. Output
The output of the game is a 4x4 grid of tiles that slide, merge, and appear according to the game mechanics. The game also displays the current score, the best score, and the game status (won or lost).

7. Places to Improve
•	Adding more features such as undo move, restart game, and game leaderboard.
•	Improving the user interface and user experience.
•	Optimizing the code for better performance.
•	Add Restart Option

8. Conclusion
•	The Game 2048 project is an interesting and challenging game that requires strategic thinking and planning. 
•	The project provided an opportunity to implement the game mechanics using Python and Tkinter, Random library. 
•	The game's objective is to slide numbered tiles on  agrid to combined them to create a tile with the number 2048. 
•	 However, one can continue to play the game after reaching the goal, creating tiles with larger numbers.
•	The game ends when all free spaces are used up and no two tiles can be merged.
•	There are several areas to improve, and the project can be further enhanced by adding more fe
