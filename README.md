# Concurrent Set Based on Linked List

[![Build Status](https://travis-ci.com/IST-CONCURRENCY-COURSE-2018/linked-list-set-<your_GitHub_account>.svg?token=B2yLGFz6qwxKVjbLm9Ak&branch=master)](https://travis-ci.com/IST-CONCURRENCY-COURSE-2018/linked-list-set-<your_GitHub_account>)

Under this task, you need to write a concurrent linked list from the 4th lecture.

Please, use [IntelliJ IDEA](https://www.jetbrains.com/idea/) (better) or Eclipse/Netbeans (worse) as a development environment. Do not use vim or emacs!

## Project description
This project includes the following files:

* `Set.java` contains the set interface.
* `SetImpl.java` contains a sequential set implementation. It is organized as a linked list, but does not work in concurrent environment.
* `pom.xml` contains information about the project and configuration details used by Maven.

It is simpler to use Java 8 in order not to have problems with modules.

## Task description
You need to modify `SetImpl` implementation, so it becomes safe to use this implementation from multiple threads. The implementation should be lock-free.

Please, see the slides and the corresponding chapter in ["The Art of Multiprocessor Programming"](https://www.e-reading.club/bookreader.php/134637/Herlihy,_Shavit_-_The_art_of_multiprocessor_programming.pdf) book (Chapter 9. "Linked Lists: The Role of Locking").

## Build and testing
Use `mvn test` command to test your solution. The following tests are automatically executed:

* `FunctionalTest.java` tests the basic correctness (sequential);
* `LinearizabilityTest.java` checks for linearizability (concurrent).

## Submission format
Do the assignment in this repository, and commit (and push!) your solution to submit it. 

Replace `<your_GitHub_account>` in the beginning of this file with your GitHub account before submission (two places: image and build links). This is required to show a build status in Travis.