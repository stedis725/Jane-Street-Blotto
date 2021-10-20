# Jane-Street-Blotto
My solution to a variation of the classic Blotto game proposed by Jane Street.

## Puzzle Conditions

There are 10 castles, numbered 1, 2, 3, ... , 10, and worth 1, 2, 3, ... , 10 points respectively. You have 100 soldiers, which you can
allocate between the castles however you wish. Your opponent also (independently) does the same. The number of soldiers on
each castle is then compared, and for each castle, whoever has the most soldiers on that castle wins its points (in the case of a tie,
no one gets points). In a given match, castles are fought in order (starting with castle 1). If at any point a player wins 3 consecutive
castles, that player is automatically awarded all remaining castles.

For example, here is one potential match:
|          | C1 | C2 | C3 | C4 | C5 | C6 | C7 | C8 | C9 | C10 |
|----------|----|----|----|----|----|----|----|----|----|-----|
| Alice    | 10 | 10 | 10 | 10 | 20 | 0  | 0  | 0  | 20 | 20  |
| Carol    | 20 | 0  | 10 | 5  | 10 | 5  | 10 | 20 | 0  | 0   |

In the example match above, Alice wins castles 2, 4, and 5, for a total of 11 points. Carol wins castles 1, 6, 7, and 8 — and then
castles 9 and 10 — for a total of 41 points. (No one wins castles 3, since that was a tie. Alice does not win castles 9 or 10 because
those were awarded to Carol after she won castles 6 through 8.).

## Task

We're going to play a tournament. You get one entry and your final score is the average of your scores playing head-to-head
against entries from over 300 Jane Streeters. An entry should be submitted as a list of 10 non-negative integers, adding up to 100,
where the Nth element is the number of soldiers being sent to castle N.

What's your entry? How did you go about coming up with it?

## Submission

My final solution was [1, 1, 42, 27, 11, 5, 6, 3, 4, 0], which I arrived at using a variation of stochastic hill climbing in which the objective function was updated throughout the optimization process as improved solutions were discovered, allowing the final solution to better perform against more sophisticated strategies that would be utilized by other competitors.  

For more details, check out my solution write-up [here](https://github.com/stedis725/Jane-Street-Blotto/blob/main/Blotto%20Write-Up.pdf) my python code [here](https://github.com/stedis725/Jane-Street-Blotto/blob/main/Blotto.ipynb).

I successfully gained admission to Jane Street's SEE Program as a result of my perfromance in this tournament.
