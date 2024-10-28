    enter into console:
    > devtools::install_github("Jacob-J-Richards/CUSUM_Package_2")
    > library(myfirstpackage2)
    > install.packages('spc')
    > library(spc)

    
    Provide your data sample as a column or row of a data frame, matrix, list, or just
    a simple numeric vector. So long as it's 1 dimensional it will coerce the data. 

    
    Provide the input arguments as such: CUSUM_Chart_2(data,k,L0,mu0,hs,sided,r) 
    the input arguments other than your provided data will be passed to 
    xcusum.crit(k, L0, mu0 = 0, hs = 0, sided = "one", r = 30) 
    for the calculation of control limits. 

    
    Given these inputs a cumulative sum chart will be produced and will terminate when 
    either your data set has been exausted and the null hypothesis remains un-rejected
    or will terminate as soon as the contol limit has been passed. 

    
    In eithercase a report on the null hypothesis and values of all
    variables will be printed upon completion of the simulation. 
    
    
