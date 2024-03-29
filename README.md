
# Introduction to Sets

## Introduction

You have definitely heard of sets before. In this section, however, you will learn the formal definition of sets, which will serve as a foundation for everything related to probability and combinatorics! You'll also learn about set operations and how to visualize set operations using Venn Diagrams. Finally, we'll introduce sets in Python. 

## Objectives

You will be able to: 

* Define a set in the context of probability theory
* Define a universal set and subsets
* Describe the process of making unions, intersections, and complements
* Use Venn Diagrams to visually demonstrate set operations
* Describe the inclusion/exclusion principle


## What is a Set? 

In probability theory, a set is defined as a *well-defined collection of objects*. 

Mathematically, you can denote a set by $S$. An element $x$ may or may not belong to a set $S$. 

For example, if $S$ is defined as the set of even numbers, then:

* If $x = 2$, $x$ belongs to $S$ because $x$ is an even number.

* If $x = 9$, $x$ does not belong to $S$ because $x$ is not an even number.


## Subsets

Set $T$ is a subset of set $S$ if *every element* in set $T$ is also in set $S$.

For example, if A = {1,2,3} and B = {1,2,3}, A is subset of B. If C = {1,2} then C is a subset of A and a subset of B.

You can learn more about subsets and the related concept of proper subsets in the Appendix. 


## Universal Sets

The collection of all possible outcomes in a certain context or universe is called the **universal set**.
A universal set is often denoted by $\Omega$.

An example of a universal set is the set of all possible outcomes when rolling a dice: $\Omega = \{1,2,3,4,5,6\}$

A universal set is not necessarily all the possible things that have ever existed. Typically, a universal set is just all the possible elements within certain bounds, e.g., the set of all countries in the world, the set of all the animal species in the Bronx Zoo, etc.

A universal set can have an infinite number of elements, for example, the set of all real numbers!

## Elementary Set Operations

Next, let's talk about set operations. Imagine you have two sets of numbers, say the first 4 multiples of 3 in set $S$:

$ S = \{3,6,9,12\}$

and the first 4 multiples of 2 in set $T$:

$ T = \{2,4,6,8\} $.

### a) Union of Two Sets

The union of two sets $S$ and $T$ is the set of elements of either S or T, or in both.  

Applied to our example, the union of $S$ and $T$ is given by the elements $\{2,3,4,6,8,9,12\}$. 

In mathematical terms, the union of $S$ and $T$ is denoted as $S \cup T$.

