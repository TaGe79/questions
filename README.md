# The Blocks Problem
 The problem is to parse a series of commands that instruct a robot arm in how to manipulate blocks
 that lie on a flat table. Initially there are N blocks on the table (numbered from 0 to N-1) with
 block B(i) adjacent to block B(i+1), for all 0 <= i < N-1 as shown below:
 
 ```
  ----- ----- ----- -----         -----
 |  0  |  1  |  2  |  3  | . . . | n-1 |
  ----- ----- ----- -----         -----
 ```
  
 Valid commands to manipulate the blocks are:
  - `move a onto b`
    where *a* and *b* are block numbers, puts block a onto block b after returning any block that are 
    stacked on top of blocks a and b to their initial positions
  - `move a over b`
    where *a* and *b* are block numbers, puts block a onto the top of the stack containing block b,
    after returning any blocks that are stacked on top of block a to their initial positions
  - `pile a onto b`
    where *a* and *b* are block numbers, moves the pile of blocks consisting of block *a* and any blocks 
    that are stacked above block *a* , onto block *b*. All blocks on top of block *b* are moved to their 
    initial positions prior the pile taking place. The blocks stacked above block *a* retain their order 
    when moved.
  - `pile a over b`
    where *a* and *b* are block numbers, puts the pile of blocks consisting of block *a* and any blocks 
    that are stacked above block *a* , onto the top of the stack containing block *b*. The blocks stacked 
    above block *a* retain their order when moved.
  - `quit`
    terminate manipulations on the block world.
    
Any command in which `a = b` or in which a and b are in the same stack of blocks is an illegal command. 
All illegal commands should be ignored and should have no affect on the configuration of blocks.
