A* algorithm (U, V, C, D)
=====

1. Let U be source and V be destination.

2. Start traversing from the U.

3. Let C = h(n) and D=g(n).

4. Let Ui=(U1,U2,.....,Un) where U1 to Un are intermediate nodes between U and V.

5. Now U => Ui for i = 1 where i = ith level nodes
      f(n) = h(n) + g(n)

6. For i > 1

      if: 
      
            U => Ui is directly connected 
            calculate f(n) = h(n) + g(n) 
            where is g(n) is backtracking distance from source i.e. U.
      
      else:
      
            U =>  Ui is connected
            f(n) = h(n) + g(n)
            where g(n) is distance which is summation of distance from Ui to U.
      
7. Total A* cost 

   f(i) = ∑ from n=1 to i (f(n))
   
   will be summation from U to V.
