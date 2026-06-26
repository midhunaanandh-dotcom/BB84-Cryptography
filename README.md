# BB84Cryptography
Welcome to my first ever project - I chose to model BB84 Cryptographic technique, which is one of the earliest Quantum Key Distribution Systems, developed by Charles Bennett and Gilles Brassard in the year 1984.
A Quantum Key Distribution(QKD) is essentially a key used by people to encrypt their data and transmit it without risking corruption or mishandling by an eavesdropper.

The key roles include the sender(Alice), receiver(Bob) and eavesdropper(Eve). The workflow is as follows: 
* Alice generates a random string of bits of chosen length(which is usually over 1000 bits - but under computational limits, upto 500 bits are used)
* She then chooses random bases of the same length to encode the bits and send them to Bob as photons
* Bob then measures these qubits, collapsing its state, using the random bases that he generated
* Alice and Bob later publicly reveal their bases - they will keep the bits whose bases match and discard the rest - and probabilistically, around half of them remains
* These bits are then used as the key for data transmission
* To verify that an eavesdropper didn't intercept, they will both reveal a substring of their respective keys and look for discrepencies
* If Eve was truly present, the error rate would be over 0%(assuming ideal conditions - not a noisy environment) so Alice and Bob will discard their bits and start over
