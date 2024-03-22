# Find-Number-Less-Than-K-IBMQ
This is an attempt to find numbers in a list that are less than a reference number using Quantum computer programming.
This task is a part of skills assessment for the QOSF's Quantum Computing Mentorship Program - cohort 9

Problem Statement:

Given a positive integer “k” and a list of integer numbers, look for the numbers within the list, that are less than k. Consider an appropriate number of qubits and explain why your proposal is valid for all kinds of numbers in case 

Example:

A = less_than_k (7,[4,9,11,14,1,13,6,15])
print(A)

“4,1,6”

Solution:
The problem has been attempted to be solved using the built in IntegerComparator library function available in Qiskit. 

The IntegerComparator function compares an integer against a static value - the flag 'geq' deteremines if the MSB needs to be set to 1 
when number is greater or lesser (if geq is True, the MSB is set to 1 when number is greater than the value compared against and if false, the MSB is set to 1 when number is lesser thena the value compared against.

The length of the binary representation for the largest number in the list (list_n) determines the number of qubits required in the comparator circuit and hence the depth of the circuit.
For E.g., if the largest number is in the range between 8 and 15, then, length of binary string is 4 and hence 4 qubits will be needed, else, if largest number is between 16 and 31, then the length of binary string is 5 and hence 5 qubits would be required

The Circuit and the Result for the above example problem set:

