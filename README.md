# Blackjack
Multiplayer blackjack

print('Blackjack ')


def start():
			
			if i == 2:
				count = [0,0]
			elif i == 3:
				count = [0,0,0]	
			elif i == 4:
				count = [0,0,0,0]
			koloda = [6,7,8,9,10,11,2,3,4]*4
			import random 
			random.shuffle(koloda)

			n = int('0')
			while n<i:
				print('The turn of %d player ' %n)
				while True :
					choice = input('Get a card ?  yes/no\n')
					if choice == 'yes':
						current = koloda.pop()
						print('Denomination of this card is %d'  %current)
						count[n] += current
						if count[n]>  21 :
							print('You got %d points \n You lose' %count[n])
							break
						else:
							print('You got %d points' %count[n])
					elif choice == 'no':
						print('You got %d points!' %count[n])		
						break
				n+=1			
			res = int('0')
			chemp = int('0')
			n=0
			while n<i:
				if res<count[n] and count[n]<21:
					res = count[n]
					chemp = n
				n+=1
			print('Player number %d win' %chemp)
			game()
def game():
		
		choice = input('Play again yes/no\n')
		if choice == 'yes':
			start()
		elif choice == 'no':
			print('Goof luck')	


choice = input('Wanna play ? yes/no\n')
if choice == 'yes':
	
	choice = input('How much players 2,3,4\n')
	if choice == '2':
		i=int('2')
	elif choice == '3':
		i=int('3')
	elif choice == '4':
		i=int('4')
	start()

elif choice == 'no':
		
		print('Good luck')			

																		
