# PokerTracker 4
PokerTracker imports and parses the hand histories that poker sites create during online play and stores the resulting statistics and information in a local PostgreSQL database. The information is used for in-game opponent analysis using a custom Heads-Up Display (HUD), an automatic real-time overlay of each players statistics for each poker table, and for statistical analysis and review using custom reports, statistics, and filters. 

* <b>Custom HUD</b> - Displays general game state data and custom statistics on each table for each opponent. Used to identify mathematically exploitable frequencies resulting from inefficient strategies used by opponents.

* <b>Example Statistic Usage</b>

<OL>
<LI>Fv3B = Fold versus Three Bet: The frequency the player raises then folds to re-raise
<LI>Represented as a percentage from 0 to 99. A value of 0 means that every time this player raises he has called a re-raise.
<LI>Fv3B = 0, This player never folds after raising. The strategic adjustment made would be to only re-raise this player with high equity holdings. This player continues at a high frequency therefore increasing the importance of having a lot of equity.
<LI>Fv3B = 99, This player almost always folds after raising. Meaning that we can re-raise them with a high freuqency and win the put uncontested. This is a scenario where we would bluff with low equity holdings because this player folds too frequently for our equity to matter significantly.
</OL>

<img src="PokerTracker 4 - Custom HUD.jpg"
     alt="Custom HUD"
     style="float: left; margin-right: 10px;" />

* <b>Custom Reporting</b> - Uses custom statistics and filters to isolate specific segments of data for statistical and strategic analysis, such as identifying population benchmarks or profitability cut-offs.

<img src="PokerTracker 4 - Custom Reporting.png"
     alt="Custom Reporting"
     style="float: left; margin-right: 10px;" />

* <b>Custom Statistic Coding</b> - Custom coded statistics using SQL expressions used to track key metrics. Statistics are used in HUDs, filters, and reports. Statistics measure specific player behavior for various segments of the game tree. 

<img src="PokerTracker 4 - Custom Statistic Coding.png"
     alt="Custom Statistic Coding"
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





