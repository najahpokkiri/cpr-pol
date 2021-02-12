---
title: "Cabinet ministers - 1990:2014"
author: "Abdul Najah"
date: '2021-01-15'
params:
  orig_date: "Original Publish Date: 15 January, 2021"
  update_date: !r paste("Updated on:", format(Sys.time(), '%d %B, %Y'))
authors:
  - najah
summary: Analysis of the cabinet ministers data from TCPD
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

<script src="{{< blogdown/postref >}}index.en_files/htmlwidgets/htmlwidgets.js"></script>

<script src="{{< blogdown/postref >}}index.en_files/pymjs/pym.v1.js"></script>

<script src="{{< blogdown/postref >}}index.en_files/widgetframe-binding/widgetframe.js"></script>

<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>

<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />

<script src="{{< blogdown/postref >}}index.en_files/kePrint/kePrint.js"></script>

<link href="{{< blogdown/postref >}}index.en_files/lightable/lightable.css" rel="stylesheet" />

<script src="{{< blogdown/postref >}}index.en_files/htmlwidgets/htmlwidgets.js"></script>

<script src="{{< blogdown/postref >}}index.en_files/pymjs/pym.v1.js"></script>

<script src="{{< blogdown/postref >}}index.en_files/widgetframe-binding/widgetframe.js"></script>

### Document History

Original Publish Date: 15 January, 2021

Updated on: 13 February, 2021

-----

-----

# Data summary

This data set on cabinet minsters in India from the year 1990-2014 provides us information on their party, appointment duration, ministry, rank, gender, caste and reservations and dynast status. This data set has 1499 observations and 22 variables.

For more info on the data please refer to the codebook - [codebook](http://lokdhaba.ashoka.edu.in:3003/static/media/qh_codebook.712c9103.pdf)

**Main variables in the data**

    ##  [1] "year"              "ls_number"         "ac_id"            
    ##  [4] "name"              "party"             "gender"           
    ##  [7] "caste"             "portfolio"         "rank"             
    ## [10] "appointment_begin" "appointment_end"   "house"            
    ## [13] "constituency"      "pid"               "State"            
    ## [16] "start_source"      "end_source"        "comments"         
    ## [19] "type_begin"        "type_end"          "dyn"              
    ## [22] "comments.1"

-----

**Sample data**

<div id="htmlwidget-1" style="width:100%;height:432px;" class="widgetframe html-widget"></div>
<script type="application/json" data-for="htmlwidget-1">{"x":{"url":"index.en_files/figure-html//widgets/widget_unnamed-chunk-2.html","options":{"xdomain":"*","allowfullscreen":false,"lazyload":false}},"evals":[],"jsHooks":[]}</script>

-----

# Distribution

**All ministers**\*

The ministers are chosen from both Loksabha and Rajyasabha. This graphs shows us the distribution of the minsters with regards to the house across the years.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-3-1.png" width="768" />

**Dynasts**

This bar plot shows us the proportion of dynast minsters from both the houses for each cabinet.

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-4-1.png" width="768" />

-----

## States

The following maps tell us the proportion of the minsters from each state.

In order to find the proportion of the ministers from each state, we created a variable named `Minister to ac ratio` which is *the ratio of number of ministers from that state to the number of Parliamentary constituencies in that state*. States in grey colour are the states which never had minsters during the period of 1990-2014.

-----

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-7-1.png" width="768" />

-----

# Term & Duration

This table shows the number of minsters/number of terms,number of unique minsters, total term and average term per person/uniq person for both the dynast and non-dynast ministers.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">

<caption>

Table 1: Term duration of minsters wrt identity

</caption>

<thead>

<tr>

<th style="text-align:left;">

House

</th>

<th style="text-align:left;">

dynastast

</th>

<th style="text-align:right;">

N\_ministers

</th>

<th style="text-align:right;">

uniq\_ministers

</th>

<th style="text-align:right;">

Total term (months)

</th>

<th style="text-align:right;">

Average term per min

</th>

<th style="text-align:right;">

Average term per uniq\_min

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

Lok Sabha

</td>

<td style="text-align:left;">

Dynast

</td>

<td style="text-align:right;">

402

</td>

<td style="text-align:right;">

137

</td>

<td style="text-align:right;">

8309.06

</td>

<td style="text-align:right;">

20.67

</td>

<td style="text-align:right;">

60.65

</td>

</tr>

<tr>

<td style="text-align:left;">

Lok Sabha

</td>

<td style="text-align:left;">

Non-dynast

</td>

<td style="text-align:right;">

655

</td>

<td style="text-align:right;">

256

</td>

<td style="text-align:right;">

13474.96

</td>

<td style="text-align:right;">

20.57

</td>

<td style="text-align:right;">

52.64

</td>

</tr>

<tr>

<td style="text-align:left;">

Rajya Sabha

</td>

<td style="text-align:left;">

Dynast

</td>

<td style="text-align:right;">

119

</td>

<td style="text-align:right;">

36

</td>

<td style="text-align:right;">

1724.47

</td>

<td style="text-align:right;">

14.49

</td>

<td style="text-align:right;">

47.90

</td>

</tr>

<tr>

<td style="text-align:left;">

Rajya Sabha

</td>

<td style="text-align:left;">

Non-dynast

</td>

<td style="text-align:right;">

280

</td>

<td style="text-align:right;">

103

</td>

<td style="text-align:right;">

5625.56

</td>

<td style="text-align:right;">

20.09

</td>

<td style="text-align:right;">

54.62

</td>

</tr>

</tbody>

</table>

-----

# Rank

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">

<thead>

<tr>

<th style="text-align:left;">

rank

</th>

<th style="text-align:right;">

dynast\_percentage

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

CM

</td>

<td style="text-align:right;">

47.75

</td>

</tr>

<tr>

<td style="text-align:left;">

DM

</td>

<td style="text-align:right;">

26.67

</td>

</tr>

<tr>

<td style="text-align:left;">

MoS

</td>

<td style="text-align:right;">

23.58

</td>

</tr>

<tr>

<td style="text-align:left;">

MoS(IC)

</td>

<td style="text-align:right;">

26.52

</td>

</tr>

<tr>

<td style="text-align:left;">

PM

</td>

<td style="text-align:right;">

33.33

</td>

</tr>

</tbody>

</table>

-----

# Portfolio

**Top ministries**

<img src="{{< blogdown/postref >}}index.en_files/figure-html/unnamed-chunk-11-1.png" width="768" />

-----

We have around 118 ministries now, we can reduce it further with some cleaning. Do we need a further analysis based on the ministries? this will enable us to address question like *what kind of ministries do dynasts prefer* . If so, we we can go ahead with further cleaning.

Eg: we can club coal/mine/petroleum to one natural resources category

<div id="htmlwidget-2" style="width:100%;height:432px;" class="widgetframe html-widget"></div>
<script type="application/json" data-for="htmlwidget-2">{"x":{"url":"index.en_files/figure-html//widgets/widget_unnamed-chunk-12.html","options":{"xdomain":"*","allowfullscreen":false,"lazyload":false}},"evals":[],"jsHooks":[]}</script>
