---
title: 'Master file Analysis'
author: "Abdul Najah"
date: '2020-06-10'
params:
  orig_date: "Original Publish Date: 10 June, 2020"
  update_date: !r paste("Updated on:", format(Sys.time(), '%d %B, %Y'))
authors:
  - najah
summary: The main analysis document of the dynasties dataset.
output:
  blogdown::html_page:
    keep_md: true
    toc: true
    toc_depth: 3
    number_sections: true
    fig_width: 6
editor_options: 
  chunk_output_type: inline
---
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />





---

### Document History

Original Publish Date: 10 June, 2020

Updated on: 13 February, 2021

---


In this project we are using a novel dataset compiled by Rahul Verma. This dataset covers the candidates contested in the different levels of elections held from 1974 to 2019 in the state of Uttar Pradesh. This includes assembly, general and local body elections. This dataset connects the contestants to the political offices to their family members within that universe. 

  We define dynast politicians as those who are preceded by family members  who are currently active in politics or were active in the past. Family is defined as a set of individuals who are bound by proximate ties based on blood or marriage, and this definition includes father, mother, grand parents, siblings and in laws. Active in politics refers to holding an office in an elected body or being a candidate in elections. According to this definition, the head of family or the patriarch is considered to be a non-dynast in the year of entry. Precisely, because of the fact that he did not enjoy any advantage of having family members in politics at that point of time. But, ones a family member enter into the universe of politics, in later years patriarch will be considered as dynast along with the descendants.Additionally,  both the first and second member should be entered to the system through assembly or general elections 
  
 
---

















# Summary statistics

##  AE - GE 

This universe includes winners and runner-ups in the general and assembly elections from the year 1977 to 2019. 

- Total observations: 11550
- Number of unique individuals: 5286
- Number of unique families : 300



The following section provides the year  and election level wise break-up  of the observations 

### Assembly Elections

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:right;"> Count </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1974 </td>
   <td style="text-align:right;"> 804 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1977 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1980 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1985 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1989 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1991 </td>
   <td style="text-align:right;"> 794 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1993 </td>
   <td style="text-align:right;"> 800 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1996 </td>
   <td style="text-align:right;"> 804 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2002 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2007 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:right;"> 806 </td>
  </tr>
</tbody>
</table>

---

### General Elections

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:right;"> Count </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1977 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1980 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1984 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1989 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1991 </td>
   <td style="text-align:right;"> 156 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1996 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1998 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1999 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2004 </td>
   <td style="text-align:right;"> 158 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:right;"> 160 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2014 </td>
   <td style="text-align:right;"> 160 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:right;"> 160 </td>
  </tr>
</tbody>
</table>

---


## Levels

Families are spread at multiple office levels. While majority them are present only at the assembly election level, there are  a quite a few of them which is spanned across multiple level of office. The following table summarises that - 


<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
<caption>Table 1: Linkages of families(Category 2)</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> level </th>
   <th style="text-align:right;"> count </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> AE </td>
   <td style="text-align:right;"> 154 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GE-AE </td>
   <td style="text-align:right;"> 94 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AE-LB </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GE-AE-LB </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GE </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
</tbody>
</table>

---


## Dynast presence in the past elections


This chart depicts the  proportion of dynast among the winners of assembly election since 1974.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/dyn proportion over time-1.png" width="768" />

---


## AE GE election contest

 There could four types of election contests:
 
  - Dynast wins against against a Dynast
  - Dynast wins against a Non-dynast
  - Non-dynast wins against another Non-dynast
  - Non-dynast wins against a dynast
  
First table shows count of the contests and the second one shows the proportion of contests. First part represents the winner in both the tables headers.
  
  
  



