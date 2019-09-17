# Source code for movie name guessing game
```
import random 
# Randomly chooses an element from the list
  
name = input("What is your name?\n ") 
# Username 
  
print("Good Luck ! ", str(name),"\n") 
  
Actors = ['Cop and gangster/ Based on an Indian Mythology', 'jithu Jiladhi', 'Tamizhann DAAAAAA!', 'Actors: Yuvan, Thala, Thangamey','Actors: Ajith & Meera Jasmine', 'Actors: Dhanush & Sherin', 'Actors: Surya & Priya Mani', 'Actors: Surya & Nayanthara','Actors: Rajnikanth & Shobhana', 'Actors: RajniKanth & Priya Raman', 'Actors: Jayam Ravi & Sayyeshaa']  

movie_names = ['vikramvedha','theri','Mersal','arrambam','aanjanaya','thulluvathoilamai','rathasarithiram','aathavan','thalapathi','valli','vanamagan']
 
movie = random.choice(movie_names)
#choose a movie from the list
print("Welcome to Guess the Movie name", str(name),"!\nGuess the name of these Kollywood movies take home a prize of __________ well I'll tell that once you win the game.\n\n Here is a hint for you.\n")

x = movie_names.index(movie)
print(Actors[x]) 
#searching and printing for movie actors from  the Actors list
print("\nGuess the characters\n") 
guesses = '' 
#total number of gusses allowed 
turns = 10
  
while turns > 0: 
      
    # counts the number of times a user fails 
    failed = 0
      
    # all characters from the input 
    # movie taking one at a time. 
    for char in movie:  
          
        # comparing that character with 
        # the character in guesses 
        if char in guesses:  
            print(char) 
              
        else:  
            print("\t*") 
              
            # for every failure 1 will be 
            # incremented in failure 
            failed += 1
              
  
    if failed == 0: 
        # user will win the game if failure is 0 
        print("\nYou Win!!!!!!!!!!!!\n \n Well your Prize........Hmmmmmm BLESSINGS FROM SAI BABA")  
          
        # this print the correct movie 
        print("\nThe movie is: ", movie)  
        break
      
    # if wrong alphabet enter another alphabet 
    guess = input("\nGuess a character:") 
      
    # every input character will be stored in guesses  
    guesses += guess  
      
    # check input with the character in movie 
    if guess not in movie: 
          
        turns -= 1
          
        # if the character doesn’t match the movie 
        # then “Wrong” will be given as output  
        print("\nWrong") 
          
        # turns left for the user
        print("You have", + turns, 'more guesses') 
          
          
        if turns == 0: 
            print("\nYou Lose") 
            print("Correct Answer is :-",str(movie))
        
```
