- 👋 Hi, I’m @Omsharmaa
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Omsharmaa/Omsharmaa is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can have a look at my recent project i.e. Number guessing game in python.
--->
print("Welcome to Our 'Number Guessing Game'. In this, you Have to guess 3 Numbers between your preferred limits....\n")
import random
p=True
while p==True:
	print('Enter 1 ; For start')#Giving Choices
	print('Enter 2 ; For exit\n')
	ch=int(input('Enter your choice: '))
	if ch==1:
		R=[];G=[] #Making two lists for showing Gussed and Actual Numbers
		c=0
		l1=int(input('\nEnter your lower limit : '))
		l2=int(input('Enter your upper limit : '))
		print()
		for i in range(3):
			n=int(input('Guess a number between your entered range : '))
			G.append(n)
			a=random.randint(l1,l2)#Making use of random module
			R.append(a)
			if n==a:
				c+=1
		if c==3:
			print('\nCongratulations !! \n You won.')
		elif c==2:
			print('\nDamn !.. you got 2 correct, you were just about to win \n Have one more try')
		elif c==1:
			print('\n1 correct !!.. Try again.')
		elif c==0:
			print('\nYou got ZERO correct... Better luck next time !!\n')
		print('\nYou Guessed :-',G)
		print('\nActual Numbers :-',R,'\n')
	if ch==2:
		p=False
