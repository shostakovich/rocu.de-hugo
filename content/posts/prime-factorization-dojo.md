---
title: "Lessons from the prime factorization dojo"
date: 2012-09-29
emoji: 🧮
categories: Programming
---

Last week, my colleagues at Gutefrage.net, and I had our second

Coding Dojo.

I learned an important lesson — even though this wasn’t the first time I practiced the kata.

## *The kata*

The task was to create a class that decomposes natural numbers into its [prime factors](http://en.wikipedia.org/wiki/Prime_factor).

Additionally, the factors should be sorted ascending.

Examples:

```ruby
1  => [] # Since 1 is no prime ;)
5  => [5]
10 => [2,5]
75 => [3,5,5]
```

You get the idea ;)

This sounds simple and like a perfect candidate for an

Introduction to TDD, right?

Unfortunately, this kata is a bit tricky.

## *Performing the kata*

The first tests are straightforward:

```ruby
module PrimeFactorDecomposer
  def decompose(number)
if number < 4
    number
else
    [2,2]
end
  end
end

describe PrimeFactorDecomposer do
  include PrimeFactorDecomposer

  it "returns no prime factors for 1" do
    decompose(1).should be_empty
  end

  it "decomposes 2 into 2" do
    decompose(2).should be == [2]
  end

  it "decomposes 3 into 3" do
    decompose(3).should be == [3]
  end

  it "decomposes 4 into 2,2" do
    decompose(4).should be == [2,2]
  end
end
```

Now decomposing 5 would be a nice test? Right? Since 5 is a prime, it would only return 5. But how can we find out if it’s a prime?

So, we could write a function that finds out if 5 is prime. Hm, that seems hard.

What about 6? But then we have to develop an algorithm that works — otherwise, we would just move sidewards and add conditionals.

## *What’s the problem?*

You do not know how to solve the problem. Not everything is as simple as the [FizzBuzz](http://www.codingdojo.org/cgi-bin/index.pl?KataFizzBuzz) Kata.

Adding another test alone does not suffice. It’s a common hurdle for newcomers to TDD.

## *How to solve this?*

Grab a sheet of paper and think about the algorithm. Or do a little spike until you fully understand the problem. Every so often it’s just not true, that a design “magically” emerges.

## *Learnings*

You need sound knowledge about where to go — otherwise you will have problems with TDD along the way. Then you have to lean back and think a little or get feedback from something else than your tests.

TDD is cool, but it cannot solve every problem. Especially not complicated algorithms (this is a straightforward one, of course).

Another personal learning for me was to watch myself better, when I do a kata the first time.

When the design does not emerge from the tests — I should listen to them. Maybe they want to tell me that I have absolutely no idea what I am doing and that I need to think more…