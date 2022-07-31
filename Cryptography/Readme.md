# Encrypting a message
Imagine Caesar wants to send this message:
SECRET MEETING AT THE PALACE
Here's what that might look like encrypted:
YKIXKZ SKKZOTM GZ ZNK VGRGIK
That looks an awfully lot like gobbledygook at first, but this encrypted message is actually very related to the original text.

# Decrypting a message
According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift amount, it was trivial for them to decode the message.
Imagine Caesar sends this message to a comrade:
EHZDUH EUXWXV
The comrade uses this substitution table, where the alphabet is shifted by 3:
A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C
They can then decode the message with certainty. The first letter "E" was shifted by 3 from "B", the second letter "H" was shifted by 3 from "E", etc. The result is this ominous message:
BEWARE BRUTUS
CHECK YOUR UNDERSTANDING
Here's another message Caesar might send:
FURVV WKH UXELFRQ

# Cracking the cipher
Imagine that a very literate and savvy enemy intercepts one of Caesar's messages.
RZ VMZ WMDIBDIB VGG AJMXZN OJ EJDI RDOC XGZJKVOMV OJ YZAZVO OCZ ZIZHT LPZZI VO OCZ IDGZ YZGOV
That enemy does not know that Caesar always uses a shift of 3, so he must attempt to "crack" the cipher without knowing the shift.
There are three main techniques he could use: frequency analysis, known plaintext, and brute force.
Frequency analysis
Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.

# Known plaintext
Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.
For example, messages tend to start with similar beginnings. In WWII, encrypted German messages always started with a weather forecast, which ultimately made them easier for British mathematician Alan Turing to crack.
Do you think Julius started this message in a common way?
# Brute force
There are only 25 possible shifts (not 26 — why not?). The enemy could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two.

# Encryption, decryption, and cracking
Thanks to this exploration of the Caesar Cipher, we now understand the three key aspects of data encryption:
Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).
Decryption: recovering the original data from scrambled data by using the secret key.
Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

