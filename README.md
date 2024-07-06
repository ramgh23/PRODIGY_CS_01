#ENCRYPT
#A python program to illustrate Caesar Cipher Technique
def encrypt(text,s):
    result = ""

    # traverse text
    for i in range(len(text)):
        char = text[i]

        # Encrypt uppercase characters
        if (char.isupper()):
            result += chr((ord(char) + s-65) % 26 + 65)

        # Encrypt lowercase characters
        else:
            result += chr((ord(char) + s - 97) % 26 + 97)

    return result

#check the above function
text = input("Enter  text: ")
s = int(input("Enter shift value: "))
print ("Text  : " + text)
print ("Shift : " + str(s))
print ("Cipher: " + encrypt(text,s))


#DECRYPT
#A python program to illustrate Caesar Cipher Technique
def decrypt(cipher,s):
    result = ""

    # traverse text
    for i in range(len(cipher)):
        char = cipher[i]

        # decrypt uppercase characters
        if (char.isupper()):
            result += chr((ord(char) - s-65) % 26 + 65)

        # decrypt lowercase characters
        else:
            result += chr((ord(char) - s - 97) % 26 + 97)

    return result
#check the above function
cipher = input("Enter  cipher: ")
s = int(input("Enter shift value: "))
print ("Cipher  : " + cipher)
print ("Shift : " + str(s))
print ("Text: " + decrypt(cipher,s))

