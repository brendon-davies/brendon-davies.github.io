taking an inbound request from sendgrid and dumping out all of the keys:

Log::debug(json_encode(collect($request->all())->keys()));



to access mysql via command line, in terminal run this command:

mysql -u lendio -p

then when prompted, enter the password L3end10

to see if binary logging is turned on, run this command:

show variables like '%bin%'

if sql_log_bin is ON, binary logging is turned on


here's the list of files you should exclude from searches
vendor,.tmp, dist,.git,bower_components,bundles,*.map,node_modules,*.csv

here's a code example of how to do a hasManyThrough relationship

borrower has many deals
deals have many approvals
borrower has many approvals through many deals

return $this->hasManyThrough(
	static::$modelNamespace . 'Approval',
	static::$modelNamespace . 'Deal',
	'borrowerId', // Foreign key on deals table...
	'dealId', // Foreign key on approvals table...
	'id', // Local key on borrower table...
	'id' // Local key on deals table...
);

here's how you use Carbon to get a utc timestamp in the future (add the first Carbon to use in tinker)

Carbon\Carbon::now()->addMonths(2)->timestamp


here is an explanation on how the laravel map function works
deals is a collection of deals, map goes through each deal and if the stage is anything other than inactive or funded then it returns the deal, so basically it filters out the inactive deals out of the collection. the filter on the end removes any null spots in the collection as a result of removing a deal from the collection

$deals = $deals->map( function($deal) { 
if (!in_array($deal->stage,['inactive','funded'])) {
return $deal;
};
})->filter();




here the SO link to the answer about writing a query to show all the dates in a month:
https://stackoverflow.com/questions/30300664/mysql-how-to-show-all-days-records-in-particular-month/60536438#60536438

link to a medium article about how to password protect a netlify site
https://medium.com/@j0hnm4r5/password-protecting-a-website-with-the-free-tier-of-netlify-and-publishing-with-a-single-npm-e509af9f108f

link to staticrypt to encrypt main page for personal docs
https://robinmoisson.github.io/staticrypt/

