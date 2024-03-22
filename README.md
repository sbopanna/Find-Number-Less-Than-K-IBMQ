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

Explanation for Qubit Length Determination:

The length of the binary representation for the largest number in the list (list_n) determines the number of qubits required in the comparator circuit and hence the depth of the circuit.
For E.g., if the largest number is in the range between 8 and 15, then, length of binary string is 4 and hence 4 qubits will be needed, similarly, if largest number is between 16 and 31, then the length of binary string is 5 and hence 5 qubits would be required

<img width="669" alt="Screen Shot 2024-03-22 at 2 19 08 PM" src="https://github.com/sbopanna/Find-Number-Less-Than-K-IBMQ/assets/29610175/1adcb3c2-1d48-4076-9a8e-d9dcf135db43">


The Circuit and the Result for the above example problem set:

<img width="328" alt="Screen Shot 2024-03-22 at 2 02 49 PM" src="https://github.com/sbopanna/Find-Number-Less-Than-K-IBMQ/assets/29610175/1dabcac2-cf88-4e63-ae59-313ebe35f436">


Example # 2:
A = less_than_k(25,[2,3,7,9,4,22,25,1,32])
The Circuit and the Result for the second example problem set:

<img width="385" alt="Screen Shot 2024-03-22 at 2 07 29 PM" src="https://github.com/sbopanna/Find-Number-Less-Than-K-IBMQ/assets/29610175/3712b3e8-b329-4343-a97b-0b899453cbf7">

