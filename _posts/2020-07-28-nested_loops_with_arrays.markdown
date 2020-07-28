---
layout: post
title:      "Nested Loops with Arrays"
date:       2020-07-28 23:00:00 +0000
permalink:  nested_loops_with_arrays
---


Sometimes nested loops are necessary and helpful when searching through an array for items that work together.

For instance, say I want to watch two movies that both equal exactly 4 hours, or 240 minutes, of watching. If I have an array that lists out each movie's runtime, how would I be able to quickly find two that match and add up to 240? Nested loops will work here!

We'll use this array. The second and third times will work together to equal our desired 240.

`movies = [120, 100, 140, 110, 280]`

Now we need to loop through the array and grab each item. So we will use the following code.


```
movies.each_with_index do |m1, i1|

end
```

Having the index will be helpful to compare with each item and ensure we do not use the same one twice.

Next we will add our nested loop:

```
movies.each_with_index do |m1, i1|
    movies.each_with_index do |m2, i2| 
        if m1 + m2 == 240 && i1 != i2
            puts "#{m1} + #{m2} are a match!"
        end
    end
end
```

Running this we will find that index 1 and index 2 are the selected movies with the runtimes that add up to the total of 240. None of the others will return because they do not satisfy our total of 240!

The puts statement will print to our terminal the correct totals that work!
