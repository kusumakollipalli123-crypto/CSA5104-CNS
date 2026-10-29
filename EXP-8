text = input("Enter plaintext: ").upper()
keyword = input("Enter keyword: ").upper()

alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
key = ""

for ch in keyword + alphabet:
    if ch in alphabet and ch not in key:
        key += ch

print("Plain alphabet :", alphabet)
print("Cipher alphabet:", key)

encrypted = ""

for ch in text:
    if ch in alphabet:
        encrypted += key[alphabet.index(ch)]
    else:
        encrypted += ch

print("Encrypted text:", encrypted)

decrypted = ""

for ch in encrypted:
    if ch in key:
        decrypted += alphabet[key.index(ch)]
    else:
        decrypted += ch

print("Decrypted text:", decrypted)
