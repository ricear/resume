---
title: Detailed cas principle
date: 2022-08-11T07:29:38.229Z
summary: The full name of CAS is Compare and Swap, which means compare and
  exchange. It is a lock-free atomic algorithm as well as an optimistic
  mechanism. CAS is mapped to the operating system as a CPU atomic instruction.
  The implementation method is based on the assembly instructions of the
  hardware platform. In Intel's CPU, the `cmpxchg` instruction is used, which
  means that CAS is implemented by hardware, thereby improving efficiency at the
  hardware level.
draft: false
featured: false
authors:
  - ricear
tags:
  - CAS
  - MULTITHREADING
categories:
  - MULTITHREADING
image:
  filename: featured.png
  focal_point: Smart
  preview_only: false
links:
  - name: Read More
    url: 'https://notebook.ricear.com/project-34/doc-529'
---
The full name of CAS is Compare and Swap, which means compare and exchange. It is a lock-free atomic algorithm as well as an optimistic mechanism.

CAS is mapped to the operating system as a CPU atomic instruction. The implementation method is based on the assembly instructions of the hardware platform. In Intel's CPU, the `cmpxchg` instruction is used, which means that CAS is implemented by hardware, thereby improving efficiency at the hardware level.

When multiple threads use CAS to manipulate a variable at the same time, at most only one will win and update successfully, and the others will fail. The failed thread will not be suspended. It will only be notified of the failure and allowed to try again (spin). Of course, the implemented thread is also allowed to give up the operation. Based on this principle, even if the CAS operation does not have a lock, it can avoid interference from other threads to the current thread.

Compared with locks, the use of CAS will make the program look more complicated, but the use of lock-free methods is completely free from the overhead and blocking of frequent scheduling between threads caused by lock contention. He is naturally immune to deadlock problems, so he is better than The lock-based approach has better performance.

Click [here](https://notebook.ricear.com/project-34/doc-529) to see more information about the post.