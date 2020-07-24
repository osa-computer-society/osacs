---
description: >-
  Data structures are some of the key tools in any programmer's toolbox,
  especially for algorithms. (WIP)
---

# Basic Data Structures

## What is a data structure?

Great question. Well, it's a way we store data. What makes them worth studying is that different data structures work better for different problems. \(TODO\)

## Why are they important?

{% hint style="info" %}
### Analogy Box

You're a high school student who needs to keep their notes in place, right? Well, imagine if every time you want to find, say, the date of the French Revolution, you
{% endhint %}

## Arrays

Arrays are one of the most fundamental data structures, and they simply model a collection of objects. \(TODO\)

## Stacks

{% hint style="info" %}
### Analogy Box

Let's say you're cleaning the dishes. After you wipe each dish, you put it on top of the stack of dishes, and after you're done cleaning all of them you've got a nice clean stack.

**When you need a plate, you take it off the top, and when you finish cleaning a plate, you stick it back on top.**

This way, you only ever interact with the top plate on the stack.
{% endhint %}

We call this kind of interaction **"last in, first out"** or **LIFO.** The last plate you finish cleaning and `push` on top of the stack is going to be the first one somebody `pops` off.

{% hint style="info" %}
In C++ terminology, the "top" of the stack is referred to as the "back," and the "bottom" of the stack is referred to as the "front."
{% endhint %}

We can model this stack of plates using a stack data structure! In practice, the abstract methods on a stack can include:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p><code>push(x)</code>
        </p>
        <p>C++: <code>push_back(x)</code>
        </p>
      </td>
      <td style="text-align:left">Insert <code>x</code> at the top of the stack.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>peek()<br />top()<br />back()</code>
      </td>
      <td style="text-align:left">Return the value of the element at the top of the stack.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>pop()<br />pop_back()</code>
      </td>
      <td style="text-align:left">Remove the top item of the stack. Note: in some implementations this also
        returns the value of the top item.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>full()</code>
      </td>
      <td style="text-align:left">Can the stack accept any more pushes?</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>empty()</code>
      </td>
      <td style="text-align:left">Can the stack accept any more pops?</td>
    </tr>
  </tbody>
</table>

### Using a stack

You'll almost never need to implement one of these yourself since almost any language has them. It's a good challenge, though!

{% code title="stack.cpp" %}
```cpp
// This demonstrates how to use the standard library stack
// in C++.

#include <iostream>
#include <stack>
using namespace std;

int main()
{
    stack<int> my_stack;

    for (int i = 1; i <= 10; i++)
        my_stack.push_back(i * i);

    while (!my_stack.empty())
    {
        cout << my_stack.top() << ' ';
        my_stack.pop();
    }
    cout << endl;

    return 0;
}
```
{% endcode %}

Till GitBook supports embeds, try an interactive example here: [https://repl.it/@piguyinthesky/C-Stack](https://repl.it/@piguyinthesky/C-Stack)

{% hint style="info" %}
## Challenge Time

Implement your own stack in C++! \(Doing it in Python is kind of trivial.\)

It should support the methods `push(x)`, `top()`, `pop()`, `empty()`, and`size()`.
{% endhint %}

### Cons

{% hint style="info" %}
So all's going dandy; everyone just takes a plate when they need it and put it back on top of the stack when they're done. However, your annoying sibling specifically wants the blue plate at the very bottom of the stack. Well, boo-hoo, they aren't getting it any time soon.
{% endhint %}

As we can tell, if the order of the elements matters, then a stack is probably **not** a good idea. We don't want any tantrums going on here.

