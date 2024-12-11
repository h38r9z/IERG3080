java c
IERG3080 Fall 2024 - Group Project 
Due:   23   Dec   2024
Instructions: 
● This   project takes 30% of the course total.
●         Your group   needs to   use Visual Studio to   implement a game   using WPF in C# 
described   in this specification, and also write a 5-page report with   details on   your system structure (class design, class reuse,   software   patterns   used), the   testing   plan,   and the difficulties you have overcome during   your   project. 
●         You   must demonstrate the ability to self-learn the details about   programming,   and provide a list of references of online resources   in your   report,   either   integral   or         supplementary to the completion of the project.
●          Every group   has to submit a zip file to the   Blackboard   consisting of the whole visual studio project, a standalone playable (your exe and other   needed   resources files),   a report in pdf format, and a 1-min demonstration video capturing the losing   (and      winning, if any) moments   of the   game.
● Your project   is expected to   be   run correctly on the Windows   machines   in   ERB1004.
● You are   required to   use Agile   methodology   in your project.
Grading scheme (max 30%). Only consider submissions that work properly. 
○          Fulfilling the   requirements   in the   implementation, and the releasable status   of   the   project (user-friendliness, robustness, etc.)      (5%)
○ Goodness of the design,   including class reusability and design   patterns   (10%)
■          Describe these in the   report.
● Advanced features (optional)
○          Feature 1
■          Fulfilling the requirements (2%)
■ Goodness of design   (4%)
○          Feature 2
■          Fulfilling the requirements (4%)
■ Goodness of design   (8%)
● Written   report (mandatory)   (5%)
○          Using proper modeling languages for describing the design
■          Do NOT put your source code directly   in the   report!
○ An appropriate list of   references   in the   report
The final score   is the   minimum of 30 and the sum of the   obtained   scores.   No   score   is   given   to the advanced features if the mandatory   parts are   not   finished.
Background 
Tetris   is an old   but   popular puzzle video game with   many variants.   In the   game,   there   is   a rectangular field. Game pieces, known as tetrominoes,   drop from   the   top   of the field,   one   at   a time. The   player can   move the falling   piece   horizontally or rotate   it   before   it   lands. The player can also accelerate the falling speed of the piece.   When   a   row   is   completely   filled,   the   row will be   eliminated.
In this   project, you   need to   implement a simplified Tetris game.   Extra features other   than   those described below are welcome,   but   not   necessary.
Baseline Requirements 
The baseline of the project   is to implement   a   single-player version   of the   game which   is   similar to the one in the   following website:
https://tetris.com/play-tetris 
There are 7 types of tetrominoes in the game   as   shown   in   the   figure   below.

Source: https://en.wikipedia.org/wiki/Tetris
The falling piece can be:
● Rotated 90 degree clockwise (or anticlockwise) by the player if the piece after rotation does not overlap with other landed pieces;
● Moved horizontally by the player if the new location does not overlap with other landed pieces.The falling spe代 写IERG3080 Fall 2024 - Group ProjectStatistics
代做程序编程语言ed depends   on the number of eliminated   rows. The   player   can   accelerate   the      falling speed of the   piece (soft drop), or land   the   piece   directly   (hard   drop).   The   game   is   over   when the landed tetrominoes have some   blocks outside the   game   field.
The score earned for eliminating   n   rows follow the formula   100      ×    2n. Once a   row   is   eliminated, the upper rows shift down to   replace   the   eliminated   row.
The following is a list of features that are NOT required to be implemented: 
● Play by mouse control 
● Hold a piece (swap to the on-hold state for future use) 
● T-spin 
● Levels (that multiples the score and increases the falling speed) 
The UI should show at least the following components:
● The game field (20 rows, 10 columns) 
● The score 
● The next tetrominoes (at least 1)
For user-friendliness, a simple   main   menu before gameplay,   a   game-over   message, the pausing feature, and the ability to start a   new game without   re-launching   the   program   are   necessary. 
Advanced Features 
The following two advanced features are optional. You can   implement   both features   if you               want to. Advanced gameplay involves two players. When   a   player clears   more   than   one   row   at a time, some garbage rows will   be sent   to   the   game field   of the   other   player.   More specifically, when n    >    1   rows are eliminated,   2n−1      garbage   rows will   be sent.   The   garbage   rows always appear from the bottom and   raise the other   existing   rows. Every garbage   row consists of garbage   blocks and a single   hole. When   the   hole   is   filled   by      landed tetrominoes,   i.e., the row is completely filled, the   row will   be   eliminated. An   example   of garbage   rows   is shown   in the figure below.

Source: https://harddrop.com/wiki/Tetris_Battle#Normal_Garbage 
Feature 1 
Implement the   battle   mode of a   local 2-player Tetris game (2   players   play on   the   same computer). That   is, your product supports both single-player   mode   and   battle   mode.   Except   the extra   rule for garbage   rows, the   remaining   rules are the same as that   in   the   baseline requirements. When a   player loses the game, the other   player wins and   the   game   session   is   ended.   If both   players   lose at the same time, then   it   is   a   draw. 

The following is a list of features that are NOT required to be implemented: 
● Computer player (AI) 
● Control settings (you can pre-define the controls) 
The UI should show at least two sets of 
● The game field (20 rows, 10 columns) 
● The score 
● The next tetrominoes (at least 1) 
One set for each player. That is, the two players are playing in their own individual game field.
Feature 2 
Implement the   battle   mode of an online   2-player Tetris game (2   players   play   on   different computers). That   is, your product supports both single-player   mode   and   battle   mode. The   requirements are the same as those   in   Feature   1, except that the   players   are   playing   on separate computers.
To   initiate the   network connection, one of the   players   is the   host while the other one   is   the client. The client   inputs the   host’s   IP address to attempt the   connection   (assume   IPv4). You   can   pre-define a port for the communication   purpose.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
