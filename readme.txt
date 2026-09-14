PLATE MAP NAMING CONVENTIONS (.csv) 

calibrator wells 
    should be named one of the following: "cal|calibrator|std|standard" 
    should be numbered 1-9 where 1 is neat, 2-8 are 4fold serial dilutions, and 9 is blank 
    example: cal1, cal2, cal3 ...

    if serial dilution is not 4, change "Dilution factor" to the appropriate integer
    if calibrator 1 is not neat, uncheck "cal 1 is neat"
    if calibrator 9 is not blank, uncheck "cal 9 is blank"

control wells
     should be named "cntrl"
     should be numbered 1-3
     example: cntrl1, cntrl2, cntr3
  
sample wells
    should be named as perturbagen, ie IL10
    should be labeled with dilution factor used, as follows: "_dil8" where 8 indicated a 1:8 dilution, ie IL10_dil8


GENERAL

user must upload txt and csv files in pairs by plate#

user must paste in spot names, else generic spot 1-10 will be used

tool will parse replicates by looking for the same name used multiple times within the same csv
    to ensure replicates are not averaged across multiple dilutions, be sure to append "_dil[x]" to the end of sample name
    calibrator dilutions are pre-loaded for 4fold dilution from neat ending in blank

tool will calculate fold change over matched BSA control
    sample and BSA control will be from same plate
    sample and BSA will be same dilution
    sample and BSA signal used to calculate fc will be for the same spot
