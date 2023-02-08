# Stochastic-modelling
MScFE 622 STOCHASTIC MODELING
Group Work Project # 1
See grading rubric here.
Scenario
Financial engineers can use volatility models to price options. As a trio (or duo) of
quants, you will be tasked with pricing options using different models. The outputs of
your work are used all day, every day by the options desk – a profitable part of the firm’s
market making. Do your job correctly, and you will be considered the ‘rocket scientists’
of the group. Do your job incorrectly, and well… let’s not go there.
A long-time client of the bank is looking to purchase an OTC Asian option on the
company SM. Remember that an Asian call option payoff at maturity is simply defined
as:
max(𝐴𝑣𝑔 𝑆
𝑡
( ) − 𝐾; 0) 𝑓𝑜𝑟 𝑡 = {0, 1, …𝑇}
(Remember to include the current price today, 𝑆 , in the calculation of the average St).
0
The client is not so sure about the maturity she wants to consider for the option.
Fortunately, you have information on vanilla options traded in the market, with the
underlying asset being the stock of SM (for SM Energy Company), in the attached Excel
file. SM stock is currently trading at $232.90 USD:
Click here to download Option Data to complete the Group Work Project.
Tasks
Step 1
a. Initially, the client seems to be looking for a very short maturity for her derivative
(around 15 days). This is a good job for Team Member A!
Team member A needs to calibrate a classic Heston (1993) model (without
jumps) to the observed market prices for both call and put options. Use the Lewis
(2001) approach with a regular MSE error function. For the moment, consider a



constant annual risk-free rate of 1.50%. Assume 1 year has 250 trading days. For
the case of put options, note that you can either:

i. Use the Lewis (2001) closed form for put options that you have on the
paper: Lewis, Alan L. "A simple option formula for general jump-diffusion
and other exponential Lévy processes." (2001)


ii. (preferred) Use put-call parity with the closed-form solution for the call
option.
As part of the pricing team, Team member A needs to report the parameter
values resulting from the calibration, describe the whole process for the other
team members to know (to which maturity (-ies) you calibrated the model, error
function considered,…), and briefly discuss the final calibration including graphs
that properly illustrate the fit of the calibration.

b. In order to double-check the different model parameters resulting from a
calibration, Team member B will repeat the same process as Team member A,
but using the Carr-Madan (1999) pricing approach to calibrate the Heston (1993)
model. Make sure that you repeat all the tasks in (a), including a discussion on
why (or why not) you obtain similar values for the different parameters as via
Lewis (2001). You can use put-call parity as well to calibrate to put option prices.

c. Using the calibrated parameters you consider appropriate from the previous
tasks, Team member C will price the Asian call option for the client. In this case,
the client wants an ATM Asian option with 20 days maturity.
As team member in charge of pricing for the client, make sure that you:

i. Obtain the ‘fair price’ of the instrument using Monte-Carlo methods in a
risk-neutral setting. Make sure you perform enough simulations in
Monte-Carlo. (Hint: You may want to check some of the Derivative Pricing
material for this)

ii. As part of the bank’s profit, you charge a 4% fee on the price to obtain the
final price that the client will end up paying. Make sure to clearly state this
in your report.

iii. Include in your report a brief but complete non-technical description (that
a client can understand) on the process you undertook for pricing,
including calibration steps and choices that you consider relevant.
Note: For Groups of 2, please use the responsibilities for Members A and C only.

