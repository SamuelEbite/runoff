# runoff
 
This program is a voting system that uses the "Instant Runoff" method, also known as ranked-choice voting, to determine the winner of an election.

The program reads in the names of candidates from the command-line arguments and prompts the user to enter the number of voters. It then prompts each voter to rank the candidates in order of preference. Invalid votes are rejected.

The program eliminates candidates with the least number of votes in each round until a candidate receives a majority of votes. If a tie occurs, all remaining candidates are declared winners.

To use the program, compile it with the CS50 library and run the resulting executable, passing in the names of the candidates as command-line arguments. For example:

bash
Copy code
./runoff Alice Bob Charlie
The program will then prompt you to enter the number of voters and to rank the candidates in each round.

The program uses the following functions:

vote: records the voter's preference if it is valid
tabulate: tabulates the votes for each non-eliminated candidate
print_winner: prints the winner if there is one
find_min: returns the minimum number of votes any remaining candidate has
is_tie: returns true if the election is tied between all remaining candidates
eliminate: eliminates the candidate (or candidates) in last place
The program also defines a candidate struct to store information about each candidate.

The program has a few pre-defined constants:

MAX_VOTERS: the maximum number of voters allowed
MAX_CANDIDATES: the maximum number of candidates allowed
The program has error handling for the following cases:

Invalid usage: when the user fails to provide the correct number of command-line arguments
Maximum number of candidates exceeded: when the number of candidates provided exceeds the maximum allowed
Maximum number of voters exceeded: when the number of voters provided exceeds the maximum allowed
Invalid vote: when the user provides an invalid vote
This program is written in C and requires the CS50 library to compile and run.
