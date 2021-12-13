# PD progression
Models describing the progression of PD symptoms along time since onset and aging

Each file is a list containing the necessary information to recreate the models for each outcome in R. For example, `hy.RData` contains the list `hy_res` where the first element are the names of the outcome variables, second element contains the two associated spline basis functions, and the third element the model estimates. E.g.


  > hy_res[[1]][[2]]
  
  [1] "dyskinesia"
  
  > class(hy_res[[2]][[2]][[1]])
  
  [1] "ns"     "basis"  "matrix"
  
  > hy_res[[3]][[2]]
 
      effect   group    term                          estimate std.error statistic    df      p.value
     <chr>    <chr>    <chr>                            <dbl>     <dbl>     <dbl> <dbl>        <dbl>
    1  fixed    NA       (Intercept)                    -0.192      0.102    -1.88  1128.  0.0604     
    2  fixed    NA       age1                            0.209      0.197     1.06  1175.  0.288      
    3  fixed    NA       year_onset1                     1.75       0.332     5.29  1083.  0.000000152
    4  fixed    NA       year_onset2                    -0.287      0.781    -0.368  752.  0.713      
    5  fixed    NA       age1:year_onset1               -1.15       0.634    -1.81  1137.  0.0710     
    6  fixed    NA       age1:year_onset2                1.44       1.46      0.988  724.  0.324      
    7  ran_pars lopnr    sd__(Intercept)                 0.235     NA        NA       NA  NA          
    8  ran_pars lopnr    cor__(Intercept).Year_bl        0.340     NA        NA       NA  NA          
    9  ran_pars lopnr    cor__(Intercept).I(Year_bl^2)  -0.646     NA        NA       NA  NA          
    10 ran_pars lopnr    sd__Year_bl                     0.104     NA        NA       NA  NA          
    11 ran_pars lopnr    cor__Year_bl.I(Year_bl^2)      -0.728     NA        NA       NA  NA          
    12 ran_pars lopnr    sd__I(Year_bl^2)                0.0169    NA        NA       NA  NA          
    13 ran_pars Residual sd__Observation                 0.269     NA        NA       NA  NA    
