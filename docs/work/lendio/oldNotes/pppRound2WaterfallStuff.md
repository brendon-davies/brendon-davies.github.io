create view pppDocuments in views schema

create view pppDeals in views schema

create view pppValues in views schema

compare data from pppDeals, pppDocuments and pppValues and use logic comparing the values from these 3 views to determine what lender the deals should be routed to

values used for troubleshooting or understanding where deals are routed to are cached in 
cachedPppDealsTemp
cachedPppDocumentsTemp
cachedPppValuesTemp
cachedPppBorrowerStatusesTemp


based off of  values in pppBorrowerStatuses view, borrowers are selected and PPPDealAutoStart job is kicked off for each borrower




PPPDealAutoStart job

validates conditions

starts/creates deal
starts/creates application


comes from funding bank goes to a funding bank


pencil in current lender
pencil in lack of requirements
run waterfall script to see performance

need to do a dry run to spit out meaningful metrics to be able to communicate to business
need to run the tinker script to create deals
hopefully won't need to but might need to run tinker script to dead out deals we just create



how many deals are we creating
avg loan amount
other metrics like that

we want to scare people, write meta analysis queries

round robin logic
account for not true round robin
assign weights (weight variable)

list of lenders
borrower number mod number of lenders = index of lender to shoot borrower to





pppborrowerstatuses view round 1 , round 2 columns

reviewd borrowers remove null, add in value, exclude later per lender

deal not iinactive that traces back to loan product category 17 =  first round


dealsPassed in pppDeals = jh 

jh and dealspassed is blank then exclude


check with dane about abotu isPPPLender value

change jackHenryLenders loanproductcategory into 17 and 18

move per borrower check for ppp doc validation into lendio validation

round1 app complete, match 

match generic reasons



need to turn on whitelistedproducts, blacklistedproducts and alreadytried products for round1 and then find the right loanproductids and fix it for round 2 as well (in main status view, lender specific validation) - done

duplicate the submit to lp lenders and change everything to round 2 for round 2
same thing for the meta analysis query - done


get with dane about borrower values being pulled in pppValues view as well as the lendio issues in main status view to see which ones we can get rid of - done

check with dane specifically about submitForPLP in main status view - done


check with devs if hasPPPApplicationSigned is valid for round 1 as well as round 2 - done


check with dane if a pass from jack henry in the first round applies to round 2 as well - done


---------------------------------------------------------------------------------------------------------------

need to ensure that the results of the waterfall distribution query matches the results of the submit to lenders php query exactly, need to be 100%

need to ensure weights are available - done


make sure document list is correct still - done

check with dane about documents in pppDocuments view - done




actually round1 app complete
borrower stage not inactive
not fraud
not test
not deleted
draw 1/2 deal already?
app signed doc
jack henry borrower
