	1. merge branch to master
	2. push to github
	3. ssh fp1.staging.lendio.net
	4. sudo -i -u deploy
	5. cd /var/www/franchise_portal)
	6. run deploy.sh ./deploy.sh
repeat for fp2.staging.lendio.net

ssh fp1.staging.lendio.net

repeat

ssh fp2.staging.lendio.net

repeat


	1. make changes to your branch locally
	2. run this command to check for any blatant syntax errors: php -l #FILENAME#
	3. merge branch into master
	4. push to github
	5. run the following commands to deploy to staging
		a. ssh fp1.staging.lendio.net
		b. sudo -I -u deploy
		c. cd /var/www/franchise-portal
		d. ./deploy.sh
	6. test functionality on staging
deploy to production by repeating steps a-d from step 5 for fp1.staging.lendio.net and fp2.staging.lendio.net 