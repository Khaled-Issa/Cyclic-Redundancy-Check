# Cyclic-Redundancy-Check
CRC or Cyclic Redundancy Check is a method of detecting accidental changes/errors in communication channel. 

CRC uses Generator Polynomial which is available on both sender and receiver side. An example generator polynomial is of the form like x3 + x + 1. This generator polynomial represents key 1011. Another example is x2 + 1 that represents key 101. 


Sender Side (Generation of Encoded Data from Data and Generator Polynomial (or Key)):

    The binary data is first augmented by adding k-1 zeros in the end of the data
    Use modulo-2 binary division to divide binary data by the key and store remainder of division.
    Append the remainder at the end of the data to form the encoded data and send the same.
    
Receiver Side (Check if there are errors introduced in transmission)
     Perform modulo-2 division again and if remainder is 0, then there are no errors. 
