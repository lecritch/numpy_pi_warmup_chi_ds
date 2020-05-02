# Part 1: Numpy practice

(If you get stuck at one part, try the other part)

Import the numpy library with the alias 'np'


```python

```

Create a variable called x that is a list of 100 0s


```python

```

Find another way to create a list of 100 0s; assign it to a new variable called y


```python

```

Turn x and y into numpy arrays


```python

```

In both x and y, insert the first 100 counting numbers in-between the 0s

With x, start inserting counting numbers at position 1

With y, start at position 0


```python

```

Remove all the 0s from both x and y

Use different methods of removal for x and y


```python

```

# Part 2: Estimating pi (with vis!)

Let's first import pyplot from matplotlib under the alias plt

(Also, run the commend %matplotlib inline so that jupyter renders the plots inside the notebook)


```python

```

Picture a circle perfectly circumscribed inside a unit square

The radius of the circle is $\frac{1}{2}$, and the area of the circle is $\pi \times (\frac{1}{2})^2 = \frac{\pi}{4}$

If we randomly throw enough points inside that square: 

 $$ \frac{\mbox{points that land in circle}}{\mbox{total points}} \approx \frac{\pi}{4} $$

so

$$ 4 \times \frac{\mbox{points that land in circle}}{\mbox{total points}} \approx \pi $$

We're going to create a plot that, inside of a unit square whose lower-left corner is at (0,0):
- plots 1000 random points
- colors them differently if they're inside or outside the circle
- calculates the error of the estimate of pi and prints it as the title of the graph

First we're going to create the points to throw inside the square.

Use numpy to create a variable x that has 1000 randomly drawn numbers between 0 and 1.

Use numpy to creat another variable y that has a different set of 1000 randomly-drawn numbers b/t 0 and 1.

(These are the x and y coordinates for the random points we'll throw at the square and inscribed circle)


```python

```

Select all the points in x that satisfy the condition
$$ (x^2 + y^2)<=\frac{1}{2} $$
and assign them to the variable inside_x

Do the same thing for the points in y, and assign them to the variable inside_y

(These are the x and y coordinates of the points inside the circle)

<i>Hint: the formula for a circle centered at (h,k) with radius r is</i> 
    $$(x-h)^2 + (y-k)^2 = r^2$$
<i>Where is the center of a circle inscribed in a unit square whose lower-left corner is at (0,0)?</i>


```python

```

Do the same thing for the points that lie within the square but outside the circle

Ie, select all the points in x and y that satisfy the condition
$$ (x^2 + y^2)>\frac{1}{2} $$
assign them to the variables outside_x and outside_y, respectively


```python

```

Now we'll calculate our $\pi$ estimate and the error from that estimate

Create the following variables:
- the number of pts inside the circle
    - name this variable pts_in_circle
    
    
- the number of pts outside the circle
    - name this variable pts_out_circle
    
    
- an estimate for $\pi$ that uses pts_in_circle and pts_out_circle
    - name this variable pi_est

    
- a calculation of the pct error of pi_est 
    - name this variable pi_est_error_pct


```python

```

Now, create a scatter plot of the "inside circle" points.  Color them blue, with alpha=.8 and edgecolor=None.

Create another scatter plot of the "outside circle" points.  Color them red, same alpha / edgecolor as above.

Plot both scatter plots in the same graph.

Call the title of the graph "Inscribed Circle in Unit Square to Estimate Pi".  Below the graph, print out a sentence saying what the pi estimate and pct error are using the variables pi_est and pi_est_error_pct.  

If you have time, try and figure out how to round to only include two digits in the pct error.


```python

```

If you have time, repeat the above steps for 100 points 


```python

```
