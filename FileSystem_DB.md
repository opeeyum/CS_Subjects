# Transaction management System

## What is Transaction?
Transaction is a set of operations, upon executing which corressponds to a single logical unit of work.

## Why Transaction management system?
Since most of the operation(s) within the transaction are I/O bound, therefore inorder to increase CPU utilisation we need TMS so that when one transaction is in its I/o, other can be scheduled to CPU.

## Properties of TMS
Acronym for the TMS properties is **A C I D**.

- A: **Atomicity** :- TMS should either execute **all** the operation within the transaction or (**none**) should not execute any operation within transaction.
- C: **Consistency** :- Complete execution of any transaction should not violate any defined constraints, if not so transaction must be aborted.
- I: **Isolation** :- Execution of one transaction should not affect the execution anyother transaction.
- D: **Durability** :- Changes made by any fully completed transaction must be saved, that is change(s) made should be recoverable regardless of system crashes or any other unexpected events.

## States of Transaction
![](/Images/states_of_transaction.png)

## Concurrency Problems
Sometime concurrent execution of several transaction leads to porblems termed as Concurrency problems, which are following:
- **Dirty Read** : Reading the value of a variable for some operation but value of the variable gets updated after read.
- **Unrepeatable Read problem** : Multiple read on same variable giving the new value upon every read.
- **Lost Update** : Changes made by one transaction(s) getting overridden by some other transaction.
- **Phantom Tuple**: Trying to perform some operation on a variable that doesn't exists (deleted by some other transaction).
- **Incorrect Summary Problem**: While performing aggregate function(s) of variables, value(s) getting updated concurrently. 

## What is Schedule?
Schedule is defined as the order in which multiple transactions are going to be executed in the database.

## Serial Schedule
If transactions are getting excuted in kind of *first come first serve* fashion then the schedule is termed as Serial schedule.
> If there are **n** transaction then total number of serial schedule possible would be **n!**.

``And, total number of schedules possible (serial + non-serial) is given by``

![](/Images/total_schedule_possible.png)

Where N1, N2, ..., N*n* are the number of operation with the transaction T1, T2, ..., T*n*.

## Recoverable Schedule

## Cascadeless Schedule

## Strict Schedule

# File system in DBMS
In this topic we discuss how to store the Database files in the secondary memory of out system.

How we are going to map file records onto the disk blocks.

## 2. What is File?
File is a collection of records.

File organisation is a logical relationship among various records.
