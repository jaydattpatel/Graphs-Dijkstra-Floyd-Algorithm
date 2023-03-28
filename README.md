# Graphs
Different operation of Directed Graph or Undirected Graph using C++

Vertices List:
( 1, Ahmedabad )
( 2, Bangalore )
( 3, Chennai )
( 4, Kolkatta )
( 5, Mumbai )
( 6, Delhi )


 Adjucents of (1, Ahmedabad ) : 
(2, Bangalore ) ( Distance: 50 )
(3, Chennai ) ( Distance: 45 )
(4, Kolkatta ) ( Distance: 10 )


 Adjucents of (2, Bangalore ) : 
(3, Chennai ) ( Distance: 10 )
(4, Kolkatta ) ( Distance: 15 )


 Adjucents of (3, Chennai ) : 
(5, Mumbai ) ( Distance: 30 )


 Adjucents of (4, Kolkatta ) : 
(1, Ahmedabad ) ( Distance: 10 )
(5, Mumbai ) ( Distance: 15 )


 Adjucents of (5, Mumbai ) : 
(2, Bangalore ) ( Distance: 20 )
(3, Chennai ) ( Distance: 35 )


________________________________________________________________________________________________________
| Adjacency Matrix |  Ahmedabad  |  Bangalore  |    Chennai  |   Kolkatta  |     Mumbai  |      Delhi  |
--------------------------------------------------------------------------------------------------------
|(    1, Ahmedabad)|      0      |      1      |      1      |      1      |      0      |      0      |
|(    2, Bangalore)|      0      |      0      |      1      |      1      |      0      |      0      |
|(    3,   Chennai)|      0      |      0      |      0      |      0      |      1      |      0      |
|(    4,  Kolkatta)|      1      |      0      |      0      |      0      |      1      |      0      |
|(    5,    Mumbai)|      0      |      1      |      1      |      0      |      0      |      0      |
|(    6,     Delhi)|      0      |      0      |      0      |      0      |      0      |      0      |
--------------------------------------------------------------------------------------------------------


________________________________________________________________________________________________________
|  Distance Matrix |  Ahmedabad  |  Bangalore  |    Chennai  |   Kolkatta  |     Mumbai  |      Delhi  |
--------------------------------------------------------------------------------------------------------
|(    1, Ahmedabad)|    999999   |        50   |        45   |        10   |    999999   |    999999   |
|(    2, Bangalore)|    999999   |    999999   |        10   |        15   |    999999   |    999999   |
|(    3,   Chennai)|    999999   |    999999   |    999999   |    999999   |        30   |    999999   |
|(    4,  Kolkatta)|        10   |    999999   |    999999   |    999999   |        15   |    999999   |
|(    5,    Mumbai)|    999999   |        20   |        35   |    999999   |    999999   |    999999   |
|(    6,     Delhi)|    999999   |    999999   |    999999   |    999999   |    999999   |    999999   |
--------------------------------------------------------------------------------------------------------


____________________________________________________________________________________________________
| Incidence Matrix | E-  0 | E-  1 | E-  2 | E-  3 | E-  4 | E-  5 | E-  6 | E-  7 | E-  8 | E-  9 |
----------------------------------------------------------------------------------------------------
|(    1, Ahmedabad)|    1  |    1  |    1  |    0  |    0  |    0  |   -1  |    0  |    0  |    0  |
|(    2, Bangalore)|   -1  |    0  |    0  |    1  |    1  |    0  |    0  |    0  |   -1  |    0  |
|(    3,   Chennai)|    0  |   -1  |    0  |   -1  |    0  |    1  |    0  |    0  |    0  |   -1  |
|(    4,  Kolkatta)|    0  |    0  |   -1  |    0  |   -1  |    0  |    1  |    1  |    0  |    0  |
|(    5,    Mumbai)|    0  |    0  |    0  |    0  |    0  |   -1  |    0  |   -1  |    1  |    1  |
|(    6,     Delhi)|    0  |    0  |    0  |    0  |    0  |    0  |    0  |    0  |    0  |    0  |
----------------------------------------------------------------------------------------------------


Finding Path from (1, Ahmedabad) to (3, Chennai) :
____________________________________________________________________________________________________________
|        Pivot Sequence      |  Ahmedabad |  Bangalore |    Chennai |   Kolkatta |     Mumbai |      Delhi |
------------------------------------------------------------------------------------------------------------
|(    1, Ahmedabad,Edges:  3)|        0   |   999999   |   999999   |   999999   |   999999   |   999999   |
|(    4,  Kolkatta,Edges:  2)|        0   |       50   |       45   |       10   |   999999   |   999999   |
|(    5,    Mumbai,Edges:  2)|        0   |       50   |       45   |       10   |       25   |   999999   |
|(    3,   Chennai,Edges:  1)|        0   |       45   |       45   |       10   |       25   |   999999   |
|(    2, Bangalore,Edges:  2)|        0   |       45   |       45   |       10   |       25   |   999999   |
|(    6,     Delhi,Edges:  0)|        0   |       45   |       45   |       10   |       25   |   999999   |
------------------------------------------------------------------------------------------------------------

Total Minumum Distance: 45

Path from (1, Ahmedabad) to (3, Chennai) :

 -> (1, Ahmedabad) -> (4, Kolkatta) -> (5, Mumbai) -> (3, Chennai)


Floyd Algorithm All Pair Shortest Path Matrix :
________________________________________________________________________________________________________
|  All Pair Matrix |  Ahmedabad  |  Bangalore  |    Chennai  |   Kolkatta  |     Mumbai  |      Delhi  |
--------------------------------------------------------------------------------------------------------
|(    1, Ahmedabad)|         0   |        45   |        45   |        10   |        25   |    999999   |
|(    2, Bangalore)|        25   |         0   |        10   |        15   |        30   |    999999   |
|(    3,   Chennai)|        75   |        50   |         0   |        65   |        30   |    999999   |
|(    4,  Kolkatta)|        10   |        35   |        45   |         0   |        15   |    999999   |
|(    5,    Mumbai)|        45   |        20   |        30   |        35   |         0   |    999999   |
|(    6,     Delhi)|    999999   |    999999   |    999999   |    999999   |    999999   |         0   |
--------------------------------------------------------------------------------------------------------


(3, Chennai) Vertex Deleted..........!


Vertices List:
( 1, Ahmedabad )
( 2, Bangalore )
( 4, Kolkatta )
( 5, Mumbai )
( 6, Delhi )


 Adjucents of (1, Ahmedabad ) :
(2, Bangalore ) ( Distance: 50 )
(4, Kolkatta ) ( Distance: 10 )


 Adjucents of (2, Bangalore ) : 
(4, Kolkatta ) ( Distance: 15 )


 No Main vertex found for adjucent........!


 Adjucents of (4, Kolkatta ) :
(1, Ahmedabad ) ( Distance: 10 )
(5, Mumbai ) ( Distance: 15 )


 Adjucents of (5, Mumbai ) :
(2, Bangalore ) ( Distance: 20 )
