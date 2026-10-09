
<!DOCTYPE html>
<html lang="en">

<body>

<pre>

- Quotes: "There is no wisdom from knowledge that we cannot instruct."

- The real "face" of the unit circle:
      The unit circle is fascinating but honestly a lie in term of calculus, from the infinity 
      of the irrationality of Pi to fascinating amount of useful equality that we can extract, 
      it sim that we can spend an infinite amount of time to describe by trying to think "outside the box" 
      all the correlations of angles and trigonometric constructions, but you are just sinking into
      infinite rationally... (and that's a good think conceptually for most).

- However, handled from Euler angle, we can leverage unit circle in a more practical way to describe time, 
      ( useful for animations/simulations/interactions when collisions occurs ) by tracking spacial variation of an 
      imaginary fields called 'i' or 'j', for this... imaginary (or parallels fields) have to be cyclic and so multiplying one unit
      by 'i' or 'j' produce, a rotated angle of 90° in direction of (+i) and 1 * i * i a rotation of 180° (-1) this match the algebra 
      equation  x² + 1 = 0 producing this negative equality  x² = -1 , now replace x by the imaginary 'i' or 'j' 
      and this match the imaginary behavior i² = -1 now we are talking ! it's just the imaginary state of a motion in time.

- So we got a rotational behavior of:
  
      1*i = 90° = (+i)
      1*i*i = i² = 180° = (-1)
      1*i*i*i = 270° = (3Pi/2) = (-i) 
      1*i*i*i*i = 360° = (+1)

- From this imaginary system, we can model point rotation in time with ease and mostly computing 
efficiency with complex imaginary algebra (later with quaternions).

- Example of complex notation:
     angle      |    complex notation 
      45°       |       1 + (1i)
      90°       |       0 + (1i)
     180°       |      -1 + (0i)
     270°       |       0 - (1i)

- Complex number and angle:
  
Of course cosine and sinus function embed this cyclic features by trigonometry table to help us 
to express angles with complex numbers by mapping ( Cosine on x ) and ( Sine on y point ) 
but with algebra computing capability ( if we care to remap the i² = -1 ) this later will be more
computing efficient, than matrix multiplication later in 3 dimensions for describing rotation
for now this only work in 2D only. ( we still can transform 2d points on oriented 3d Constriction Plane )
to fully control position but it's will not be as efficient as quaternions.

     angle      |           complex notation       |           real        imaginary
      45°       |       cos(PI/4) + sin(PI/4)i     |       (1/sqrt(2)) + (1/sqrt(2))i
      90°       |       cos(PI/2) + sin(Pi/2)i     |
     180°       |         cos(PI) + sin(PI)i       |
     270°       |      cos(3Pi/2) - sin(3PI/2)i    |

Example 1:
      
- So how to rotate a simple point:
    By multiplying one complex number by another one:
    - we need an angle: let say 90°, Pi/2 (in radians).
    - we need a point:  2 + 2i    ->   {x:2,y:2}
    - a equation cyclic remap i² = -1

- First build our complex momentum rotation of 90°:
         90° -> 0 + i  
         pt1 -> 2 + 2i
  
  ..., then multiply our point by the complex number momentum build from angle:
  
  - (simple) Algebra rotation computation:
                    
     (0+i) * (2+2i) = (0*2) + (0*2i) + (i*2) + (i*2i) = 0 + 0 + 2i + 2i² = 2i + 2*(-1) = -2 + 2i 
  
  transformed point = { (real) x: -2 , (imaginary) y: 2 }
      
  - you can use python to easily confirm your algebra multiplication: 

```python  
     >>> complex(0+j) * complex(2+2j)
     >>> (-2+2j)
```  
      
 Example 2:
      
      (0-4i) * (2+2i) =   (0*2) + (0*2i) + (-4i*2) + (-4i*2i)  = 0 + 0 -8i -8i² = -8i -8*(-1) = 8 - 8i

- note: 
      this is just a rotation of points in 2d, 
      translation, is a simple complex point addition or subtraction 
      but one dimensional complex numbers are constraints to x and y only.
      
</pre>
</body>
</html>


