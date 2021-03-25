# Batobatopik-CLI
Rock Paper Scissor Game using Command line, With 3 difficulty levels

### Python
``` Python
import random

lives = 15
score = 0


def win():
    print("*            *   *   *     *")
    print(" *          *    *   * *   *")
    print("  *   *    *     *   *  *  *")
    print("   * *  * *      *   *   * *")
    print("    *    *       *   *     *")

def lose():
    print("*          * * *     * * *   * * * *")
    print("*         *     *   *        *")
    print("*        *       *   * * *   * * *")
    print("*         *     *         *  *")
    print("* * * *    * * *     * * *   * * * *")


def gameStartEasy():
    global lives
    global score
    print(f"You have {lives} lives")
    
    while lives > 10:
        print()
        playerBet = input("EASY || r for ROCK | p for PAPER | s for scissor: ")

        if playerBet.lower() == 'r':
            print("YOU: ROCK")
            choices = ['p', 's']
            computerBet = random.choice(choices)
            if computerBet == 'p':
                print("COMPUTER: PAPER")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet == 's':
                print("COMPUTER: SCISSOR")
                win()
                print(f"You have {lives} lives left")
                score += 1
                print(f"Score: {score}")

        elif playerBet.lower() == 'p':
            print("YOU: PAPER")
            choices = ['r', 's']
            computerBet = random.choice(choices)
            if computerBet == "s":
                print("COMPUTER: SCISSOR")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet == 'r':
                print("COMPUTER: ROCK")
                win()
                print(f"You have {lives} lives left")
                score += 1
                print(f"Score: {score}")

        elif playerBet.lower() == 's':
            print("YOU: SCISSOR")
            choices = ['r', 'p']
            computerBet = random.choice(choices)
            if computerBet == 'r':
                print("COMPUTER: ROCK")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet == 'p':
                print("COMPUTER: PAPER")
                win()
                print(f"You have {lives} lives left")
                score += 1
                print(f"Score: {score}")

        else:
            print("Invalid Input!")
                
        

def gameStartMedium():
    global lives
    global score
    print(f"You have {lives} lives left")
    print(f"Score: {score}")

    while lives > 5:
        print()
        playerBet = input("MEDIUM || r for ROCK | p for PAPER | s for scissor: ")
        
        if playerBet.lower() == 'r':
            print("YOU: ROCK")
            choices = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
            computerBet = random.choice(choices)
            if computerBet >= 3:
                print("COMPUTER: PAPER")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet <= 2:
                print("COMPUTER: SCISSOR")
                win()
                print(f"You have {lives} lives left")
                score += 2
                print(f"Score: {score}")

        elif playerBet.lower() == 'p':
            print("YOU: PAPER")
            choices = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
            computerBet = random.choice(choices)
            if computerBet >= 3:
                print("COMPUTER: SCISSOR")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet <= 2:
                print("COMPUTER: ROCK")
                win()
                print(f"You have {lives} lives left")
                score += 2
                print(f"Score: {score}")

        elif playerBet.lower() == 's':
            print("YOU: SCISSOR")
            choices = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
            computerBet = random.choice(choices)
            if computerBet >= 3:
                print("COMPUTER: ROCK")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet <= 2:
                print("COMPUTER: PAPER")
                win()
                print(f"You have {lives} lives left")
                score += 2
                print(f"Score: {score}")

        else:
            print("Invalid Input!")
            

def gameStartHard():
    global lives
    global score
    print(f"You have {lives} lives left")
    print(f"Score: {score}")

    while lives > 0:
        print()
        playerBet = input("HARD || r for ROCK | p for PAPER | s for scissor: ")
        if playerBet.lower() == 'r':
            print("YOU: ROCK")
            choices = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
            computerBet = random.choice(choices)
            if computerBet > 1:
                print("COMPUTER: PAPER")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet < 2:
                print("COMPUTER: SCISSOR")
                win()
                print(f"You have {lives} lives left")
                score += 2.5
                print(f"Score: {score}")

        elif playerBet.lower() == 'p':
            print("YOU: PAPER")
            choices = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
            computerBet = random.choice(choices)
            if computerBet > 1:
                print("COMPUTER: SCISSOR")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet < 2:
                print("COMPUTER: ROCK")
                win()
                print(f"You have {lives} lives left")
                score += 2.5
                print(f"Score: {score}")

        elif playerBet.lower() == 's':
            print("YOU: SCISSOR")
            choices = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
            computerBet = random.choice(choices)
            if computerBet > 1:
                print("COMPUTER: ROCK")
                lose()
                lives -= 1
                print(f"You have {lives} lives left")
                print(f"Score: {score}")
            elif computerBet < 2:
                print("CCOMPUTER: PAPER")
                win()
                print(f"You have {lives} lives left")
                score += 2.5
                print(f"Score: {score}")
        else:
            print("Invalid Input!")


playerName = input("Input your name: ")
print()

while True:
    try:
        coins = int(input("How many Coins? : "))
        print()
        if coins > 14:
            while True:
                print(f"Hi {playerName.upper()}! Available Coins: {coins}")
                playBBP = input("Want to play BATO-BATO-PIK (15 coins) [press y if yes / press any key if no]?: ")
                
                if playBBP.lower() == 'y':
                    coins -= 15
                    print()
                    print(f"Welcome {playerName.upper()}! GOODLUCK!")
                    print(f"Available Coins: {coins}")
                    print()
                    print("                BATO-BATO-PIK")
                    print("                 LEVEL: EASY")
                    print()
                    gameStartEasy()
                    print()
                    print("                 NEXT LEVEL: MEDIUM")
                    print()
                    gameStartMedium()
                    print()
                    print("                 NEXT LEVEL: HARD")
                    print()
                    gameStartHard()
                    print()
                    print( "                 G A M E   O V E R!")
                    print(f"                     Score: {score}")
                    print( "       Your Score will be added to your available Coins")
                    coins = coins + score
                    lives = 15
                    score = 0
                    print()
                    if coins < 15:
                        print("Sorry! Not Enough Coins!")
                        print(f"Available Coins: {coins}")
                        break  
                else:
                    print(f"Thank You {playerName}!")
                    break
            print()
            exitScreen = input("Press Any key to Exit")
            break
        else:
            print("Sorry! Not Enough Coins!")
            print(f"Available Coins: {coins}")
    except:
        print("Invalid Input")
```
