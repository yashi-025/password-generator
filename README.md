# password-generator
import string
import random
def Password(length):
    complex=input("enter the complexity level out of medium(m),difficult(d): ")
    if complex=="m":
        case=input("one uppercase is must or not(y/n): ")
        if case=="n":
            char=string.ascii_letters+string.digits
        elif case=="y":
            char=string.ascii_uppercase+string.ascii_lowercase+string.digits         
    elif complex=="d":
        case=input("one uppercase is must or not(y/n): ")
        if case=="n":
            char=string.ascii_letters+string.digits+string.punctuation
        elif case=="y":
            char=string.ascii_uppercase+string.ascii_lowercase+string.digits+string.punctuation    
    password =''.join(random.choice(char) for _ in range(length))
    return password
length =int(input("enter the desired length of password: "))
password=Password(length)
print("the generated password is: ",password)
