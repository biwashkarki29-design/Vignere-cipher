#!/usr/bin/env python3

import sys
import secrets

# Expect exactly 2 arguments: n and filename
if len(sys.argv) != 3:
    print(f"Invalid number of arguments. \nEnter length of key to generate and filename.")
    sys.exit(1)

# Parse number of bytes
try:
    n = int(sys.argv[1])
    if n <= 0:
        raise ValueError
except ValueError:
    print("Error: length of key must be a positive integer")
    sys.exit(1)

# Output filename
filename = sys.argv[2]

key = secrets.token_bytes(n)

print(f"Generating key of length {n} bytes into file '{filename}'")
#print(f"Your Key = {key}")

with open(filename, "wb") as f:
    f.write(key)


