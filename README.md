# Backgammon Adversarial Search

### About
+ This is an Artificially Intelligent Backgammon playing Bot which plays against the compuer bot. I have employed an Attacking Strategy for my Bot.

### Basic Strategy
+ My basic stratergy is initially at start of the game making primes near home board which makes our position near home board as strong as possible.
+ Opponent thus gets blocked and gets less points free to come back in game , once he gets hit.
+ After making home board strong I use running game stratergy to get back our checkers 
to home board from opponent's home board.
+ I have maintain pip count to calculate where I exactly are in the game.
+ pipcount ->> gives avg. number of moves you have to move to complete the game.
+ During bear-off I are keeping in minds that if opponent has it's bots in our home during our bear-off I choose move carefully and avoid leaving vulnerable checker.

### Playing format


#### Input
>C1 C2 C3 ...... C24
>B
>R1 R2

Where C[24] is denotes the state of the board, with positive entries denoting white markers,
and negative denoting black markers. YOU ALWAYS HAVE TO PLAY ON BEHALF OF
ALICE/WHITE, IE MOVING FROM LEFT TO RIGHT.
B is a string, consisting of ‘a’ and ‘b’, denoting the markers on the bar.
And R1 and R2 denote dice rolls, as performed by the mediator, with (R1, R2) being u.a.r. from
Z6xZ6.

#### Output
>S1 D1
>S2 D2

Where, S1, D1, S2, and D2 denote columns, and S1 -> D1 and S2 -> D2 are the player’s two moves,
in that order.

+ If any move is invalid please output the “pass” keyword for that move. EXAMPLE : If you
want to move one checker from C1->C5 and the other to be passed your output will be:

>1 3
>pass

+ If you want to move your checker from the bar to any position(say C2) and the other
checker from C1->C3 your output will be:

>Z 2
>1 3

+ For bearing off, from say C11, you output the move:

>11 O
>pass