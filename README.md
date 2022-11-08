# Push_Swap
 Push_Swap is a 42 school project which consist to produce a sorting Algorithm following some concepts to standardize the process; We were free to develop this project with any known or available algorithm

## RULES
- The game is composed of 2 stacks named __A__ and __B__.
- To start with:
	- A contains a random number of either positive or negative numbers without any duplicates.
	- B is empty.
- The goal is to sort in ascending order numbers into stack __A__.
- To do this, you have the following operations.

## OPERATIONS
* [`sa`](srcs/operations/sa_swap_a.c) - swap __a__: swap the first 2 elements at the top of stack __a__. (do nothing if there is only one or no elements).
* [`sb`](srcs/operations/sb_swap_b.c) - swap __b__: swap the first 2 elements at the top of stack __b__. (do nothing if there is only one or no elements).
* [`ss`](srcs/operations/ss_sa_sb.c) - ss: swap __a__ and swap __b__ at the same time.
* [`pa`](srcs/operations/pa_push_a.c) - push __a__: take the first element at the top of __b__ and put it at top of __a__. (do nothing if __b__ is empty).
* [`pb`](srcs/operations/pb_push_b.c) - push __b__: take the first element at the top of __a__ an dput it at top of __b__. (do nothing if __a__ is empty).
* [`ra`](srcs/operations/ra_rotate_a.c) - rotate __a__: shift up all elements of stack __a__ by 1. the first element becomes the last one.
* [`rb`](srcs/operations/rb_rotate_b.c) - rotate __b__: shift up all elements of stack __b__ by 1. the first element becomes the last one.
* [`rr`](srcs/operations/rr_ra_rb.c) - rr: rotate __a__ and rotate __b__ at the same time.
* [`rra`](srcs/operations/rra_reverse_rotate_a.c) - reverse rotate __a__: shift down all elements of stack __a__ by 1. the last element becomes the first one.
* [`rrb`](srcs/operations/rrb_reverse_rotate_b.c) - reverse rotate __b__: shift down all elements of stack __b__ by 1. the last element beoomes the first one.
* [`rrr`](srcs/operations/rrr_rra_rrb.c) - rrr: reverse rotate __a__ and reverse rotate __b__ at the same time.

## Installation

To build the programm there is only a few steps:
First of all, you can download the repository through the following steps in any shell of your preference:
```
git clone https://github.com/aoumad/Push_Swap push_swap
cd push_swap_42
make
```
This commands will compile everything and a executable "push_swap" should be created.

### Instructions

To run the application you shall input the program plus the arguments, which is the list of numbers to organize. For example:
```
$ ./push_swap 3 4 8 9 7 5 1 0 2 6
or
$ ./push_swap "10 30 60 42 80 99 -42"
```
This project was structured to run with integers, with numbers within the range of -2147483648 to 2147483647.
Also, even accepting a string of numbers, if you try to input a word or a letter, as 'a' or 'hello', it will not work, returning an error message.

## Other Information

- This project was made using C language, obeying all 42 norms;
- The tests folder has several tests and lists to better understand the project.
- There is also a visualizer (pyviz.py), it uses the operations that your program produces and present a graphic representation of this proccess. Keep in mind that you need to have installed python and the Tkinter lib;
- There is also an script in perl to automate the list generation and execution of the program, created by a fellow cadetes in 42-SP (ps_tester.pl) - Please, check the notion produced;
