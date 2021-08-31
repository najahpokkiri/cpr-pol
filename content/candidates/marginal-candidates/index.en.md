---
title: "Marginal candidate analysis"
author: ''
date: '2020-09-24'
draft: true
params:
  orig_date: 'Original Publish Date: 24 September, 2020'
  update_date: !r paste("Updated on:", format(Sys.time(), '%d %B, %Y'))
authors:
  - najah
summary: "                          "
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


---

### Document History

Original Publish Date: 24 September, 2020

Updated on: 15 February, 2021

---



<!-- ```{r reading the data} -->

<!-- ge_all <- fread("D:/cpr/UP/up-dynasties/dyn_other_data/GE_all.csv") -->

<!-- names(ge_all) <- tolower(names(ge_all)) -->

<!-- ge_all <- ge_all %>% filter(poll_no ==0 , party != "NOTA", vote_share_percentage >0) -->



<!-- #names(ge_all) -->
<!-- # -->
<!-- # dim(ge_all) -->

<!-- ge_mc <- ge_all %>% filter(vote_share_percentage<5) -->

<!-- ge_mc <- ge_mc %>% mutate(ind= case_when(party == "IND" ~ 1, -->
<!--                                    TRUE ~0)) -->


<!-- ``` -->

<!-- ```{r} -->
<!-- ge_all %>%  group_by(year) %>% summarise(count = n()) %>% filter(count>1000) %>% -->
<!--   ggplot(aes(factor(year), count, group = 1))+ -->
<!--   geom_point()+ -->
<!--   geom_line()+ -->
<!--   geom_smooth() -->
<!-- ``` -->


<!-- ```{r} -->
<!-- #ge_all %>%  group_by(year) %>% summarise(count = n()) %>% ungroup() %>% summarise(mean(count)) -->

<!-- g#e_all %>%  group_by(year) %>% summarise(count = n()) %>% filter(year>1999)%>% ungroup() %>% summarise(mean(count)) -->

<!-- ## proportion of candidates who wins -->

<!-- ge_all %>%  group_by(year) %>% mutate(win_count =n_distinct(candidate[position==1]),count_cand = n(), prop_win = win_count/count_cand) %>% distinct(year, prop_win) %>% -->
<!--   ggplot(aes(factor(year), prop_win, group=1))+ -->
<!--   geom_point()+ -->
<!--   geom_smooth() -->

<!-- #ge_all %>%  group_by(year) %>% mutate(win_count =n_distinct(candidate[position==1]),count_cand = n(), prop_win = win_count/count_cand) %>% distinct(year, prop_win) %>%filter(year>1999) %>% ungroup() %>%  summarise(mean(prop_win)) -->

<!-- ``` -->
<!-- Historically only 12% percent of the candidates makes it to the parliament. If we look at the election post 2000, it is as low as 7. -->

<!-- On an average we have more than 5000 candidates contesting in Loksabha elections. It is close to 8000 in elections post 2000 -->

<!-- among office eligible persons only less than 01% of the them contests for elections. Among them more than 65% do not even recieve 5% of vote share. After 2000, it is closer to 80%. ANd 1 out of 10 makes it to parliament finally. -->


<!-- # Marginal candidates -->

<!-- ```{r} -->

<!-- ge_win <- ge_all %>% filter(position ==1) -->

<!-- ge_mc %>% group_by(year,state_name, constituency_no) %>% mutate(count_mc = n(), count_ind = sum(ind)) %>% distinct(year,state_name, constituency_no, .keep_all =TRUE) %>% group_by(year) %>% summarise(mc_tot = sum(count_mc), cand_tot = sum(n_cand),ind_tot = sum(count_ind), mc_prop =mc_tot/cand_tot , ind_prop = ind_tot/cand_tot, mp_prop = mc_prop-ind_prop) %>% select(year, mc_prop, ind_prop, mp_prop) %>% pivot_longer(2:4) %>% -->
<!--   ggplot(aes(factor(year), value, group =name, color = name))+ -->
<!--   geom_point()+ -->
<!--   #geom_line()+ -->
<!--   geom_smooth()+ -->
<!--   theme_minimal() -->


<!-- ge_mc %>% group_by(year,state_name, constituency_no) %>% mutate(count_mc = n()) %>% distinct(year,state_name, constituency_no, .keep_all =TRUE) %>% group_by(year) %>% summarise(mc_tot = sum(count_mc), cand_tot = sum(n_cand), mc_prop =mc_tot/cand_tot ) %>% summarise(mean(mc_prop)) -->

<!-- ge_mc %>% group_by(year,state_name, constituency_no) %>% mutate(count_mc = n()) %>% distinct(year,state_name, constituency_no, .keep_all =TRUE) %>% group_by(year) %>% summarise(mc_tot = sum(count_mc), cand_tot = sum(n_cand), mc_prop =mc_tot/cand_tot ) %>%filter(year>1999) %>%  summarise(mean(mc_prop)) -->

<!-- ge_mc %>% -->
<!--   group_by(year)%>% -->
<!--   summarise(count = n())%>% -->
<!--   group_by(Year) %>% -->
<!--   mutate(sum = sum(count), prop = count/sum) %>% -->
<!--   select(Year, ind, count, prop) %>% -->
<!--   pivot_wider(names_from = ind, values_from = 3:4) %>% -->
<!--   #kable(digits =2) %>% -->
<!--   #kable_styling(bootstrap_options = "striped") -->

<!-- ge_mc %>%  group_by(year) %>% summarise(count = n()) %>% filter(count>1000) %>% -->
<!--   ggplot(aes(factor(year), count, group = 1))+ -->
<!--   geom_point()+ -->
<!--   geom_line()+ -->
<!--   geom_smooth() -->

<!-- ``` -->

<!-- ### Positon 1-3 average vote shares across years -->

<!-- ```{r} -->


<!-- g -->
<!-- ge_all %>% filter(position %in% c(1,2,3)) %>% group_by(year,position) %>% summarise(mean_vote_share = mean(vote_share_percentage)) %>% -->
<!--   ggplot(aes(factor(year), mean_vote_share, group = position, color = factor(position))) + -->
<!--   geom_point()+ -->
<!--   #geom_line()+ -->
<!--   geom_smooth()+ -->
<!--   theme_minimal() -->
<!-- ``` -->




