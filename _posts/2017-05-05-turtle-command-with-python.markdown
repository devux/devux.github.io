---
layout: post
title:  "Turtle Command with Python"
date:   2016-03-30 12:57:14 +0530
categories: Technical
author: devux@devakumar.mj
---

# What Is Turtle Command Problem ?
Turtle is on a N * N grid, with N obstacles. The turtle can only move F orward one position
and can turn L eft or R ight. The grid has 4 directions N, E, W, S <br/>

Assuming that the initial position of turtle is 1, 1 (bottom left corner of the grid facing North) and the grid has random obstacles in a few of its cells, given the movement instructions, find the
final position of turtle and printing the grid state will be an added plus. When there is an
obstacle, movement is not possible.<br/>



# Dividing the problem in to Two parts
1.Code to move turtle as per user instruction <br/>
2.Create a grid n*n with n hurdles <br/>

 Mostly I use ruby but this is my first code with python because we have turtle module in python it will help to solve this problem in easiest way

# 1.Code to move turtle as per user instruction

#### Importing Modules

	import turtle 
	import re 

turtle module to move a object from one place other place as per user instruction <br>
re module helps in regular expression part


#### Get Instruction from user 

	print "Enter a Instruction with the following words: F,R,L \n",
	instruct = raw_input()

	instructFilter = re.sub(r'[^flrFLR]', '', instruct)

	print "Accepted string from your Input \n"
	print instructFilter
	instructArray = list(instructFilter)



In the above snippet We can get the value from user for instruction like "ffFFFFLRRRLlrflrflrflffffff"
 and this `re.sub(r'[^flrFLR]', '', instruct)` function remove unwanted letters from the string

f- forward
r- turn right
l- turn left

#### Moving the turtle as per instruction

	totalLength = len(instructArray)
	for index in range(len(instructArray)):
	  if instructArray[index] == 'f':
		  turtle.forward(1)
	  elif instructArray[index] == 'r':
		  turtle.right(90)
	  elif instructArray[index] == 'l':
	    turtle.left(95)

	  # Last cycle of for loop
	  if index == totalLength -1:
			print turtle.pos()

Using for loop iteration process will happen for each instruction in a array-instructArray <br>
Inside conditions<br>

turtle.forward(1) - will move forward the turtle 
turtle.right(90) - will turn the turtle to right side
turtle.left(90) - will turn the turtle to left side
 and
turtle.pos() -  will print the current position of turtle

#### Code Exit from execution
	print "Press Enter to exit \n",
	process = raw_input()
	print process

put the above code into file name it with .py ex index.py and run `python index.py` you will see the out put like this

Image will come here

# 2.Create a grid n*n with n hurdles

#### Modules

	import random # module to generate random value
 random mobule helps to genrate randome no , we can use this for hurdles

#### Get N value from user

	# Initial setup
	board = []
	print "Enter N value to build grid and hurdles \n",
	grid_value = int(raw_input())

 Now the N value is stored in var grid_value

#### Build N*N Grid with N Hurdles

	for row in range(grid_value):
	  board.append([])
	  random_value = random.randint(0,grid_value-1)
	  for column in range(grid_value):
	    if column == random_value & column != 0:
	      board[row].append('1')
	    else:
	      board[row].append('0')

using for I can build N*N grid and inserted Hurdles value in random place

#### Print the Grid

	def print_board(board):
	  for row in board:
	    print " ".join(row)

	print_board(board)

Using the above code you can see the generated Grid with random Hurdles
0 - Empty point
1 - Hurdle point


Now the Pending Work is How to connect these two programs.My thought If we connected the program together we can solve the problem and we can get the exact solution for tha problem. <br>




	                                                       ****************

