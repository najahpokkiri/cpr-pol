---
title: "Schools and Colleges"
author: "Najah"
date: "07/04/2021"
params:
  orig_date: "Original Publish Date: 7th March, 2021"
  update_date: !r paste("Updated on:", format(Sys.time(), '%d %B, %Y'))
authors:
  - najah
summary: Analysis of schools and colleges data
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



### Document History

Original Publish Date: 7th March, 2021

Updated on: 09 April, 2021

---







# UP


The [All India Survey on Higher Education (AISHE)](http://aishe.nic.in/) website provided two kind of college data. 1, Colleges affiliated to Universities. 2, Stand alone institutions. 

There were *7690* affiliated colleges *1136* stand-alone colleges. Among these two categories, only *7718* observations had year of establishment. Once I filtered the list of colleges that provided the year of establishments to colleges that are established after 1974, the observations further came down to **7002**. This again reduced to **6825** after geocoding and chucking out the universities.






## Data summary{.tabset}



### Main variables


```
##  [1] "District"        "University.Type" "University.Name" "inst_type"      
##  [5] "college_name"    "college_type"    "Address"         "Website"        
##  [9] "Management"      "year_estd"       "Specialised.in"  "Location"       
## [13] "Upload.Year"     "full_name"       "full_adress"     "lat"            
## [17] "long"            "AC_NO"           "AC_NAME"         "PC_NO"          
## [21] "PC_NAME"         "Longitude"       "Latitude"        "ST_Name"
```

### types of management



```
## # A tibble: 5 x 2
##   Management         count
##   <chr>              <int>
## 1 Central Government    11
## 2 Local Body           344
## 3 Private Aided        314
## 4 Private Un-Aided    5801
## 5 State Government     429
```





### Year by year break-up of number of colleges

I kept *Private un-aided* as private and clubbed all others as government colleges.


<img src="edu_inst_files/figure-html/unnamed-chunk-5-1.png" width="768" />


----

After my initial inspections, I went to merge the college data with UP dynasties data after allotting the coleges to each election year based on the year of establishment






```
## # A tibble: 12 x 2
##    year_el count
##    <chr>   <int>
##  1 1974       55
##  2 1980       64
##  3 1985       43
##  4 1987       40
##  5 1989       40
##  6 1991       50
##  7 1993      167
##  8 1996      554
##  9 2002     1239
## 10 2007     2050
## 11 2012     2297
## 12 2017      300
```









---

Average number of colleges built every year in a constituency is 1.37


### Distribution of number of colleges established every election year in a constituency

<img src="edu_inst_files/figure-html/unnamed-chunk-8-1.png" width="768" />


---




### Distribution of number of colleges in a constituency{.tabset}

#### Post 2009

<img src="edu_inst_files/figure-html/unnamed-chunk-9-1.png" width="768" />

---

#### Pre 2009

<img src="edu_inst_files/figure-html/unnamed-chunk-10-1.png" width="768" />




### spatial distribution


## regressions{.tabset}


### dynast definitions



<img src="D:/cpr/misc/dyn_def.jpeg" width="640" />





### Dynast definition 2{.tabset}

#### All colleges





<table style="text-align:center"><caption><strong>Regression Results - UP colleges - Dynast 2</strong></caption>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td colspan="4"><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="4" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td colspan="3">n_colleges</td><td>n_college_bin</td></tr>
<tr><td style="text-align:left"></td><td><em>OLS</em></td><td><em>normal</em></td><td><em>glm: quasipoisson</em></td><td><em>probit</em></td></tr>
<tr><td style="text-align:left"></td><td><em></em></td><td><em></em></td><td><em>link = log</em></td><td><em></em></td></tr>
<tr><td style="text-align:left"></td><td>(1)</td><td>(2)</td><td>(3)</td><td>(4)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn_cum_2</td><td>-0.218</td><td>-0.219</td><td>-0.104<sup>*</sup></td><td>-0.147<sup>*</sup></td></tr>
<tr><td style="text-align:left"></td><td>(0.151)</td><td>(0.151)</td><td>(0.062)</td><td>(0.078)</td></tr>
<tr><td style="text-align:left">caste_uc</td><td>0.071</td><td>0.071</td><td>0.040</td><td>0.100</td></tr>
<tr><td style="text-align:left"></td><td>(0.147)</td><td>(0.147)</td><td>(0.093)</td><td>(0.087)</td></tr>
<tr><td style="text-align:left">caste_yadav</td><td>0.274</td><td>0.270</td><td>0.147</td><td>0.216<sup>*</sup></td></tr>
<tr><td style="text-align:left"></td><td>(0.195)</td><td>(0.195)</td><td>(0.108)</td><td>(0.112)</td></tr>
<tr><td style="text-align:left">caste_non_yadav_obc</td><td>-0.041</td><td>-0.040</td><td>-0.042</td><td>0.090</td></tr>
<tr><td style="text-align:left"></td><td>(0.170)</td><td>(0.170)</td><td>(0.101)</td><td>(0.098)</td></tr>
<tr><td style="text-align:left">caste_dalit</td><td>-0.255</td><td>-0.259</td><td>-0.210<sup>**</sup></td><td>0.081</td></tr>
<tr><td style="text-align:left"></td><td>(0.162)</td><td>(0.162)</td><td>(0.101)</td><td>(0.095)</td></tr>
<tr><td style="text-align:left">caste_muslim</td><td>-0.192</td><td>-0.192</td><td>-0.133</td><td>0.090</td></tr>
<tr><td style="text-align:left"></td><td>(0.182)</td><td>(0.182)</td><td>(0.106)</td><td>(0.107)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>4,825</td><td>4,825</td><td>4,825</td><td>4,825</td></tr>
<tr><td style="text-align:left">R<sup>2</sup></td><td>0.313</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.311</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Akaike Inf. Crit.</td><td></td><td>23,761.650</td><td></td><td>3,915.605</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td colspan="4" style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>




#### Private colleges






<table style="text-align:center"><caption><strong>Regression Results - UP private colleges - Dynast 2</strong></caption>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td colspan="4"><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="4" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td colspan="3">n_private</td><td>n_college_bin</td></tr>
<tr><td style="text-align:left"></td><td><em>OLS</em></td><td><em>normal</em></td><td><em>glm: quasipoisson</em></td><td><em>probit</em></td></tr>
<tr><td style="text-align:left"></td><td><em></em></td><td><em></em></td><td><em>link = log</em></td><td><em></em></td></tr>
<tr><td style="text-align:left"></td><td>(1)</td><td>(2)</td><td>(3)</td><td>(4)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn_cum_2</td><td>-0.182</td><td>-0.182</td><td>-0.102</td><td>-0.110</td></tr>
<tr><td style="text-align:left"></td><td>(0.136)</td><td>(0.136)</td><td>(0.064)</td><td>(0.080)</td></tr>
<tr><td style="text-align:left">caste_uc</td><td>0.032</td><td>0.032</td><td>0.004</td><td>0.001</td></tr>
<tr><td style="text-align:left"></td><td>(0.132)</td><td>(0.132)</td><td>(0.098)</td><td>(0.101)</td></tr>
<tr><td style="text-align:left">caste_yadav</td><td>0.214</td><td>0.214</td><td>0.118</td><td>0.092</td></tr>
<tr><td style="text-align:left"></td><td>(0.175)</td><td>(0.175)</td><td>(0.113)</td><td>(0.125)</td></tr>
<tr><td style="text-align:left">caste_non_yadav_obc</td><td>-0.038</td><td>-0.038</td><td>-0.058</td><td>0.036</td></tr>
<tr><td style="text-align:left"></td><td>(0.153)</td><td>(0.153)</td><td>(0.106)</td><td>(0.111)</td></tr>
<tr><td style="text-align:left">caste_dalit</td><td>-0.247<sup>*</sup></td><td>-0.247<sup>*</sup></td><td>-0.249<sup>**</sup></td><td>-0.052</td></tr>
<tr><td style="text-align:left"></td><td>(0.145)</td><td>(0.145)</td><td>(0.106)</td><td>(0.109)</td></tr>
<tr><td style="text-align:left">caste_muslim</td><td>-0.184</td><td>-0.184</td><td>-0.162</td><td>-0.029</td></tr>
<tr><td style="text-align:left"></td><td>(0.164)</td><td>(0.164)</td><td>(0.112)</td><td>(0.122)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>4,825</td><td>4,825</td><td>4,825</td><td>4,825</td></tr>
<tr><td style="text-align:left">R<sup>2</sup></td><td>0.309</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.307</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Akaike Inf. Crit.</td><td></td><td>22,713.360</td><td></td><td>3,174.829</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td colspan="4" style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>


### Dyn defnition 3{.tabset}

#### All college






<table style="text-align:center"><caption><strong>Regression Results - UP all colleges - Dynast 3</strong></caption>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td colspan="4"><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="4" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td colspan="3">n_colleges</td><td>n_college_bin</td></tr>
<tr><td style="text-align:left"></td><td><em>OLS</em></td><td><em>normal</em></td><td><em>glm: quasipoisson</em></td><td><em>probit</em></td></tr>
<tr><td style="text-align:left"></td><td><em></em></td><td><em></em></td><td><em>link = log</em></td><td><em></em></td></tr>
<tr><td style="text-align:left"></td><td>(1)</td><td>(2)</td><td>(3)</td><td>(4)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn_cum_3</td><td>-0.274<sup>*</sup></td><td>-0.274<sup>*</sup></td><td>-0.126<sup>**</sup></td><td>-0.061</td></tr>
<tr><td style="text-align:left"></td><td>(0.144)</td><td>(0.144)</td><td>(0.058)</td><td>(0.074)</td></tr>
<tr><td style="text-align:left">caste_uc</td><td>0.075</td><td>0.075</td><td>0.046</td><td>0.095</td></tr>
<tr><td style="text-align:left"></td><td>(0.147)</td><td>(0.147)</td><td>(0.093)</td><td>(0.087)</td></tr>
<tr><td style="text-align:left">caste_yadav</td><td>0.275</td><td>0.275</td><td>0.153</td><td>0.206<sup>*</sup></td></tr>
<tr><td style="text-align:left"></td><td>(0.195)</td><td>(0.195)</td><td>(0.108)</td><td>(0.112)</td></tr>
<tr><td style="text-align:left">caste_non_yadav_obc</td><td>-0.042</td><td>-0.042</td><td>-0.042</td><td>0.085</td></tr>
<tr><td style="text-align:left"></td><td>(0.170)</td><td>(0.170)</td><td>(0.101)</td><td>(0.098)</td></tr>
<tr><td style="text-align:left">caste_dalit</td><td>-0.253</td><td>-0.253</td><td>-0.205<sup>**</sup></td><td>0.081</td></tr>
<tr><td style="text-align:left"></td><td>(0.162)</td><td>(0.162)</td><td>(0.101)</td><td>(0.095)</td></tr>
<tr><td style="text-align:left">caste_muslim</td><td>-0.186</td><td>-0.186</td><td>-0.130</td><td>0.077</td></tr>
<tr><td style="text-align:left"></td><td>(0.182)</td><td>(0.182)</td><td>(0.106)</td><td>(0.107)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>4,825</td><td>4,825</td><td>4,825</td><td>4,825</td></tr>
<tr><td style="text-align:left">R<sup>2</sup></td><td>0.313</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.311</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Akaike Inf. Crit.</td><td></td><td>23,760.110</td><td></td><td>3,918.516</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td colspan="4" style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>



#### Private colleges






<table style="text-align:center"><caption><strong>Regression Results - UP private colleges - Dynast 3</strong></caption>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td colspan="4"><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="4" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td colspan="3">n_private</td><td>n_college_bin</td></tr>
<tr><td style="text-align:left"></td><td><em>OLS</em></td><td><em>normal</em></td><td><em>glm: quasipoisson</em></td><td><em>probit</em></td></tr>
<tr><td style="text-align:left"></td><td><em></em></td><td><em></em></td><td><em>link = log</em></td><td><em></em></td></tr>
<tr><td style="text-align:left"></td><td>(1)</td><td>(2)</td><td>(3)</td><td>(4)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">caste_uc</td><td>0.036</td><td>0.036</td><td>0.011</td><td>0.001</td></tr>
<tr><td style="text-align:left"></td><td>(0.132)</td><td>(0.132)</td><td>(0.098)</td><td>(0.101)</td></tr>
<tr><td style="text-align:left">caste_yadav</td><td>0.219</td><td>0.219</td><td>0.125</td><td>0.090</td></tr>
<tr><td style="text-align:left"></td><td>(0.175)</td><td>(0.175)</td><td>(0.113)</td><td>(0.125)</td></tr>
<tr><td style="text-align:left">caste_non_yadav_obc</td><td>-0.039</td><td>-0.039</td><td>-0.059</td><td>0.034</td></tr>
<tr><td style="text-align:left"></td><td>(0.153)</td><td>(0.153)</td><td>(0.106)</td><td>(0.111)</td></tr>
<tr><td style="text-align:left">caste_dalit</td><td>-0.242<sup>*</sup></td><td>-0.242<sup>*</sup></td><td>-0.244<sup>**</sup></td><td>-0.050</td></tr>
<tr><td style="text-align:left"></td><td>(0.145)</td><td>(0.145)</td><td>(0.106)</td><td>(0.109)</td></tr>
<tr><td style="text-align:left">caste_muslim</td><td>-0.177</td><td>-0.177</td><td>-0.158</td><td>-0.033</td></tr>
<tr><td style="text-align:left"></td><td>(0.163)</td><td>(0.163)</td><td>(0.112)</td><td>(0.122)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>4,825</td><td>4,825</td><td>4,825</td><td>4,825</td></tr>
<tr><td style="text-align:left">R<sup>2</sup></td><td>0.309</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.307</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Akaike Inf. Crit.</td><td></td><td>22,711.610</td><td></td><td>3,175.206</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td colspan="4" style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>


### adr variables

Inorder to use the adr variables in the model, I have to limit the years to post 2009.






<table style="text-align:center"><caption><strong>Regression Results - UP colleges: adr variables - Dynast 2</strong></caption>
<tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="1" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td>n_colleges</td></tr>
<tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn_cum_2</td><td>-0.021</td></tr>
<tr><td style="text-align:left"></td><td>(0.087)</td></tr>
<tr><td style="text-align:left">caste_uc</td><td>-0.044</td></tr>
<tr><td style="text-align:left"></td><td>(0.148)</td></tr>
<tr><td style="text-align:left">caste_yadav</td><td>0.068</td></tr>
<tr><td style="text-align:left"></td><td>(0.170)</td></tr>
<tr><td style="text-align:left">caste_non_yadav_obc</td><td>-0.194</td></tr>
<tr><td style="text-align:left"></td><td>(0.162)</td></tr>
<tr><td style="text-align:left">caste_dalit</td><td>-0.250</td></tr>
<tr><td style="text-align:left"></td><td>(0.160)</td></tr>
<tr><td style="text-align:left">caste_muslim</td><td>-0.233</td></tr>
<tr><td style="text-align:left"></td><td>(0.166)</td></tr>
<tr><td style="text-align:left">ed</td><td>-0.015</td></tr>
<tr><td style="text-align:left"></td><td>(0.013)</td></tr>
<tr><td style="text-align:left">assets</td><td>0.000</td></tr>
<tr><td style="text-align:left"></td><td>(0.000)</td></tr>
<tr><td style="text-align:left">num_crim</td><td>0.002</td></tr>
<tr><td style="text-align:left"></td><td>(0.005)</td></tr>
<tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>1,182</td></tr>
<tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>


# India




There were **45022** affiliated colleges **11987** stand-alone colleges. Among these two categories, only **52232** observations had year of establishment. This further reduced  to  **49959**  observations after geocoding .







## Data summary{.tabset}

###Year by year break-up of number of colleges


<img src="edu_inst_files/figure-html/unnamed-chunk-23-1.png" width="768" />



---




### state break-up


<img src="edu_inst_files/figure-html/unnamed-chunk-24-1.png" width="768" />




----


We are focusing on data post 2009 since we only have pan-India dynasty data after 2009. Thus in our college data set before mergin with dynasty has **19148 ** observations.








### State wise break-up post 2009



<img src="edu_inst_files/figure-html/unnamed-chunk-26-1.png" width="768" />











---

Average number of colleges built  in a constituency  in India during last 10 years is 1.67



### Distribution of number of colleges established every election year in a constituency

<img src="edu_inst_files/figure-html/unnamed-chunk-28-1.png" width="768" />

### Distributions of the number colleges established in the constituencies during 2009&2014

<img src="edu_inst_files/figure-html/unnamed-chunk-29-1.png" width="768" />

## regressions {.tabset}


### All colleges





<table style="text-align:center"><caption><strong>Regression Results - India all colleges</strong></caption>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td colspan="4"><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="4" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td colspan="3">n_colleges</td><td>n_college_binary</td></tr>
<tr><td style="text-align:left"></td><td><em>OLS</em></td><td><em>normal</em></td><td><em>glm: quasipoisson</em></td><td><em>probit</em></td></tr>
<tr><td style="text-align:left"></td><td><em></em></td><td><em></em></td><td><em>link = log</em></td><td><em></em></td></tr>
<tr><td style="text-align:left"></td><td>(1)</td><td>(2)</td><td>(3)</td><td>(4)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn</td><td>-0.277<sup>**</sup></td><td>-0.277<sup>**</sup></td><td>-0.154<sup>***</sup></td><td>-0.070</td></tr>
<tr><td style="text-align:left"></td><td>(0.117)</td><td>(0.117)</td><td>(0.045)</td><td>(0.072)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">State fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>4,631</td><td>4,631</td><td>4,631</td><td>4,631</td></tr>
<tr><td style="text-align:left">R<sup>2</sup></td><td>0.288</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.282</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Akaike Inf. Crit.</td><td></td><td>23,555.670</td><td></td><td>3,188.970</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td colspan="4" style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>


### Private colleges










<table style="text-align:center"><caption><strong>Regression Results - India private colleges</strong></caption>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td colspan="4"><em>Dependent variable:</em></td></tr>
<tr><td></td><td colspan="4" style="border-bottom: 1px solid black"></td></tr>
<tr><td style="text-align:left"></td><td colspan="3">n_private</td><td>n_college_binary</td></tr>
<tr><td style="text-align:left"></td><td><em>OLS</em></td><td><em>normal</em></td><td><em>glm: quasipoisson</em></td><td><em>probit</em></td></tr>
<tr><td style="text-align:left"></td><td><em></em></td><td><em></em></td><td><em>link = log</em></td><td><em></em></td></tr>
<tr><td style="text-align:left"></td><td>(1)</td><td>(2)</td><td>(3)</td><td>(4)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn</td><td>-0.248<sup>**</sup></td><td>-0.248<sup>**</sup></td><td>-0.177<sup>***</sup></td><td>-0.053</td></tr>
<tr><td style="text-align:left"></td><td>(0.098)</td><td>(0.098)</td><td>(0.047)</td><td>(0.071)</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">State fixed effects</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td style="text-align:left">Observations</td><td>4,631</td><td>4,631</td><td>4,631</td><td>4,631</td></tr>
<tr><td style="text-align:left">R<sup>2</sup></td><td>0.281</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.275</td><td></td><td></td><td></td></tr>
<tr><td style="text-align:left">Akaike Inf. Crit.</td><td></td><td>21,838.520</td><td></td><td>3,194.619</td></tr>
<tr><td colspan="5" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td colspan="4" style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
</table>

---

### with adr


```
## 
## <table style="text-align:center"><caption><strong>Regression Results - India all colleges with adr</strong></caption>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td><em>Dependent variable:</em></td></tr>
## <tr><td></td><td colspan="1" style="border-bottom: 1px solid black"></td></tr>
## <tr><td style="text-align:left"></td><td>n_colleges</td></tr>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">dyn</td><td>-0.252<sup>**</sup></td></tr>
## <tr><td style="text-align:left"></td><td>(0.126)</td></tr>
## <tr><td style="text-align:left">ed</td><td>-0.009</td></tr>
## <tr><td style="text-align:left"></td><td>(0.017)</td></tr>
## <tr><td style="text-align:left">assets</td><td>-0.000</td></tr>
## <tr><td style="text-align:left"></td><td>(0.000)</td></tr>
## <tr><td style="text-align:left">num_crim</td><td>0.022</td></tr>
## <tr><td style="text-align:left"></td><td>(0.019)</td></tr>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Year fixed effects</td><td>Yes</td></tr>
## <tr><td style="text-align:left">State fixed effects</td><td>Yes</td></tr>
## <tr><td style="text-align:left">Observations</td><td>620</td></tr>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td style="text-align:right"><sup>*</sup>p<0.1; <sup>**</sup>p<0.05; <sup>***</sup>p<0.01</td></tr>
## </table>
```
