# GHP Construction with Duration Matching

This notebook is used for constructing portfolio of bonds using duration matching to hedge liabilities.

If you have the assets on hand, you can secure future liabilities by matching the duration of your liabilities with the durations of your assets to immunize yourself against level shifts in the yield curve. In practice, you might also want to protect against changes in the slope and curvature of the yield curve by using convexity hedging, but duration hedging is a simple but essential step towards ensuring that you will have the money to meet your liabilities when interest rates fluctuate.

## Duration Matching
The formula to find the weights of GHP portfolio consisting of 2 bonds is:
$$ w_s = \frac{d_l -d_t}{d_l - d_s} $$ 
where $w_s$ is the weight in the short duration bond which has duration $d_s$ and the duration of the longer bond is $d_l$. We designate the targeted duration as $d_t$.
