# cs540-homework-6--game-theory-solved
**TO GET THIS SOLUTION VISIT:** [CS540 Homework 6- Game Theory Solved](https://www.ankitcodinghub.com/product/cs540-hw6-game-theory-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;117938&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS540 Homework 6- Game Theory Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Assignment Goals

Practice implementing a minimax algorithm Develop an internal state representation

Summary

In this assignment, you’ll be developing an AI game player for a modified version of the game called Teeko. We call this modified version Teeko2.

As you’re probably aware (https://xkcd.com/1002/) , there are certain kinds of games that computers are very good at, and others where even the best computers will routinely lose to the best human players. The class of games for which we can predict the best move from any given position (with enough computing power) is called Solved Games (https://en.wikipedia.org/wiki/Solved_game) . Teeko is an example of such a game, and this week you’ll be implementing a computer player for a modified version of it.

How to play Teeko

Teeko is very simple:

If after the drop phase neither player has won, they continue taking turns moving one marker at a time -to an adjacent space only! (Note this includes diagonals, not just left, right, up, and down one space.) -until one player wins.

How to play Teeko2

Visually, this makes a diamond shape on the board.

Program Specification

This week we’re providing a basic Python class and some driver code, and it’s up to you to finish it so that your player is actually intelligent.

Here is our partially-implemented game: teeko2_player.py

(If your computer doesn’t like downloading .py files, grab teeko2_player.py.txt and remove the .txt extension.)

If you run the game as it stands, you can play as a human player against a very stupid AI. This sample game currently works through the drop phase, and the AI player only plays randomly.

First, familiarize yourself with the comments in the code. There are several TODOs that you will complete to make a more “intelligent” player.

Make Move

Generate Successors

Define a successor function (e.g. succ(state) ) that takes in a board state and returns a list of the legal successors. During the drop phase, this simply means adding a new piece of the current player’s type to the board; during continued gameplay, this means moving any one of the current player’s pieces to an unoccupied location on the board, adjacent to that piece.

Note: wrapping around the edge is NOT allowed when determining “adjacent” positions.

Evaluate Successors

Using game_value(state) as a starting point, create a function to score each of the successor states. A terminal state where your AI player wins should have the maximal positive score (1), and a terminal state where the opponent wins should have the minimal negative score (-1).

1. Finish coding the diagonal and diamond checks for game_value(state) .

2. Define a heuristic_game_value(state) function to evaluate non-terminal states. (You should call game_value(state) from this function to determine whether state is a terminal state before you start

evaluating it heuristically.) This function should return some float value between 1 and -1.

Implement Minimax

Follow the pseudocode recursive functions on slide 43 of this presentation

(https://happyharrycn.github.io/CS540-Fall20/lectures/games_part1.pdf) , incorporating the depth cutoff to ensure you terminate in under 5 seconds.

1. Define a Max_Value(state, depth) function where your first call will be Max_Value(curr_state, 0) and every subsequent recursive call will increase the value of depth.

2. When the depth counter reaches your tested depth limit OR you find a terminal state, terminate the recursion.

We recommend timing your make_move() method (use Python’s time library

(https://docs.python.org/3/library/time.html#time.time) ) to see how deep in the minimax tree you can explore in under five seconds. Time your function with different values for your depth and pick one that will safely terminate in under 5 seconds.

Testing Your Code

We will be testing your implementation of make_move() under the following criteria:

1. Your AI must follow the rules of Teeko2 as described above, including the drop phase and continued gameplay.

2. Your AI must return its move as described in the comments, without modifying the current state.

3. Your AI must select each move it makes in five seconds or less.

4. Your AI must be able to beat a random player in 2 out of 3 matches.

We will be timing your make_move() remotely on the CS linux machines, to be fair in terms of processing power.

Submission Notes

Please submit your files in a zip file named hw6_&lt;netid&gt;.zip, where you replace &lt;netid&gt; with your netID

(your wisc.edu login). Inside your zip file, there should be only one file named: teeko2_player.py. Do not submit a Jupyter notebook .ipynb file.

Be sure to remove all debugging output before submission; your functions should run silently (except for the image rendering window). Failure to remove debugging output will be penalized (10pts).

Changelog

Updated the teeko2_player.py file to do valid move checking on the opposing player and to include print statements to see the game progress. Also, clarified that adjacent spots include diagonals.

Game AI

Criteria Ratings Pts

Repeated calls to make_move() result in legal moves 25.0 to &gt;0.0 pts

No

The current board state is not modified in make_move() 10.0 pts

The result of make_move() is correctly formatted in both the drop phase and continued gameplay 10.0 to &gt;0.0 pts

No

make_move() returns a move in under 5 seconds 10.0 to &gt;0.0 pts

No

make_move() wins against a random opponent in at least 2 out of 3 games 25.0 pts

Manual inspection: make_move() uses a recursive minimax algorithm 20.0 to &gt;0.0 pts

No
