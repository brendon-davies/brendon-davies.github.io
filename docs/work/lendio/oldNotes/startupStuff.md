Processes to start when re-booting computer
	1. Start vagrant :
		a. In any directory run this command: vup
	2. Start gatling:
		a. in any directory run this command: gat
	3. start local pipeline:
		a. in any directory run this command: ngrs
	4. start local personal dev:
		a. in any directory run this command: ltup
	5. start ngrok:
		a. in any directory run this command: sngrok
	6. run rabbit:
		a. vup
		b. rabbit
	7. start laravel log:
		a. in any directory run this command: larvl
		
bp on localhost:3001 cd scotty/vue npm run dev
		

to start docs locally navigate to the directory where the `docs` folder is at and run this command
docsify serve docs



bp (local.lendio.com/bp/basic-info) scotty/vue npm run build



robot unicorn npm run watch


when making a change to phpstandards and you need to run something in api, in order to have api run against the changes in phpstandards you have to run this command in api: composer update-standards




ng (pipeline) npm run start

changing php standards major things like framework changes and things like that
    - in api and lender-portal delete vendor folder
       rm -rf vendor
       composer install -o -vvv && composer dumpautoload

changing php standards for minor things like bug fixes or other development
    - in api and lender-portal delete lendiodevs folder
      rm -rf vendor/lendiodevs
     composer install -o -vvv && composer dumpautoload




		
to run cypress locally:
cd dev
cd cypress-e2e
npm run dev


		
in dev run nvm use 10.12

pm2 start gatling.json

pm2 log gatling

in vagrant

sudo service nginx run start

to make it so any robot-unicorn pages don’t have to have the cache refreshed locally go into the wp-config.php and change define('WP_CACHE', true); to false


to run chef locally outside of vagrant you have to run the following commands:

sudo su
PATH=/bin:/usr/bin:/usr/local/bin
chef-client
just type `exit` to get out of su


phpstandards deploy
on new branch in php standards run ./bump-version.sh in phpstandards

create new branches in api and lender-portal
update composer.json in api to have new phpstandards version
do the same for the composer.json file in lender-portal composer.json

run composer update-standards in both api and lender-portal repos to update the composer.lock 

push the branches out to github


edgepark 800-321-0591
byram 877-902-9726

echo $b->borrowerValues()->where('attributeId', 72)

the below commands clears the cache, changes borrower values and then shows the cache of data to be sent to hubspot. as long as the values returned from getting the hubspot cache match the internal names of the properties in hubspot then the value will be sent to hubspot and should be successfully received by hubspot. the values are defined in the HubspotContacts.php file. if a value doesn’t have a tablename before it in this file then that's how it should be sent to hubspot: IE annualrevenue. if a value has a tablename before it, the value should be sent to hubspot exactly like that: IE borrowerValues.creditScore. when checking the internal name of the property on hubspot, if there was no tablename before the value then that's what the internal name should be in hubspot, IE: annualrevenue should show as annualrevenue in hubspot for the internal name. if the value has a table name before it then in hubspot the internal name is all lowercase, and beginning with the period (.) in the name it will be snake case, IE: borrowerValues.creditScore should show in hubspot as borrowervalues_credit_score for the internal name. the logic for sending the values to hubspot is contained within the getAnalytics function within BorrowerValue.php in phpstandards/src/models 
Cache::clear()

Cache::get('hubspotBatch')

$b = Borrower::find(2876115)

BorrowerAttribute::saveBorrowerValues(
            [
            	[
                	'id' => 72,
                	'value' => 50066
            	],
	    
	   [
	                	'id' => 66,
	                	'value' => 605
	            	],
            	[
                	'id' => 4,
                	'value' => 24
            	]
            ],
            $b->id,
            SYS_USER_ID,
            [],
            $b
        )



BorrowerAttribute::saveBorrowerValues(
            [
            	[
                	'id' => 72,
                	'value' => 50065
            	]            ],
            $b->id,
            SYS_USER_ID,
            [],
            $b
        )






BorrowerAttribute::saveBorrowerValues(
            [[
                'id' => 4,
                'value' => 1
            ]],
            $b->id,
            SYS_USER_ID,
            [],
            $b
        )


BorrowerAttribute::saveBorrowerValues(
			[[
				'id' => 72,
				'value' => 50019
			]],
			$b->id,
			SYS_USER_ID,
			[],
			$b
		)



;


lender portal locally
url: local-lp.lendio.com
username: lpguy@lendio.com
password: lendio
