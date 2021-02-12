---
title: AC Survey
author: Abdul Najah
date: '2021-01-21'
authors:
  - najah
summary: Analysis of the data recieved from the demo AC survey
output:
  blogdown::html_page:
    keep_md: true
    toc: true
    toc_depth: 3
    number_sections: true
    fig_width: 6
---
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />







### Data summary

**Main Variables**


```
##  [1] "ivr_mobile_number"        "age"                     
##  [3] "gender"                   "audience_name"           
##  [5] "ivr_response_status"      "ivr_response_status_name"
##  [7] "ac_name"                  "pc_name"                 
##  [9] "district_name"            "state_name"              
## [11] "q1_response"              "q2_response"
```

------------------------------------------------------------------------

**Variable summary**

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> state_name </th>
   <th style="text-align:right;"> n_call </th>
   <th style="text-align:right;"> n_ac </th>
   <th style="text-align:right;"> n_pc </th>
   <th style="text-align:right;"> q1_response_rate </th>
   <th style="text-align:right;"> q2_response_rate </th>
   <th style="text-align:right;"> q1_and_q2_response_rate </th>
   <th style="text-align:right;"> q1_or_q2_response_rate </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:right;"> 21112 </td>
   <td style="text-align:right;"> 170 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 2.73 </td>
   <td style="text-align:right;"> 2.90 </td>
   <td style="text-align:right;"> 1.87 </td>
   <td style="text-align:right;"> 3.76 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:right;"> 31314 </td>
   <td style="text-align:right;"> 198 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 7.49 </td>
   <td style="text-align:right;"> 9.22 </td>
   <td style="text-align:right;"> 5.97 </td>
   <td style="text-align:right;"> 10.74 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Telangana </td>
   <td style="text-align:right;"> 28027 </td>
   <td style="text-align:right;"> 91 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 9.43 </td>
   <td style="text-align:right;"> 9.65 </td>
   <td style="text-align:right;"> 7.25 </td>
   <td style="text-align:right;"> 11.83 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Uttar Pradesh </td>
   <td style="text-align:right;"> 15090 </td>
   <td style="text-align:right;"> 393 </td>
   <td style="text-align:right;"> 80 </td>
   <td style="text-align:right;"> 5.88 </td>
   <td style="text-align:right;"> 7.67 </td>
   <td style="text-align:right;"> 4.63 </td>
   <td style="text-align:right;"> 8.91 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> West Bengal </td>
   <td style="text-align:right;"> 19195 </td>
   <td style="text-align:right;"> 284 </td>
   <td style="text-align:right;"> 42 </td>
   <td style="text-align:right;"> 4.68 </td>
   <td style="text-align:right;"> 5.70 </td>
   <td style="text-align:right;"> 3.44 </td>
   <td style="text-align:right;"> 6.94 </td>
  </tr>
</tbody>
</table>

---

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> state_name </th>
   <th style="text-align:right;"> mean_call_ac </th>
   <th style="text-align:right;"> mean_q1_or_q2_response_ac </th>
   <th style="text-align:right;"> mean_age_ac </th>
   <th style="text-align:right;"> mean_male_pc </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:right;"> 124.19 </td>
   <td style="text-align:right;"> 4.67 </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:right;"> 158.15 </td>
   <td style="text-align:right;"> 16.99 </td>
   <td style="text-align:right;"> 45.73 </td>
   <td style="text-align:right;"> 74.87 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Telangana </td>
   <td style="text-align:right;"> 307.99 </td>
   <td style="text-align:right;"> 36.44 </td>
   <td style="text-align:right;"> 36.74 </td>
   <td style="text-align:right;"> 66.56 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Uttar Pradesh </td>
   <td style="text-align:right;"> 38.40 </td>
   <td style="text-align:right;"> 3.42 </td>
   <td style="text-align:right;"> 37.85 </td>
   <td style="text-align:right;"> 84.06 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> West Bengal </td>
   <td style="text-align:right;"> 67.59 </td>
   <td style="text-align:right;"> 4.69 </td>
   <td style="text-align:right;"> 25.04 </td>
   <td style="text-align:right;"> 44.71 </td>
  </tr>