---

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;"> year </th>
   <th style="text-align:right;"> fam v/s fam </th>
   <th style="text-align:right;"> fam v/s non-fam </th>
   <th style="text-align:right;"> non-fam v/s fam </th>
   <th style="text-align:right;"> non-fam v/s non-fam </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1977 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 465 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1980 </td>
   <td style="text-align:right;"> NA </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 459 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1984 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 72 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1985 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 378 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1989 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 431 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1991 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 422 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1993 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 357 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1996 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 49 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 400 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1998 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 57 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1999 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 53 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2002 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 41 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 322 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2004 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 47 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2007 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> 293 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 62 </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:right;"> 274 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2014 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 38 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 64 </td>
   <td style="text-align:right;"> 76 </td>
   <td style="text-align:right;"> 251 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 38 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;"> year </th>
   <th style="text-align:right;"> fam v/s fam </th>
   <th style="text-align:right;"> fam v/s non-fam </th>
   <th style="text-align:right;"> non-fam v/s fam </th>
   <th style="text-align:right;"> non-fam v/s non-fam </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1977 </td>
   <td style="text-align:right;"> 0.00 </td>
   <td style="text-align:right;"> 0.02 </td>
   <td style="text-align:right;"> 0.01 </td>
   <td style="text-align:right;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1980 </td>
   <td style="text-align:right;"> NA </td>
   <td style="text-align:right;"> 0.03 </td>
   <td style="text-align:right;"> 0.02 </td>
   <td style="text-align:right;"> 0.95 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1984 </td>
   <td style="text-align:right;"> 0.01 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.01 </td>
   <td style="text-align:right;"> 0.91 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1985 </td>
   <td style="text-align:right;"> 0.00 </td>
   <td style="text-align:right;"> 0.03 </td>
   <td style="text-align:right;"> 0.03 </td>
   <td style="text-align:right;"> 0.94 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1989 </td>
   <td style="text-align:right;"> 0.00 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.04 </td>
   <td style="text-align:right;"> 0.89 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1991 </td>
   <td style="text-align:right;"> 0.00 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.05 </td>
   <td style="text-align:right;"> 0.89 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1993 </td>
   <td style="text-align:right;"> 0.00 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.04 </td>
   <td style="text-align:right;"> 0.89 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1996 </td>
   <td style="text-align:right;"> 0.01 </td>
   <td style="text-align:right;"> 0.10 </td>
   <td style="text-align:right;"> 0.05 </td>
   <td style="text-align:right;"> 0.83 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1998 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.10 </td>
   <td style="text-align:right;"> 0.11 </td>
   <td style="text-align:right;"> 0.72 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1999 </td>
   <td style="text-align:right;"> 0.08 </td>
   <td style="text-align:right;"> 0.19 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.67 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2002 </td>
   <td style="text-align:right;"> 0.03 </td>
   <td style="text-align:right;"> 0.10 </td>
   <td style="text-align:right;"> 0.06 </td>
   <td style="text-align:right;"> 0.80 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2004 </td>
   <td style="text-align:right;"> 0.08 </td>
   <td style="text-align:right;"> 0.24 </td>
   <td style="text-align:right;"> 0.09 </td>
   <td style="text-align:right;"> 0.59 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2007 </td>
   <td style="text-align:right;"> 0.02 </td>
   <td style="text-align:right;"> 0.12 </td>
   <td style="text-align:right;"> 0.13 </td>
   <td style="text-align:right;"> 0.73 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:right;"> 0.07 </td>
   <td style="text-align:right;"> 0.31 </td>
   <td style="text-align:right;"> 0.12 </td>
   <td style="text-align:right;"> 0.49 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:right;"> 0.05 </td>
   <td style="text-align:right;"> 0.15 </td>
   <td style="text-align:right;"> 0.11 </td>
   <td style="text-align:right;"> 0.68 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2014 </td>
   <td style="text-align:right;"> 0.05 </td>
   <td style="text-align:right;"> 0.21 </td>
   <td style="text-align:right;"> 0.26 </td>
   <td style="text-align:right;"> 0.48 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:right;"> 0.03 </td>
   <td style="text-align:right;"> 0.16 </td>
   <td style="text-align:right;"> 0.19 </td>
   <td style="text-align:right;"> 0.62 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:right;"> 0.04 </td>
   <td style="text-align:right;"> 0.29 </td>
   <td style="text-align:right;"> 0.20 </td>
   <td style="text-align:right;"> 0.48 </td>
  </tr>
</tbody>
</table>

---

## Elections won

This table shows the count of the unique individuals with regards to the number of elections they have **won**

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
<caption>Table 2: Break-up of unique individuals wrt to elections won</caption>
 <thead>
  <tr>
   <th style="text-align:right;"> n_elections_won </th>
   <th style="text-align:right;"> n_individuals </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 2089 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1886 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 665 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 329 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 173 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 74 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 35 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 12 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

Density graph of the same:

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-4-1.png" width="768" />

Density graph graph of the number of elections won by **families**

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-5-1.png" width="768" />


This density graph represents the same



---


## Elections contested

This table shows the count of the unique individuals with regards to the number of elections they have **contested** .


<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
<caption>Table 3: Break-up of unique individuals wrt to elections contested</caption>
 <thead>
  <tr>
   <th style="text-align:right;"> n_elections_contested </th>
   <th style="text-align:right;"> n_individuals </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 2764 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 1061 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 558 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 333 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 255 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 127 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 78 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 54 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 30 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>


