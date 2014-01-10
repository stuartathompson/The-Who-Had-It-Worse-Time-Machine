The Who Had It Worse Time Machine
=================================

An interactive showing how today’s young adults face serious challenges in the form of high and rising tuition fees, a tough job market and high housing prices

Coding, design, layout and data work by Stuart A. Thompson

Writing by Rob Carrick

Time Machine graphic by Murat Yukselir

See the full version here: http://www.theglobeandmail.com/globe-investor/personal-finance/household-finances/proof-that-young-adults-have-it-worse-much-worse-than-30-years-ago/article10280516/

Nominated for best Data Storytelling (Big Media) at the 2013 Data Journalism Awards: https://review.wizehive.com/voting/view/dja2013/14524/1244521/0
Won silver for best infogrpahic at the 2013 Canadian Online Publishing Awards: http://www.theglobeandmail.com/community/digital-lab/globe-and-mail-wins-four-canadian-digital-publishing-awards/article15432499/

Description of the project
-------
Today’s young adults face serious challenges in the form of high and rising tuition fees, a tough job market and high housing prices. But are they worse off than previous generations? Much has been written about this issue, but a data presentation has never been used to prove the point. We wanted to create the definitive data tool for explaining this trend in hard numbers. The resulting visualization went viral: The “Who Had It Worse Time Machine” let readers compare their graduating year with those from over 30 years ago to see whether they had it better or worse than that time period. We used every significant metric available, from housing prices to income.

The results paint a compelling portrait for today’s youth. They are worse off on every significant metric. Most dramatically, their income is lower today (when adjusted for inflation) while other costs are much higher. The tool and related column resonated so much with our readers that it was shared more than 3,500 times on social media and earned hundreds of comments.

What data did you use and how did you obtain it?
-------
One of the reasons a tool like this was never created was the difficulty in assembling such a large amount of data over several years. We defined a date range going back as far as 1976 and set out to gather data on the metrics most relevant to students and young adults. As such, the data came from more than half a dozen sources.

Income, unemployment and tuition figures were downloaded from a database run by Statistics Canada. Average housing prices were provided in spreadsheet form by the Canadian Real Estate Association. Monthly five-year mortgage rates came from the Bank of Canada in spreadsheet form and were averaged over each year. Student loan data came from the government-run Human Resources and Skills Development agency in a spreadsheet. For data research purposes, we also collected Income tax data from library technicians at the Canada Tax Foundation, which were faxed in hard-copy and needed to be entered manually.

Income, housing and student loan data were adjusted for inflation using a tool provided by the Bank of Canada.

Technical challenges, tools used
-------
The data was analyzed using Excel. Preliminary charts were made, comparing actual dollars with adjusted figures and charting several metrics side by side. Many visualization options were considered and tested during this phase, but the significant difference in dollar amount between housing and all other metrics made charting all the figures together a difficult challenge. A custom radar chart was created as the main visualization piece using Raphael.js. An SVG path equation was created in several steps. First, we set the maximum and minimum values for each set of data. Then, a percent range was created using the relevant value.For example, if the highest house price was $339,200 and the lowest was $147,430, a value of $339,200 would be considered 100 per cent and $147,430 would be considered 0 per cent. This equation was used to plot several distinct values on a single radar chart by calculating the percentage difference from the center of the radar chart to the end point of each axis. This made the scale of actual dollar amounts moot and let us display the variety of data together at one time.

A jQuery UI slider was used to let readers scroll through several years and see how values changed. The trend became clear: a tall, skinny chart in 1976 signified high income and low expenses, while a fat, stout chart in 2010 showed lower income and much higher expenses.

A series of smaller line charts were created using the g.Raphael library to make the trendlines clear over time and to add an additional explanation for each metric. These charts were edited for style and additional lines and axes were added to overlay additional metrics, such as adding mortgage rates over the housing price.

