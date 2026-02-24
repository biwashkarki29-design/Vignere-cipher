#!/usr/bin/env python3

import sys 

if len(sys.argv) != 3:
    print("Give both PLAINtext and keyfile name and no more!!")
    exit(1)

ciphertext_file = sys.argv[1]
key_file = sys.argv[2]

with open(ciphertext_file, "rb") as f:
    cipher = f.read()

with open(key_file, "rb") as f:
    key = f.read()

plain = bytearray()
key_len = len(key)

for i in range(len(cipher)):
    c = cipher[i]
    k = key[i % key_len]
    p = (c-k) % 256
    plain.append(p)

sys.stdout.buffer.write(plain) 

