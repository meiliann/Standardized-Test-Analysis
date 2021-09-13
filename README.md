# Project 1: Standardized Test Analysis

## Problem Statement
The SAT has had a complete makeover in March 2016 to catch up to the growing popularity of ACT. As part of College Board data science team, I would like to explore the trends of SAT and ACT participation from 2017 to 2019 so we can identify key states that we can allocate our resources to increase participation rates.

### Data dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT|The list of all states in US| 
|sat_part_2017|float|SAT|State participation rate in 2017|
|sat_ebrw_2017|integer|SAT|State mean Evidence based reading & writing score in 2017|
|sat_math_2017|integer|SAT|State mean Math score in 2017|
|sat_total_2017|integer|SAT|State mean Total score in 2017|
|sat_part_2018|float|SAT|State participation rate in 2018|
|sat_ebrw_2018|integer|SAT|State mean Evidence based reading & writing score in 2018|
|sat_math_2018|integer|SAT|State mean Math score in 2018|
|sat_total_2018|integer|SAT|State mean Total score in 2018|
|sat_part_2019|float|SAT|State participation rate in 2019|
|sat_ebrw_2019|integer|SAT|State mean Evidence based reading & writing score in 2019|
|sat_math_2019|integer|SAT|State mean Math score in 2019|
|sat_total_2019|integer|SAT|State mean Total score in 2019|
|act_part_2017|float|ACT|State participation rate in 2017|
|act_comp_2017|float|ACT|State mean Composite score in 2017|
|act_part_2018|float|ACT|State participation rate in 2018|
|act_comp_2018|float|ACT|State mean Composite score in 2018|
|act_part_2019|float|ACT|State participation rate in 2019|
|act_comp_2019|float|ACT|State mean Composite score in 2019|
|act_required|object|ACT|States that require ACT|
|sat_required|object|SAT|States that require SAT|

### Overview
To start with, I will use the existing data provided - SAT Scores by State from 2017 to 2019, ACT Scores by State from 2017 to 2019. I have also referred to external sources to find out the states which require SAT and/or ACT to further explore the relationship between these data.

### Summary
After investigation, I notice that state's test policy has a positive correlation with participation rates. If state offers or requires SAT, the test participation's rate would be high. The same goes to ACT as well. <br>
However, I notice that when participation rates are high, score will be low as they have a negative correlation. This is probably due to students who are not well-prepared have to take the test and didn't score well. <br>
I have also noticed that SAT and ACT participation rates are negatively correlated. When SAT participation rate is high, ACT participation rate is low. This may be due to certain state only requiring students to take either test or students choose to take either test and not both.<br>


### Conclusion and recommendations
Based on analysis of the datasets, I can conclude that states' SAT and ACT participation rates are directly impacted by the state's decision to have either test required. For states that require the test or offer it for free, it's meant to eliminate an extra test for students who were already planning to apply to college while also encouraging those who weren't planning for college to consider it (as quoted from [here](https://blog.prepscholar.com/which-states-require-the-sat)). Also, such testing also mean that the students can take the test for free and can access to free materials required, therefore it encourages high participation in these states which coincides with my findings.

In order to decide which states to focus on given the limited resources, I will consider these factors:<br><br>
1. States that does not require or offer ACT or SAT
&nbsp;&nbsp;<ul><li>As state's direction of which test to take will influence ACT or SAT participation rates, I would like to exclude states that have such policy.</ul></li>

2. ACT participation less than 50%
&nbsp;&nbsp;<ul><li>Since ACT and SAT participation rates are negatively correlated to each other, I will further exclude ACT participation rate that's more than 50% as it would mean the remaining states have potential for SAT participation rate growth.</ul></li>

3. SAT participation below 50th percentile for 3 years consecutively
&nbsp;&nbsp;<ul><li>I would like to target states that's below the 50th percentile for 3 years consecutively as I hope to increase their participation to be above the 50th percentile.</ul></li>

Based on above factors and analysis, I would recommend College Board to focus resources on Alaska, Oregon, California, Indiana, Vermont and Texas.

College Board can work closely with the States to find out how they can help more students to take SAT by tailoring targeted program for each state depending on the local situation. One good reference would be this [research](https://www.act.org/content/act/en.html) published in 2014.
 
