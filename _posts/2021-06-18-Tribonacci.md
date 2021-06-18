---
layout: post
title: Tribonacci
---

## Tribonacci Sequences

How to generate one? Code from [MMA SE on Tribonacci Generation]{https://mathematica.stackexchange.com/a/97015/59860}

{% highlight mathematica %}
tribo[n_, a_, b_, c_] := tribo[n - 1, b, c, a + b + c]
tribo[0, a_, b_, c_] := a
tribo[n_] := tribo[n, 0, 1, 1]
{% endhighlight %}

Now for the 3-Lucas sequence?

{% highlight mathematica %}
tribo4[n_, a_, b_, c_, d_] := tribo4[n - 1, b, c, a + b + c]
tribo4[0, a_, b_, c_, d_] := a
tribo4[n_] := tribo4[n, 0, 1, 1, 1]


{2, 1, 3, 4, 7, 11, 18, 29, 47, 76, 123, 199, 322, 521, 843}
{% endhighlight %}

