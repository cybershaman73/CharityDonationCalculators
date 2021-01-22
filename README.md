# Charity Donation Calculator
  This Excel-based calculator, derived from original rewards calculator created by EDEN POOL, will take your pools active stake, pledge and current network variables to           provide you with the total rewards given to the pool for making blocks in a given epoch. Those rewards are then used to calculate, based on your pool’s operational               expenses, the profit you will make and how much you have available for charity donations.

1.	SHEET1 labeled “EPOCH-243” is the reward calculator. There are variables that need to be changed PER EPOCH to get accurate pool rewards that are used to determine profit/expense/donation in SHEET2. Those variables that must be changed per epoch are bold highlighted in RED along left most column:

      > 	d, decentralization factor
      > 	T, Total ADA in circulating supply (pull off pooltool.io, pool.pm, adapools.org, etc.)
      > 	Ts, Amount of the Total ADA circulating that is actively staked to community pools
      >   Ps, Total Active Stake in the pool
      > 	POOL real blocks, this value comes from running LeaderLogs or waiting until the end of an epoch to see how many blocks you were scheduled to make.

      f.	Note the Fixed Cost & Pool tax margin under “Rewards Distribution table” Those will be specific to your setup and have to be entered into colum “D” under “Pool Fixed         Cost” & “Pool Variable Fee”
 
      g.	The “Optimal Rewards” for the pool are based on making the expected blocks based on your active stake. The “Real Rewards” are what the protocol pays you based on how         many blocks you actually made. This is where pool luck comes into play!!

2.	SHEET2 labled “PROFITS-243” takes values from sheet 1 and calculates your pools profits for that epoch based on your expenses. You can add however many rows of expenses you want. 

      a.	The “5-day moving average ADA price $USD” is used to provide a fair market value for our donations made in USD. If you can donate in ADA, you don’t have to worry about       this conversion and make appropriate changes to the calculator. Source for 5-day moving average: https://www.barchart.com/crypto/quotes/%5EADAUSD/technical-analysis

      b.	Monthly expenses are broken into 6 epochs periods, 5 days each. 

      c.	Make sure to add your expenses for each category into the formula for the cell. 

      d.	The “Pool Operator Stipend” expense is a variable expense based on this formula: 
      =((PoolFixedFeeIncome+PoolVariableFeeIncome)/(PoolActiveStake*5dayMovingAvg$ADAprice))*(PoolActiveStake*5dayMovingAvg$ADAprice)/2.8

      i.	The “2.8” factor of division at the end of the formula can be changed to provide whatever amount of income the SPO feels is fair for their efforts in maintaining the         pool. This is considered your stipend and will be proportional to pool active stake & price of ADA.

      e.	The “Marketing Variable” income follows the same formula with a smaller factor of division. Again, this can be modified to fit your budget.
 
      f.	Once all your expenses are calculated, the income is pulled from the first sheet automatically. This allows for a profit to be calculated. 

      g.	There are currently NO TAXES being calculated with these sheets. You can add that at your own discretion per the tax laws of your region.

      h.	With expenses, income and profit calculated, you can now enter in your desired charity donations. Since GROW is 100% profits to charity, I don’t have a percentage           calculator built in. That can be done easily by added a percentage rule to the formula in cells F17 & F18. 
