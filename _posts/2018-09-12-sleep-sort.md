---
layout: post
title: Sleep sort - an out of the box sorting algorithm 
tags: [tutorial, c++]
---

Have you heard of "sleep sort" algorithm? I recently came across it while searching for the most out of the box algorithms on the internet. So I decided to implement this in c plus plus and try it by myself. In this tutorial, we will implement this algorithm in c plus plus. While doing so, we'll learn:

1. How to multi-thread in c plus plus
2. How to generate random numbers in c plus plus
3. How to compile the code in Linux
4. Use of std::shared_ptr and std::make_shared()

The algorithm is quite simple and can be described in just one line: **For every element x in the unsorted list A, start a program that sleeps for x duration of time and prints x after that.** Did you get it ? Let's see the pseudo code for it.

pseudo_code

~~~code
function sleep_and_print(x):
	sleep(x)
    print x

function sleep_sort(A):
	for every x in list A:
    	create_a_new_thread(sleep_and_print(x))
    add all the threads with the main thread
~~~

Although the pseudo code seems simple. However, multi-threading part makes it a bit tricky. So, let's dive into the implementation of this algorithm in c plus plus.

**sleep_sort.cpp**

~~~cpp
#include <iostream>
#include <vector>
#include <thread>
#include <time.h>

static const int num_threads = 20;
void sleep_and_print(int x)
{
    // sleep for time x
    std::this_thread::sleep_for(std::chrono::milliseconds(x));
    std::cout<<x<<" ";
}

int main() {

    srand(time(NULL));
    std::vector<int> num_list;
    std::cout<<std::flush;
    std::cout<<"Unsorted list: "<<std::endl;
    
    for(size_t i = 0; i< 20; i++)
    {
        int num = int(rand()%100);
        std::cout<<num<<" ";
        num_list.push_back(num);
    }

    std::vector<std::shared_ptr<std::thread>> threads_vec(num_list.size());

    for (int i = 0; i < num_list.size(); ++i) {
        threads_vec[i] = std::make_shared<std::thread>(sleep_and_print, num_list[i]);
    }

    std::cout << "\nSorted list: \n";

    //Join the threads with the main thread. This will execute all the function calls 
    //parallely
    for (int i = 0; i < num_threads; ++i) {
        threads_vec[i]->join();
    }

    return 0;
}
~~~

Compiling the code in Linux:

~~~bash
$ g++ -std=c++11 -pthread sleep_sort.cpp -o sleep_sort
~~~

And here is the output:

~~~bash
$ ./sleep_sort
Unsorted list: 
19 24 19 63 97 36 67 9 5 67 7 84 33 87 20 88 67 40 78 94 
Sorted list: 
5 7 9 19 19 20 24 33 36 40 63 67 67 67 78 84 87 88 94 97
~~~