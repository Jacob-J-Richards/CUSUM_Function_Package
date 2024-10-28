    enter into console:
    
    devtools::install_github("Jacob-J-Richards/Cumulative_Sum_Chart_Implimentation_Package")
    library(myfirstpackage2)
    install.packages('spc')
    library(spc)

    
    Provide your data sample as a column or row of a data frame, matrix, list, or just
    a simple numeric vector. So long as it's 1 dimensional it will coerce the data. 

    
    Provide the input arguments as such: CUSUM_Chart_2(data,k,L0,mu0,hs,sided,r) 
    the input arguments other than your provided data will be passed to 
    xcusum.crit(k, L0, mu0 = 0, hs = 0, sided = "one", r = 30) 
    for the calculation of control limits. 

    Usage
    xcusum.crit(k, L0, mu0 = 0, hs = 0, sided = "one", r = 30)
    Arguments
    k     reference value of the CUSUM control chart.
    L0     in-control ARL.
    mu0     in-control mean.
    hs     so-called headstart (enables fast initial response).
    sided     distinguishes between one-, two-sided and Crosier’s modified two-sided CUSUM
    scheme by choosing "one", "two", and "Crosier", respectively.
    r     number of quadrature nodes, dimension of the resulting linear equation system
    is equal to r+1 (one-, two-sided) or 2r+1 (Crosier).

    
    Given these inputs a cumulative sum chart will be produced and will terminate when 
    either your data set has been exausted and the null hypothesis remains un-rejected
    or will terminate as soon as the contol limit has been breached and the null hypothesis 
    has been rejected. 

    H0: population mean of which inputted sample was spawned from is equal to mu0 
    inputted at function call
    

    
    In eithercase a report on the null hypothesis and values of all
    variables will be printed upon completion of the simulation. 
    
    
