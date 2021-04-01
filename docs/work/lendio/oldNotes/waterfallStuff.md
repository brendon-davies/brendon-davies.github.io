data-warehouse/src/ppp-bi-pipeline is the repo/path

wvscw



2 creates views.pppDocuments which is a snapshot of documents in optimus right now

3 actual waterfall lives here
	concat statement on line 10 is order of lenders for waterfall
	if adding new lender on top of adding in validation blocks need to replicate functionality on line 146
	
	kabbage is the catch all, keep them at the bottom of the waterfall
	

3.5 is caching queries

	cachedPppValuesTemp and cachedPppBorrowerStatuses are run frequently (bottom 2 blocks)
	cachedPppBorrowerStatuses can tell you why files aren't getting sent (dq criteria)
	


run 3 first, 3.5 bottom 2 blocks (run all blocks in 3.5 once a week)

run first block in 4 once, then you need to massage the amounts by adjusting dates
take a screenshot and post it in submissionplan channel

5 comment out main block starting on line 11 and then line 35 re-create the dates from 4
also make sure list starting on line 48 matches list of lenders in waterfall 3 (kabbage is not there)
comment out line 76 for a dry run

use job3 to do a dry run of 5

if it fails it will throw out a message

if everything is ok then uncomment the job dispatch line and run it again 

for kabbage run separate query, export as csv, slack csv to ian gillette, paul and mike riding, once ian says he has sent the file to kabbage take all borrowerIds and create an array named $borrowers (already preset config in List Creation spreadsheet), in tinker on job3 create that array and then run this command as a dry run, if everything goes ok with the dry run then uncomment the line to dispatch the jobs and run it again


collect($borrowers)->each(function($borrowerId) {
    $borrower = Borrower::find($borrowerId);
    $loanProductId = 917;
    // $loanProductId = 922;
    $job = new App\Jobs\PPPDealAutoStart($borrower, $loanProductId);
    try {
      $job->validatePreconditions($borrower);
        // app(\Illuminate\Contracts\Bus\Dispatcher::class)->dispatch($job->onConnection('rabbitmq'));
      echo ".";
    } catch (Throwable $e) {
      echo "\nBorrower ".$borrower->id." is not eligible for auto submit! ".$e->getMessage();
    }
})->count();


if you get a CHANNEL_ERROR just exit out of tinker, cd up one dir, then cd back and go back in

go to views db cachedpppborrowerstatuses


Here's the distribution amounts as of 08/05/2020
DreamSpring - 300 
Fountainhead - 200
MBE - 800



firgure out why dead deals created >= 01-11 for reason other than sent to mp and footrpint did not prevent another deal from being created

active deal for any draw should prevent a deal from being created
  active deal is not soft deleted, 17 or 18, stage <> inactive and created >= 01-11-2021

deal deaded out for possible fraud borrower regardless of created date should dq for new deals







change pppDeals to only check for deals created on or after 1/11/21





















