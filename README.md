import math

text = input("Enter plaintext: ").upper()
a = int(input("Enter a: "))
b = int(input("Enter b: "))

if math.gcd(a, 26) != 1:
    print("Invalid value of a")
else:
    result = ""

    for ch in text:
        if ch.isalpha():
            p = ord(ch) - 65
            c = (a * p + b) % 26
            result += chr(c + 65)
        else:
            result += ch

    print("Encrypted text:", result)

    inverse = 0
    for i in range(26):
        if (a * i) % 26 == 1:
            inverse = i
            break

    result2 = ""

    for ch in result:
        if ch.isalpha():
            c = ord(ch) - 65
            p = (inverse * (c - b)) % 26
            result2 += chr(p + 65)
        else:
            result2 += ch

    print("Decrypted text:", result2)
