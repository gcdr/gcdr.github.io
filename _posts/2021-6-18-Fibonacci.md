---
layout: post
title: Fibonacci Sequences
---

## Fibonacci Sequences

How to generate one?

{% highlight mathematica %}
seq1 = Table[Fibonacci[x], {x, 0, 14}]

{0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377}
{% endhighlight %}

Now for the Lucas sequence?

{% highlight mathematica %}
seq2 = Table[LucasL[x], {x, 0, 14}]

{2, 1, 3, 4, 7, 11, 18, 29, 47, 76, 123, 199, 322, 521, 843}
{% endhighlight %}

Then try adding or multiplying them against each other. Notice a strange pattern below? That is the magic of these sequences.

{% highlight mathematica %}
seq3 = seq1 + seq2

{2, 2, 4, 6, 10, 16, 26, 42, 68, 110, 178, 288, 466, 754, 1220}

seq4 = seq1 seq2

{0, 1, 3, 8, 21, 55, 144, 377, 987, 2584, 6765, 17711, 46368, 121393, 317811}
{% endhighlight %}
