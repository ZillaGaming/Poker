# PokerTracker 4
PokerTracker imports and parses the hand histories that poker sites create during online play and stores the resulting statistics and information in a local PostgreSQL database. The information is used for in-game opponent analysis using a custom Heads-Up Display (HUD), an automatic real-time overlay of each players statistics for each poker table, and for statistical analysis and review using custom reports, statistics, and filters. 

* <b>Custom HUD</b> - Displays general game state data and custom statistics on each table for each opponent. Used to identify mathematically exploitable frequencies in opponent's strategies.

* <b>Example Statistic Usage</b>

<OL>
<LI>FvMR = Fold versus Minimum Raise: The frequency the player folds to a minimum raise. Represented as a percentage from 0 to 99. A value of 99 means that every time this player faces a minimum raises he has folded and conceded his equity share in the pot. 
<LI> Example Scenario = Two Players. Blinds $25/$50. Starting pot (reward) is $75. Player 1 minimum raises and risks an additional $75 (total of $100) to win the $75. Let's assume that Player 1 has no equity and only wins if Player 2 folds (concedes the pot). Player 1 is risking $75 to win $75. If Player 1 wins the pot 50% of the time Player 1 breaks even. If that number is greater than 50% he makes money every time and should always make this play. If that number is less than 50% he loses money every time and should never make this play. If we give Player 1 equity (winning the pot without Player 2 folding) than the breakeven threshold of 50% goes down depending on how much equity Player 1 recieves. In a real scenario, Player 1 would always have more than 0% equity. This establishes a benchmark that if Player 2 has FvMR > 50% than Player 1 has identified a strategic opportunity that is ALWAYS profitable even with no equity. 
<LI> Business Relevance = In business it is rare to have such a fixed set of constraints like you would have within a game, however the risk-reward analysis can prove useful in a business setting by ensuring that you are maximizing your resources (money, time, etc.) to ensure that the business is pursuing projects that will have the greatest return on investment (ROI). In this specific example we looked at a simplified poker model that examined the application of the statistic FvMR, however this could easily be replaced by an online business model examining website traffic, click through rates, total value of sales, cost per click or acquisition, etc. 
</OL>

<img src="PokerTracker 4 - Custom HUD.jpg"
     alt="Custom HUD"
     style="float: left; margin-right: 10px;" />

* <b>Custom Statistic Coding</b> - Custom coded statistics using SQL expressions used to track key metrics. Statistics are used in HUDs, filters, and reports. Statistics measure specific player behavior for various segments of the game tree. 

<img src="PokerTracker 4 - Custom Statistic Coding.png"
     alt="Custom Statistic Coding"
     style="float: left; margin-right: 10px;" />

* <b>Custom Reporting</b> - Uses custom statistics and filters to isolate specific segments of data for statistical and strategic analysis, such as identifying population benchmarks or profitability cut-offs.

<img src="PokerTracker 4 - Custom Reporting.png"
     alt="Custom Reporting"
     style="float: left; margin-right: 10px;" />

* <b>HUD Builder</b> - Used to create the HUDs. Builder shows each statistical group (panel on the table dsiplay), the custom statistics involved with each group, and an approximated representation of the table visualization.

<img src="PokerTracker 4 - HUD Builder.png"
     alt="HUD Builder"
     style="float: left; margin-right: 10px;" />

# Microsoft Excel

* <b>Bluffing and Bluff Catching Model</b> - Used to calclualte combinatorics required for game theory optimal (GTO) bluffing and bluff catching frequencies as well as the expected value (EV) based on various frequencies, bet sizes, and equities.

<img src="Microsoft Excel - Bluffing and Bluff Catching Model.png"
     alt="Microsfot Excel - Bluffing and Bluff Catching Model"
     style="float: left; margin-right: 10px;" />

# CardRunnersEV
CardRunnersEV is poker analysis software that will allow you to build decision trees and calculate the EV of every decision within that tree.

* <b>Game Tree Analysis</b> - Used to build the postflop game trees and explore permutations of possible outcomes based on different bet actions, bet sizes, and stack sizes.

<img src="CardRunnersEV - Game Tree Analysis.png"
     alt="Cardrunners EV - Game Tree Analysis"
     style="float: left; margin-right: 10px;" />

# PIOSolver
PioSOLVER is a GTO solver for Texas Hold'em. It handles postflop spots with arbitrary starting ranges, stack sizes, bet-sizes as well as desired accuracy and displays the solution tree.

* <b>PostFlop Range Tree Builder</b> - Used to build the postflop game trees and explore permutations of possible outcomes based on different bet actions, bet sizes, and stack sizes.

<img src="PIOSolver - PostFlop Range Tree Builder.png"
     alt="PostFlop Range Tree Builder"
     style="float: left; margin-right: 10px;" />

* <b>PostFlop Solver Analysis</b> - Visualization of EV for GTO strategies, particularly useful for identifying areas where mixed strategies are implemented (multiple strategies deployed at non-zero frequencies).

<img src="PIOSolver - PostFlop Solver Analysis.png"
     alt="PostFlop Solver Analysis"
     style="float: left; margin-right: 10px;" />





