Name: The Persistent Variable
Category: Reverse Engineering
Difficulty: Medium
Points: 500
Solution: 198B
Flag: CTF{st4tic_m3mory_h4ck}

Challenge Description
Scenario:
We found a legacy binary used for validating access codes. The developers claimed that by using specific Storage Classes, they could hide the validation key from standard memory-dumping tools. Your task is to analyze how the program handles memory and find the input that unlocks the flag.

Instructions:
Download the attached binary.
Find the input required to trigger the "Success" message.
The input is the key, but the flag is what the program prints upon success.

 Hints (Configured in CTFd)
 Hint 1 (Free): "Local variables live on the Stack, but static variables live in the .data segment. Have you checked the initialized data sections in Ghidra?"
 Hint 2 (10 pts): "The check logic uses a bitwise XOR operation. If $(A \oplus B = C)$, then $(A \oplus C = B)$."
 Hint 3 (Free): "The program expects a Hexadecimal input (e.g., 0x1A2B)."