</tbody>
</table>


------------------------------------------------------------------------

# States




------------------------------------------------------------------------

## Calls & Responses

### States

The following plot shows the proportion and the number of calls made and responded in each state along with the break-up of the gender. It is evident that, there is a huge gender bias in the calls made in the all three states except West Bengal. Also, among the four states, Uttar Pradesh seems to have received the least number of calls contradicting its population size.

Throughout the analysis, we count a responded call as the ones that have answered at least one of the two questions. It is quite evident that the number of respondents is relatively much less, averaging around 5% of the calls made. At the same time, the gender proportion of the respondents is identical to the callers.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-5-1.png" width="768" />

------------------------------------------------------------------------

We use density plots to observe the distribution and the differences of `Number of calls` , `Number of responses` and the `Response rate`. among the states. Response rate is simply the percentage of the calls that received response to at least one of the the two questions. We observe significant variation among the states on all three variables.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-6-1.png" width="768" /><img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-6-2.png" width="768" /><img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-6-3.png" width="768" />

------------------------------------------------------------------------

### Assembly constituencies

We explore the variation within the state by looking at the assembly constituency level.The following box plots illustrates the distribution of the calls, response and the response rate in all unique assembly constituencies in each state. The jittered dots represents the relavant value of the variables in every unique constituency in each states.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-7-1.png" width="768" />




------------------------------------------------------------------------

## Gender

Density plots along the lines of gender does reflect the sample bias in the gender as expected . Telengana and Rajasthan have a fair distribution given we take the sample bias into account while Uttar Pradesh has a inconsistent distribution. West Bengal seems to have a symmetrical distribution.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-9-1.png" width="768" />







--


## Age

The following plot depicts the age distribution along with gender of the the callers. Looking at the aggregate picture, we observe that the proportion of calls to individuals less than 25 years is quite high among women.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-13-1.png" width="768" />

Once we look further into the states, the general trend fades away and looks more like the gender is fairly distributed along the age across the states. All the states except West Bengal has a fair distribution of age among both genders, while West Bengal one is extremely right skewed with a high number of young responders under 25 years of age.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-14-1.png" width="768" />







## Demography

### Urban


In this section, we are attempting to ensure that there is no urban/rural bias in the sample. We define urban ACs as the constituencies with more than 40% of urban areas.  The distribution of urban/rural ACs in the dataset looks like this. 


<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> state_name </th>
   <th style="text-align:right;"> urban_y </th>
   <th style="text-align:right;"> count </th>
   <th style="text-align:right;"> n_ac </th>
   <th style="text-align:right;"> calls_per_ac </th>
   <th style="text-align:right;"> response_per_ac </th>
   <th style="text-align:right;"> response_rate_per_ac </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 11318 </td>
   <td style="text-align:right;"> 85 </td>
   <td style="text-align:right;"> 133.15 </td>
   <td style="text-align:right;"> 5.25 </td>
   <td style="text-align:right;"> 3.94 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 5438 </td>
   <td style="text-align:right;"> 47 </td>
   <td style="text-align:right;"> 115.70 </td>
   <td style="text-align:right;"> 4.51 </td>
   <td style="text-align:right;"> 3.90 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 27612 </td>
   <td style="text-align:right;"> 170 </td>
   <td style="text-align:right;"> 162.42 </td>
   <td style="text-align:right;"> 17.58 </td>
   <td style="text-align:right;"> 10.82 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 3688 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 141.85 </td>
   <td style="text-align:right;"> 14.54 </td>
   <td style="text-align:right;"> 10.25 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Uttar Pradesh </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 13522 </td>
   <td style="text-align:right;"> 335 </td>
   <td style="text-align:right;"> 40.36 </td>
   <td style="text-align:right;"> 3.54 </td>
   <td style="text-align:right;"> 8.76 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Uttar Pradesh </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1381 </td>
   <td style="text-align:right;"> 53 </td>
   <td style="text-align:right;"> 26.06 </td>
   <td style="text-align:right;"> 2.53 </td>
   <td style="text-align:right;"> 9.70 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> West Bengal </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 14525 </td>
   <td style="text-align:right;"> 210 </td>
   <td style="text-align:right;"> 69.17 </td>
   <td style="text-align:right;"> 5.07 </td>
   <td style="text-align:right;"> 7.33 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> West Bengal </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 4085 </td>
   <td style="text-align:right;"> 63 </td>
   <td style="text-align:right;"> 64.84 </td>
   <td style="text-align:right;"> 3.78 </td>
   <td style="text-align:right;"> 5.83 </td>
  </tr>
