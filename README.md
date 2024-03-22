# Find-Number-Less-Than-K-IBMQ
This project, part of the Quantum Open Source Foundation's (QOSF) Quantum Computing Mentorship Program - cohort 9, aims to identify numbers within a list that are less than a reference number using quantum computer programming.

#Problem Statement:

Given a positive integer "k" and a list of integers, the goal is to find numbers within the list that are less than "k".

#Example:

A = less_than_k (7,[4,9,11,14,1,13,6,15])
print(A)

“4,1,6”

#Solution:

Utilizing Qiskit's built-in IntegerComparator library function, this project compares integers against a static value, setting the most significant bit (MSB) based on the comparison result.

The IntegerComparator function compares an integer against a static value - the flag 'geq' deteremines if the MSB needs to be set to 1 
when number is greater or lesser (if geq is True, the MSB is set to 1 when number is greater than the value compared against and if false, the MSB is set to 1 when number is lesser than the value compared against).


#Explanation for Qubit Length Determination:

The number of qubits required in the comparator circuit is determined by the length of the binary representation for the largest number in the list. For example, if the largest number falls between 8 and 15, 4 qubits will be needed; similarly, if the largest number is between 16 and 31, 5 qubits would be required.

The following table illustrates as an example, the number of qubits required for a range of numbers that are the largest in the list provided

<img width="669" alt="Screen Shot 2024-03-22 at 2 19 08 PM" src="https://github.com/sbopanna/Find-Number-Less-Than-K-IBMQ/assets/29610175/1adcb3c2-1d48-4076-9a8e-d9dcf135db43">

When a comparator value of 7 is used and the largest number to be compared in the list is 17 (represented by the binary string 10001), the initial step involves generating and comparing all numbers in the range 0 to 31 (00000 - 11111) with the static integer 7. In the simulation, the result set marks all integers from 0 to 6 as lesser than. This derived list from the quantum circuit result set is then compared with the supplied list to determine the existence of values in the list, thereby identifying which numbers in the supplied list are lower than the comparator.

The Circuit and the Result for the problem set provided as a part of the QOSF evaluation:

<img width="328" alt="Screen Shot 2024-03-22 at 2 02 49 PM" src="https://github.com/sbopanna/Find-Number-Less-Than-K-IBMQ/assets/29610175/1dabcac2-cf88-4e63-ae59-313ebe35f436">


#Example # 2:

A = less_than_k(25,[2,3,7,9,4,22,25,1,32])


The Circuit and the Result for this second example problem set:

<img width="385" alt="Screen Shot 2024-03-22 at 2 07 29 PM" src="https://github.com/sbopanna/Find-Number-Less-Than-K-IBMQ/assets/29610175/3712b3e8-b329-4343-a97b-0b899453cbf7">


# References 
[1] Deutsch, David, and Richard Jozsa. "Rapid solution of problems by quantum computation." Proceedings of the Royal Society of London. Series A: Mathematical and Physical Sciences 439.1907 (1992): 553-558.

[2] Bernstein, Ethan, and Umesh Vazirani. "Quantum complexity theory." SIAM Journal on computing 26.5 (1997): 1411-1473.

[3] Grover, Lov K. , "A fast quantum mechanical algorithm for database search", Proceedings of the 28th Annual ACM Symposium on the Theory of Computing (1996), arXiv:quant-ph/9605043

[4] Qiskit Documentation - https://docs.quantum.ibm.com/api/qiskit/0.26/

[5] John A. Cortese, Timothy M. Braje "Loading Classical Data into a Quantum Computer"

[6] Rubens Viana Ramos, Paulo Benício Melo de Sousa and David Sena Oliveira, "Solving mathematical problems with quantum search algorithm"

[7] Ashish Mandoi, "Quantum Search on an unstructured input -  https://github.com/AsishMandoi/quantum-search"





