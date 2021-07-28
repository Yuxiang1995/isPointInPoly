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
1)When a point is inside the polygon, the sum of the angles between it and the vertices of the polygon is 2π. As shown in Convex(a) and Non-Convex(a).

2)while the point is outside the polygon, the sum of the angles is 0. As shown in Convex(b) and Non-Convex(b).

3)It should be noted that due to the order, the included angle here has positive and negative. Cross product is employed to deal with this problem.

For example:

**Convex:**
![Image text](https://github.com/kernel-Peanut/isPointInPoly/blob/main/convex.png)

**Non-Convex:**
![Image text](https://github.com/kernel-Peanut/isPointInPoly/blob/main/non-convex.png)
