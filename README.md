## Can Reach monad

### Description
This challenge is to write a function canReach that will check whether it possible to reach destination on chess board in provided steps of knight.

### Hint (What's a monad?)
In functional programming, a monad is a structure that represents computations defined as sequences of steps. A type with a monad structure defines what it means to chain operations, or nest functions of that type together. This allows the programmer to build pipelines that process data in steps, in which each action is decorated with additional processing rules provided by the monad.

### For example:

Lets imagine that you have a chess board and only one knight piece on it. We want to find out if the knight can reach a certain position in certain moves. We'll just use a pair of numbers to represent the knight's position on the chess board. The first number will determine the column he's in and the second number will determine the row: [c, r].

In the picture the knight is in [6, 2]:
```js
   1 2 3 4 5 6 7 8
8 | | | | | | | | |
7 | | | | | | | | |
6 | | | | | | | | |
5 | | | | | | | | |
4 | | | | |x| |x| |
3 | | | |x| | | |x|
2 | | | | | |*| | |
1 | | | |x| | | |x|
```

In one movement he can reach the next squares:
[ [ 8, 1 ], [ 8, 3 ], [ 4, 1 ], [ 4, 3 ], [ 7, 4 ], [ 5, 4 ] ]

```js
* startPos: actual position of the knight
* finalPos: final position of the knight
* movements: num of movements
* canReach returns: true if the knight could reach the "to square" starting in "from square" in "movements" steps | false otherwise

canReach([6, 2], [8, 1], 1) === true
canReach([6, 2], [8, 2], 1) === false
canReach([6, 2], [8, 1], 2) === false
canReach([6, 2], [8, 2], 2) === true
canReach([6, 2], [6, 2], 0) === true
canReach([6, 2], [8, 1], 0) === false
```

#### Write your code in `src/index.js`
#### Run test locally `npm test`
