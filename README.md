# PokerTracker 4
PokerTracker imports and parses the hand histories that poker sites create during online play and stores the resulting statistics and information in a local postgreSQL database. The information is used for in-game opponent analysis using a custom Head-Up Display (HUD), an automatic real-time overlay of each players statistics for each poker table, and for statistical analysis and review using custom reports, statistics, and filters. 

* Custom Statistic Coding = Custom programmed statistics to track key strategic metrics used in HUDs and reports.
* Custom HUD = Displays general game state data and custom statistics on each table for each opponent. Used for identifying strategically and mathematically inefficient frequencies employed by opponents.
* Custom Pop-Up HUD = A visually smaller version of Custom HUD. Displays only essential metrics with additional information available from clickable pop-ups.
* HUD Builder = Used to create the HUDs. Builder shows each statistical group (each represents a diffent panel on the table dsiplay), the custom statistics involved with each group, and an approximated representation of the table visualization.
* Custom Reporting = Uses custom statistics and filters to isolate specific segments of data for statistical and strategic analysis, such as identifying population benchmarks or playability cut-offs.

# PIOSolver
PioSOLVER is a game theory optimal (GTO) solver for Texas Hold'em. It handles postflop spots with arbitrary starting ranges, stack sizes, bet-sizes as well as desired accuracy and displays the solution tree.

# CardRunnersEV
CardRunnersEV is poker analysis software that will allow you to build decision trees and calculate the expected value (EV) of every decision within that tree.

# SimplePostflop
Simple Postflop is software for calculating Nash-Equilibrium strategies in pre-flop and post flop Texas Hold'em situations. SimplePostflop builds GTO strategies in pre-flop and post flop situations according to bet-sizing and ranges of two players.
