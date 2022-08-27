# CMS Spread Option

A constant maturity swap (CMS) spread option makes payments based on a bounded spread between two index rates (e.g., a GBP CMS rate and a EURO CMS rate).  The GBP CMS rate is calculated from a 15 year swap with semi-annual, upfront payments, while the EURO CMS rate is based on a 15 year swap with annual, upfront payments. 

We assume that both the forward GBP and EURO CMS rates follow geometric Brownian motion under their respective  -forward measures.  Here respective initial forward CMS rates are calculated.  The forward rates are then convexity adjusted from respective parallel bonds specified using

•	the same payment times as the underlying CMS,

•	coupon equal to the forward CMS rate, Coupon payment is computed as https://finpricing.com/lib/FiBondCoupon.html

•	initial bond yield equal to the forward CMS rate.

From the above the correlation, under foreign T-forward measure, between the Brownian motions respectively driving the foreign bond yield and GBP swap rate processes constrains the correlation between the Brownian motions driving the Euro bond yield and forward GBP CMS rate processes under domestic T-forward measure.  

To evaluate the expression above, we require the SDE followed by the forward exchange rate process under domestic T-forward measure.  This is derived by changing measure from foreign  -forward measure, to domestic risk-neutral measure, to domestic  -forward measure.

References:

https://osf.io/9db5u/download
