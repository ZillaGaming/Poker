# PokerTracker 4
PokerTracker imports and parses the hand histories that poker sites create during online play and stores the resulting statistics and information in a local PostgreSQL database. The information is used for in-game opponent analysis using a custom Head-Up Display (HUD), an automatic real-time overlay of each players statistics for each poker table, and for statistical analysis and review using custom reports, statistics, and filters. 

* Custom Statistic Coding = Custom coded statistics using SQL expressions used to track key performance metrics used for analysis in HUDs and reports.
* Custom HUD = Displays general game state data and custom statistics on each table for each opponent. Used for identifying strategically and mathematically inefficient frequencies employed by opponents.
* Custom Pop-Up HUD = A visually smaller version of Custom HUD. Displays only essential metrics with additional information available from clickable pop-ups.
* HUD Builder = Used to create the HUDs. Builder shows each statistical group (panel on the table dsiplay), the custom statistics involved with each group, and an approximated representation of the table visualization.
* Custom Reporting = Uses custom statistics and filters to isolate specific segments of data for statistical and strategic analysis, such as identifying population benchmarks or hand playability cut-offs.

# PIOSolver
PioSOLVER is a game theory optimal (GTO) solver for Texas Hold'em. It handles postflop spots with arbitrary starting ranges, stack sizes, bet-sizes as well as desired accuracy and displays the solution tree.

* PostFlop Range Tree Builder = Used to build the postflop game trees and explore permutations of possible outcomes based on different bet actions, bet sizes, and stack sizes.

* PostFlop Solver Analysis = Visualization of expected value (EV) for GTO strategies, particularly useful for identifying areas where mixed strategies are implemented (multiple strategies deployed at non-zero frequencies).

# SimplePostflop
Simple Postflop is software for calculating Nash-Equilibrium strategies in pre-flop and post flop Texas Hold'em situations. SimplePostflop builds GTO strategies in pre-flop and post flop situations according to bet-sizing and ranges of two players.

* Solver Analysis = Visualization of expected value (EV) for GTO strategies, particularly useful for identifying areas where mixed strategies are implemented (multiple strategies deployed at non-zero frequencies).

# CardRunnersEV
CardRunnersEV is poker analysis software that will allow you to build decision trees and calculate the EV of every decision within that tree.

* Game Tree Analysis = Used to build the postflop game trees and explore permutations of possible outcomes based on different bet actions, bet sizes, and stack sizes.

# Microsoft Excel

* Bluffing and Bluff Catching Model = Used to calclualte combinatorics required for GTO bluffing and bluff catching frequencies and also the EV based on bet size and equity.
