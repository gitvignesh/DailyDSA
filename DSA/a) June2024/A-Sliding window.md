
**Variation-1: Fixed size**
The idea behind having a fixed sliding window is to **maintain** two pointers that are k apart from each other and fit a certain constraint.
One key thing that tell if a problem can be solved using the fixed sliding window technique is if the problem specifies a subarray length, **k**

**Variation-2: Variable size**
Sliding Window (variable) tells us that we can keep expanding our window as long as we don't break the constraint we are given. We already saw this with Kadane's algorithm when we tried to expand the window as much as possible to get to our maximum sum.