This is a density of graph of the number of elections contested by **families**


<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-7-1.png" width="768" />


---


## Life span

This section looks at the life span of families. Life span is calculated by computing the difference in entry year of the family with the. Life span is simply the longitudinal life of a family. This  is calculated by simply computing the difference in the entry year of a family with the year in which the last member has contested. The following graph is a density chart of the the life span of the unique families in the dataset.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-8-1.png" width="768" />

---


## Retention

This chart depicts the retention  of candidates after each election year.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/retention chart 2-1.png" width="768" />













# Land distribution

The dataset contains a variable named land which records the land owned by the candidate/family. The information is recorded in *bhigas*.

## Families

This boxplot shows the difference the land owned by family and  a non-family entity.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae_ge families land-1.png" width="768" />

---



### Political Experience

This boxplot shows the difference in the land ownership according to a candidate's political experience. Political experience is the sum of term duration of every election that they have won.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge political experience land-1.png" width="768" />

---


#  Educational institutions

The data set has variable which record the candidate's/ family's ownership of school/college/both. 


## Families

This barplot depicts the difference in the ownership of educational institutions among family and non-family entities.



<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge education family-1.png" width="768" />




## Political Experience


This depicts the ownership of the educational institutions with regards to political experience of the unique individuals.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge education pol experience-1.png" width="768" />

### caste

Depicts the ownership of educational institutions with regards to the caste of the unique candidate.


<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-9-1.png" width="768" />


---


# Industries

The  dataset records the information regarding the candidate's family's ownership  of industries in 12 different categories. For the ease if analysis we clubbed them to 5 categories.

Current category  Old category
----------------  --------------
Petrol Pump       Petrol Pump

Others

3

4

5





## Families




Ownership of industries among families and non-families


<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
<caption>Table 4: Industry ownership</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Politician's identity </th>
   <th style="text-align:right;"> Average number of  ownersip </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Family </td>
   <td style="text-align:right;"> 1.65 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Non-family </td>
   <td style="text-align:right;"> 0.67 </td>
  </tr>
</tbody>
</table>

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-12-1.png" width="768" />



### rent thick 

Ownership of rent thick and non-rent thick industires with regards to the family type.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Politician's identity </th>
   <th style="text-align:left;"> rent-type </th>
   <th style="text-align:right;"> Proportion </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Family </td>
   <td style="text-align:left;"> non-rent-thick </td>
   <td style="text-align:right;"> 0.39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Family </td>
   <td style="text-align:left;"> rent-thick </td>
   <td style="text-align:right;"> 0.61 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Non-family </td>
   <td style="text-align:left;"> non-rent-thick </td>
   <td style="text-align:right;"> 0.71 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Non-family </td>
   <td style="text-align:left;"> rent-thick </td>
   <td style="text-align:right;"> 0.29 </td>
  </tr>
</tbody>
</table>

Ownership of industries among families and non-families with regards to the industry category.



<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge industires families-1.png" width="768" />


## Political experience

Ownership of industries with regards to the candidate's political experience

<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge industries political experience-1.png" width="768" />



# Political experience


## Family

Political experience composition among families and non-families.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge families caste-1.png" width="768" />



This tables shows the distribution of the unique individuals' experience/

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Experience Categories </th>
   <th style="text-align:right;"> Count </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 0 </td>
   <td style="text-align:right;"> 2164 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 1-5 </td>
   <td style="text-align:right;"> 1562 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 6-15 </td>
   <td style="text-align:right;"> 932 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 16+ </td>
   <td style="text-align:right;"> 244 </td>
  </tr>
</tbody>
</table>

This table shows the distribution of the experience categories among the families and non-families.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Experience Categories </th>
   <th style="text-align:right;"> Non-Families </th>
   <th style="text-align:right;"> Families </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 0 </td>
   <td style="text-align:right;"> 2148 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 1-5 </td>
   <td style="text-align:right;"> 1520 </td>
   <td style="text-align:right;"> 42 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 6-15 </td>
   <td style="text-align:right;"> 811 </td>
   <td style="text-align:right;"> 121 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 16+ </td>
   <td style="text-align:right;"> 123 </td>
   <td style="text-align:right;"> 121 </td>
  </tr>
</tbody>
</table>



---


## caste

This shows the caste composition of the candidates with regards to their experience.




<img src="{{< blogdown/postref >}}index.en_files/figure-html/ae ge pol exp caste-1.png" width="768" />

