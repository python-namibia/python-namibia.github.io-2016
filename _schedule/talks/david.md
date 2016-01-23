---
layout: talk
date: 2016-01-26 15:00:00
title: "How do I know if this code works?"
speaker: David MacIver
location: Room 01
day: Tuesday
duration: 30 minutes
---

I have a problem. I write some code to solve that problem. How do I know if I succeeded?

If I only have to solve one form of the problem, I can just run it and look at the answer, but most
software has to deal with a huge variety of inputs and situations. How do you know you haven't missed
something?

Property-based testing provides one answer to this question. Using the Hypothesis property based testing
library (and the py.test testing framework), we'll see how we can create those situations before our
software ever escapes into the wild and test that it still behaves correctly, thus giving us far more
confidence in our code than we could otherwise have had.
