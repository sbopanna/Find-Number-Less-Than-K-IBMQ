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

