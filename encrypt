#!/usr/bin/env python3

import sys 

if len(sys.argv) !=3:
    print("Give both PLAINtext and keyfile name and no more!!")
    exit(1)

plaintext_file = sys.argv[1]
key_file = sys.argv[2]

with open(plaintext_file, "rb") as f:
    plaintext = f.read()

with open(key_file, "rb") as f:
    key = f.read()

#if len(key) == 0:
    #print("Error: key file is empty")

cipher = bytearray()

key_len = len(key)

for i in range(len(plaintext)):
    p = plaintext[i]
    k = key[i % key_len]
    c = (p + k) % 256
    cipher.append(c)

sys.stdout.buffer.write(cipher) #

