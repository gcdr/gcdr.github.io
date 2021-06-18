---
layout: post
title: Tribonacci
---

## Tribonacci Sequences

How to generate one?

{% highlight mathematica %}
tribo[n_, a_, b_, c_] := tribo[n - 1, b, c, a + b + c]
tribo[0, a_, b_, c_] := a
tribo[n_] := tribo[n, 0, 1, 1]
{% endhighlight %}

Now for the 3-Lucas sequence?

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


[MMA SE on Tribonacci Generation]{https://mathematica.stackexchange.com/a/97015/59860}
