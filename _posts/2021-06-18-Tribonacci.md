---
layout: post
title: Tribonacci
---

## Tribonacci & Quadranacci Sequences

How to generate one? Code from [MMA SE on Tribonacci Generation](https://mathematica.stackexchange.com/a/97015/59860)

{% highlight mathematica %}
tribo[n_, a_, b_, c_] := tribo[n - 1, b, c, a + b + c]
tribo[0, a_, b_, c_] := a
tribo[n_] := tribo[n, 0, 1, 1]

seq1 = Table[tribo[x], {x, 0, 14}]
{0, 1, 1, 2, 4, 7, 13, 24, 44, 81, 149, 274, 504, 927, 1705}
{% endhighlight %}

Now for the 4-Quadranacci sequence?

{% highlight mathematica %}
quadra4[n_, a_, b_, c_, d_] := quadra4[n - 1, b, c, d, a + b + c + d]
quadra4[0, a_, b_, c_, d_] := a
quadra4[n_] := quadra4[n, 0, 1, 1, 1]

Table[quadra4[x], {x, 0, 14}]
{0, 1, 1, 1, 3, 6, 11, 21, 41, 79, 152, 293, 565, 1089, 2099}
{% endhighlight %}

