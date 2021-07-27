# isPointInPoly
A fast algorithm which can determine whether a point is inside an arbitrary polygon, this method can support convex and non-convex polygon. 
It costs O(n), n refers to the n-sided shape.

**Input:**

point: tuple(x, y)
poly: [x1, y1, x2, y2, ..., xn, yn]

**Output:**

True: inside
False: outside

## Algorithm
When a point is inside the polygon, the sum of the angles between it and the vertices of the polygon is 2π. On the contrary, the sum of the angles is 0 while the point is outside the polygon. It should be noted that due to the order, the included angle here has positive and negative. Cross product is employed to deal with this problem.

For example:

**Convex:**
![Image text](https://github.com/kernel-Peanut/isPointInPoly/blob/main/convex.png)

**Non-Convex:**
![Image text](https://github.com/kernel-Peanut/isPointInPoly/blob/main/non-convex.png)
