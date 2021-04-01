here is how nate helped me trace where the stuff from the document GET endpoint is used

searched for /document, found that in the document.service.ts where it is set up as the urlPath

in documentsForBorrower method in there you can see that it calls this.http.get on that url

searched for documentsForBorrower method in code base and found it in document.store.ts

somehow we got to document.state.ts, i think we looked at document.action.ts and saw there was class called SubscriberToBorrowerDocuments in there, searched for that and found it in the document.state.ts

searched for subscribertoborrowerdocuments, found it in the borrower-detail-tabs.component.ts






dWmwNu3G%zEdJ9vWfSl&5TWFbEyQzz6tz7p8C44$A^b5fjsSGalQeSjd5luWMBFh$ZElk1Kv
