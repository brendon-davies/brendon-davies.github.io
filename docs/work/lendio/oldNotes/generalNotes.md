In api php artisan schedule:ocrolus-check-status

run this in local dev environment to give yourself admin rights
INSERT INTO lenderUserRoles (lenderUserId, roleid, created)
SELECT u.id
	,  lur.roleId
	, NOW()
FROM users AS u
JOIN users AS ub ON 1=1
JOIN lenderUserRoles AS lur ON 1=1
	AND lur.lenderUserId = ub.id
WHERE 1=1
	AND u.email = 'brendon.davies@lendio.com' -- your email address
	AND ub.email = 'brian.hosie@lendio.com' -- the email address of the person you want to copy the rights of
;

dev
./get_wp_plugins.sh
robot-unicorn
npm ci
grunt

to get bp running on localhost:3001/bp/basic-info
scotty/vue
npm run dev


this will break foreign key relationships:
SET FOREIGN_KEY_CHECKS=0;
##NOTE: be sure to set this back to 1 when you are done with it


the `name` from `borrowers` is what you search for in in fullstory for the name


vagrant ssh -c 'cd /var/www/api; ./vendor/bin/phpunit tests/Unit/Referral/ReferralLeadTest.php'


if changes to phpstandards don't seem to be working, run one of the following:
	composer clearVendor in api
	composer update-standards in api
	
this is the command you run in phpstandards to get the tag

git describe --tags --abbrev=0

this is the command you need to run to be able to tinker in a remote server

export PATH=/usr/local/php/7.3.3/bin:$PATH

exclude: vendor,.tmp, dist,.git,bower_components,bundles,*.map,node_modules,*.csv,*.CSV,*.ufm,*.sql,*.afm,*.json,*.pdf,*.md,*.svg,*.c,*.txt,*.po,*.export,*.lock,*.example,*.min.js,H.php,*.ipynb,*.pot,*.conf,*.tcl,*gitk-git

fE^kWuQ6tnhR3G*B

angular cli command
npx ng <angular cli command>


if you get a cURL error: in api/lp in vagrant run php artisan config:clear






^4fxKq&2K3TzYi60NEAu
my ngrok url

https://brendon-davies.ngrok.io

https://brendon-davies.ngrok.io/api/sendgrid/inbound?token=34db9dc1b50832116ba71d35521494f04bf19b8d


if you have deal(s) that need to be visible in partner portal, you need to create an application for them
to do that, use these tinker commands

an array of dealIds
$da = [1759229,1759230];

loop over each deal id and start an application for them
foreach ( $da as $dealId ) { $deal = App\Models\Deal::find($dealId); $application = App\Models\Application::create(['dealId' => $deal->id, 'lenderId' => TENANT_INSTITUTION_ID, 'lenderUserId' => SYS_USER_ID, 'loanProductId' => $deal->loanProduct->id, 'contactLenderUserId' => $deal->loanProduct->contactLenderUserId,'inactive' => null,]); };




to seed a lender with deals that are eligible to bulk submit just run this command in vagrant


php artisan db:seed --class=PppTestSeeder


here is how you output to a file in php (for debugging or something of the like)

file_put_contents('/var/www/api/benchmarkData.txt', 'dealId: ' . $deal->id . "\n", FILE_APPEND | LOCK_EX);



partners have an  affiliates record
lenders have an institutions record

partners send us leads
lenders work the leads to offer loan products

an entity can be just a partner, just a lender, or both

run this command both inside and outside vagrant to fix stuff

php artisan route:cache 








model creation

__construct    New Model


newlenderuserpassword.php



























in env overrides set up SBA_URL = sandbox url
 loanProductLender institutions for the deal has to have has to have an sba toker






3 different breath attacks
cold dc 8 + con mod + prof bonus 15 foot cone

radiant breath wisdom saving throw and they take radiant damage and blinded and deafened until next turn if they fail 1d4 damage at each turn until they beat the wisdom save 4d6 for damage if i want to heal 4d4 increases for level

misty breath bring pacifying energy charisma save 15 foot cone if they fail they get turned a mist for 1d4 hours 

boss killer radiant damage or cold 4d10 
chance for disentrigation i must succeed a charisma saving throw when i succede the creature i hit must make charisma saving throw
if they fail they take force damage, if it takes the creature to zero they are disentigrated, works on creatues or objects
 

roll 1d6 and get 4-6 i can use it a second time

sword is now +2 to hit and damage

armor
full plate no disadvantage for dex checks
resistance to cold and radiant damage, no longer resistance to lightning

orb of mort given to ish goddes of death

orb of pourvoir given to morjon

orb of connisance given to ish's friend

these orbs created the ice catacombs
corpse of ish and morjon far northnern point of our world


eeyami is succedes partner
eluani is the sister that stayed with the pluzon

spellbook from hind
	expeticous retreat
	jump
	silent image
	darkness
	dark vision
	blindness/deafness
	enlarge/reduce
	levitate
	scorching ray
	clairvoyance
	dispel magic
	lightning bolt
	slow
	water breathing
	polymorph
	ice storm
	banishment
	hold monster
	dream
	
rod of absorption

hint to location of heavens brood
hiding near tinib by shercoast and redliff, further east

void unsigned envelopes