Step 2
Unfortunately, the client seems hesitant about the short maturity considered in step 1.
After giving it some thought, she thinks that an instrument with 60 days maturity would
better adapt to her needs.
a. Team member C will now repeat Task (a) in Step 1 for the new case at hand
(60-day maturity instrument) using a Heston model with jumps (i.e., Bates, 1996
model). Make sure you follow all the proper steps in the calibration of Bates, and
that you explain them. Except for the mentioned change of the target maturity,
use all other instructions from Task (a) in Step 1.
b. Team member A will repeat the previous Task (a) in Step 2 using Carr-Madan
(1999) approach to Bates (1996) model. Except for the mentioned change of the
target maturity, use all other instructions from Task (b) in Step 1.
c. Team member B will perform a pricing process similar to Task (c) of Step 1. In
this case, rather than an OTC instrument, the client has decided she wants to buy
a Put option on firm SM with 70 days maturity and moneyness of 95% (i.e., strike
is 95% of the current price).
Note: For Groups of 2, please use the responsibilities for Members A and C only.
Step 3
Since the initial idea of our client was to purchase a very short-term maturity OTC
instrument, we were not so concerned about the potential risks arising from future
evolutions of interest rates. However, considering how volatile are the demands of the
client (first asks for a very short-term Asian, then a mid-term regular put option… what
will be next?), your boss asks the team to provide some insights on future interest rates.
Specifically, as a team, you will need to:
a. Calibrate a CIR (1985) model considering current rates, describing the overall
process.
Since we as a bank operate mostly on a European setting, we will consider
Euribor rates. Current rates and maturities are given in the following table:


Make sure you properly build the term structure of the Euribor. Then, use the
cubic spline method to interpolate weekly rates for a period of 12 months (1
years). Calibrate the model to interpolated term structure. Make sure you briefly
describe the process, clearly show the output of the calibration, and discuss the
different parameters obtained as well as the fit of your model under those
parameters to market rates (include graphs).
b. Given the different CIR model parameters obtained in the previous step, simulate
Euribor 12-month rates daily for a period of 1 year. Perform 100,000 Monte-Carlo
simulations. Discuss the results obtained (include graphs) regarding:
i. Select a level of confidence you are comfortable with, which is the range
(max and min) that the 12-month Euribor can take in the next year?
ii. What is the expected value of the 12-month Euribor in 1 year?
iii. How will this expected number affect the pricing of your products in 1 year
versus the current 12-month Euribor rate?
Step 4
As a team, the group will organize both the Python file for all the steps as well as work
together on a report that contains the answers to all the questions above (except for the
code) in a clear and organized manner (think about how you would present this to your
boss).
Submission Requirements and Format
One team member submits the following on behalf of the entire group:
● 1 PDF document containing ONLY the answers to the questions, EXCLUDING
code
○ Use the available Report Template and fill out the required information in
the first page.
● 1 zipped file that contains:
○ Jupyter notebook that is executable
○ html of both the Jupyter notebook containing all code, results, and graphs
*Use Google Colab or GitHub to collaborate in completing the executable Python program.
NOTE: The PDF must be uploaded separately from the zipped folder that includes any
other types of files. This allows Turnitin to generate a similarity report.

Your instructor will evaluate your group submission for GWP1 using the following rubric:
Quantitative Analysis
(Open-Ended Questions)
40 Points
Technical and Non-Technical Reports
30 Points
Writing and Formatting
20 Points
The group is able to apply results,
formulas, and their knowledge of
theory to real-life finance scenarios
by doing the following:
● Providing all the necessary
information to support their
arguments.
● Presenting arguments that reflect
group discussion and research.
● Using authoritative references to
support a position and provide
updated information.
● Concluding with practical
takeaways for more insightful
financial decision-making.
Technical reports contain 3 parts:
1) code for each question (be sure to
explicitly state the question number),
2) the corresponding output of that code,
and
3) interpretations and/or recommended
courses of action that reasonably follow
from those results.
Note: Technical reports will include the
technicalities of models, such as names,
methods of estimation, parameter
values, etc., and exclude generalities
about the work done. It should NOT
include names of Python code that were
used.
A submission that looks
professional should:
● Include the axes, labels, and
scales in graphs.
● Be free of significant
grammatical errors or typos.
● Be an organized,
well-structured, and easy-to-read
document.

● Include proper citations and a
bibliography in MLA format.
Non-technical reports contain 3 parts:

1) clear explanation of results;
2) the recommended course of action
that follows; and
3) the identification of factors that
impact each portfolio.
Note: AVOID all references to model
names, algorithms, and unnecessary
details. Instead, focus on the investment
decision.

