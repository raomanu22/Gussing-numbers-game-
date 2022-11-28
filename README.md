# Gussing-numbers-game-


print('Welcome To The Game Of Numbers \U0001F920')
print('Game Rules: \n If You Guess The Number In: \n 1st Try +10 \n 2nd Try +6 \n 3rd Try +3 \n')
final_score=0
played=0

def num_game():
    import random

    n=int(input('Enter Starting Range: '))
    m=int(input('Enter Ending Range: '))

    score=0
    count=0

    num= random.randint(n,m)

    while count<3:
    
        a=int(input('Guess The Number: '))
    
        if a<num:
            print('Have One More Try, Your Guess Was Too Low \U0001F605 ')

        elif a>num:
            print('Have One More Try, Your Guess Was Too High \U0001f605 ')
    
        else:
            print('Congrat\'s ,You Have Guessed It \U0001F607 ')
    
            if count==0:
                score+=10
    
            elif count==1:
                score+=6
    
            elif count==2:
                score+=3
    
            print('Your Score Is:',score,'\U0001F973 ')
            break

        count+=1

    if count==3:
        print('Better Luck Next Time \U0001F61E ')
    global final_score
    final_score+=score
    global played
    played+=1


    def choice():
        z=input('Do You Want To Play Again? (Y/N):  ')
        if z=='y' or z=='Y':
            num_game()

        elif z=='n' or z=='N':
            print('You Played',played,'Times And')
            print('Your Final Score Is:',final_score,'\U0001F389 ','\n \U0001F643 Thanks For Playing')
            
            exit()
    
        else:
            print('Invalid Input')
            
            choice()
    choice()


num_game()