A popular way to represent sets and their relationships is through Venn Diagrams, (https://en.wikipedia.org/wiki/Venn_diagram), see picture below!

<img src="images/new_union.png" width="250"/>

### b) Intersection of Two Sets 

The intersection of two sets $S$ and $T$ is the set that contains all elements of $S$ that also belong to $T$. 

Applied to our example, the intersection of $S$ and $T$ is given by {6}, so it contains the elements that are multiples of both 2 AND 3.

In mathematical terms, the intersection of $S$ and $T$ is denoted as $S \cap T$.

<img src="images/new_intersection.png" width="250"/>

### c) Relative Complement or the Difference

If you have S and T, the relative complement of S contains all the elements of T that are NOT in S. This is also sometimes referred to as the *difference*. The difference is denoted by $ T\backslash S $ or $T-S$.

In this case, the relative complement of S (or $ T\backslash S $) is $\{2,4,8\}$. The relative complement of T (or $ S\backslash T $) is $\{3,9,12\}$.

<img src="images/new_rel_comp.png" width="250"/>

### d) Absolute Complement

There is another definition of the complement when considering universal sets $\Omega$ as well. In this context, we're talking about the *absolute complement*.

The absolute complement of $S$, with respect to the Universal set $\Omega$, is the collection of the objects in $\Omega$ that don't belong to $S$.

Note how the definition of $\Omega$ is very important here. Imagine a set $S= \{\text{elephant, alligator, tiger, bear}\}$. The complement of this set will depend on how the universal set is defined: Is $\Omega$ equal to *the animals in the Bronx Zoo*, or *the 20 most deadly animals in the world*?

Mathematically, the absolute complement of $S$ is denoted as $S'$ or $S^c$.

Let's reconsider $S$ and $T$ as defined previously.

Let's define $\Omega$, the universal set (denoted by the box around the two Venn diagrams), as the set that contains the multiples of both 2 and 3 until 20. Then the elements of $\Omega$ are $\{2,3,4,6,8,9,10,12,14,15,16,18,20\}$. 

The absolute complement of $S$ (so, $S'$ or $S^c$) is then given by $\{2,4,8,10,14,15,16,18,20\}$.

<img src="images/new_abs_comp.png" width="250"/>

## A quick note on the Inclusion-Exclusion Principle

Note that if you want to know how many elements are in set $S$ versus $T$, you can't simply sum up the elements, because they have elements in common.

In combinational mathematics, the inclusion-exclusion principle is a counting technique that solves this problem. 

When having two sets, the method for counting the number of elements in the union of two finite sets is given by:

$\mid S \cup T \mid = \mid S \mid + \mid T \mid - \mid S \cap T \mid $,

where the horizontal lines denote the cardinality of a set, which is the number of elements in the set, considering a set with a finite number of elements.

The formula expresses the fact that the sum of the sizes of the two sets may be too large since some elements may be counted twice. For the double-counted elements, one is subtracted again.

To learn about the Inclusion-Exclusion Principle, refer to the Appendix for this Module.


## Empty Sets

When there are no elements in a certain set, this set is **empty**, denoted by $\emptyset$ or simply $\{\}$


## Sets and Set Operations: A Summative Example

To put this all together, let's consider an example with restaurants:

Think about a *set A* with all the restaurants that serve Italian food.
Next, there is a *set B* with all the restaurants that serve burgers.

The **union** of these sets, *set C*, contains the set of restaurants that either serve Italian food, burgers or both.

You could say that the **universal set** here, *set U*, contains all the restaurants in the world (with any type of food). Then *set C* is a **subset** of *set U*. 

The **intersection** of *A* and *B* contains the restaurants that serve _both_ Italian food and burgers.

The **relative complement** of *set A* (relative to *set B*) contains the restaurants that serve burgers but _not_ Italian food.

The **absolute complement** of *set A* contains the restaurants that serve *any food* but _no_ Italian food.


## Introduction to Sets in Python

Here are some things to bear in mind when working with sets in Python:

* Sets are unordered collections of unique elements.
* Sets are iterable.
* Sets are collections of lower level python objects (just like lists or dictionaries).

Let's use our example sets $S$ and $T$ to show how sets can be defined in Python. 

Remember, $S$ is the set that includes the first four multiples of 3: 

$ S = \{3,6,9,12\}$ 

and $T$ is the set that includes the first four multiples of 2: 

$ T = \{2,4,6,8\} $.

To define sets in Python, we have the following two equivalent options: 


```python
# Define S = {3,6,9,12} and T = {2, 4, 6, 8}

S = {3, 6, 9, 12}

T = set([2, 4, 6, 8])

print("Set S:", S)
print("\nSet T:", T)
```

    Set S: {9, 3, 12, 6}
    
    Set T: {8, 2, 4, 6}


You can check that both definitions of a set are equivalent: 


```python
{3, 6, 9, 12} == set({3, 6, 9, 12})
```




    True



Notice that when printing the sets, the order of the elements was changed. Let's do a quick check to see if these are equivalent: 


```python
print({3, 6, 9, 12} == {9, 3, 12, 6})
print({2, 4, 6, 8} == {8, 2, 4, 6})
```

    True
    True


Yes, they are! This is because, as mentioned before, sets are unordered collections of unique elements: as long as the elements in two defined sets are the same, the order in which we input them into Python does not matter in terms of determining if they are equivalent. 

To read more about sets in Python, you can find and read the documentation here: [Sets](https://docs.python.org/3.6/library/stdtypes.html#set-types-set-frozenset). 


## Summary

In this section, you learned about sets, subsets, and universal sets. Next, you were introduced to some elementary set operations such as unions, intersections, and complements. After that, all this information was tied together through the inclusion-exclusion principle. Next, you saw how sets translate into Python. You'll start exploring set operations in Python in further detail in the next lab!

If you're interested in diving a little bit deeper into sets to learn about notation, the difference between subsets and proper subsets, and the inclusion/exclusion principle, refer to the Appendix to this Module.