</tbody>
</table>

### Calls

We see that both mean values and calls per constituency is considerably less for urban constituencies. We scrutinise this further by looking at a box plot.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-18-1.png" width="768" />

### Response rate



<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-19-1.png" width="768" />


It seems that there is a rural bias in the sampling even though the response rate from urban and rural area looks similar. We can statistically confirm this using  a t-test. 


```
## 
## 	Welch Two Sample t-test
## 
## data:  survey_all_urban$count by survey_all_urban$urban_y
## t = 24.685, df = 22658, p-value < 2.2e-16
## alternative hypothesis: true difference in means is not equal to 0
## 95 percent confidence interval:
##  15.10509 17.71079
## sample estimates:
## mean in group 0 mean in group 1 
##        126.7733        110.3653
```
We observe that there is a difference in the mean's of both urban and rural constituencies and it is significant at .005 level.  Hence, it is safe to conclude that there is a rural bias in the sample.




### SC/ST

In the following table, `sample_prop` is the proportion of calls made to the that particular category and the `electorate_prop` is the electorate proportion of that category. 

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> State_Name </th>
   <th style="text-align:left;"> reservation </th>
   <th style="text-align:right;"> electorate_prop </th>
   <th style="text-align:left;"> state_name </th>
   <th style="text-align:right;"> calls_prop </th>
   <th style="text-align:right;"> response_prop </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:left;"> GEN </td>
   <td style="text-align:right;"> 0.79 </td>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:right;"> 0.93 </td>
   <td style="text-align:right;"> 0.94 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:left;"> SC/ST </td>
   <td style="text-align:right;"> 0.21 </td>
   <td style="text-align:left;"> Gujarat </td>
   <td style="text-align:right;"> 0.07 </td>
   <td style="text-align:right;"> 0.06 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:left;"> GEN </td>
   <td style="text-align:right;"> 0.71 </td>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:right;"> 0.70 </td>
   <td style="text-align:right;"> 0.69 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:left;"> SC/ST </td>
   <td style="text-align:right;"> 0.29 </td>
   <td style="text-align:left;"> Rajasthan </td>
   <td style="text-align:right;"> 0.30 </td>
   <td style="text-align:right;"> 0.31 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Uttar_Pradesh </td>
   <td style="text-align:left;"> GEN </td>
   <td style="text-align:right;"> 0.79 </td>
   <td style="text-align:left;"> Uttar Pradesh </td>
   <td style="text-align:right;"> 0.77 </td>
   <td style="text-align:right;"> 0.77 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Uttar_Pradesh </td>
   <td style="text-align:left;"> SC/ST </td>
   <td style="text-align:right;"> 0.21 </td>
   <td style="text-align:left;"> Uttar Pradesh </td>
   <td style="text-align:right;"> 0.23 </td>
   <td style="text-align:right;"> 0.23 </td>
  </tr>
</tbody>
</table>

In both UP and Rajasthan, there is a fair representation of SC/ST community in the calls made and responses received.  But, in Gujarat, representation of SC/ST in this samples falls way below of their electoral proportion. 


# Answers

This analysis only includes only individuals who have  atleast responded either one of the two questions.

## All India

### Education

In this grapph, we look at how people's response differes with their education levels.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-22-1.png" width="768" />

### Gender

Here, we check if we observe any difference in the answers with regards to gender. As we can see, clearly there no difference along the gender lines.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-23-1.png" width="768" />



## States

In the following charts, we observe how answers variate in different states with regards to education and gender.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-24-1.png" width="768" />

---
  
<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-25-1.png" width="768" />

---

### Gender

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-26-1.png" width="768" />
  
  
