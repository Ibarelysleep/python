#pythoncodetocrackapassowrd

psswrd = int(input("Enter the password you wish to test:\n"))
psswrdlen = len(psswrd)
characters = ["1", "2", "3", "4", "5", "6", "7", "8", "9", "0",\
 "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m",\
 "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
Status = "ongoing"

def crack():
    global psswrd, status, psswrdlen
    count = 0    
    while status == "ongoing":
        guess = ""
        while len(guess) < psswrdlen:
            guess += random.choice(characters)
        # Compare guess to the real password
        if guess == psswrd:
            print("Password cracked!: " + str(guess))
            status = "finished"
            count += 1
            print(str(count) + " guesses")
        else:
            count += 1
            
while password != "":
    status = "ongoing"
    crack()
    print("________")
    psswrd = str(input("Enter another password you wish to test:\n"))
    psswrdlen= len(psswrd)
