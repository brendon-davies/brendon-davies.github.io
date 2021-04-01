	1. Open sourcetree and navigate to repository changes need to be made in.
	2. Update repository by pulling newest version from github
	3. Create branch off of master branch in repository
	4. Check out new branch if you didn't do that automatically
	5. Make coding changes
	6. After coding changes have been made and tested, commit changes to working branch.
	7. Merge working branch into master do not do STRIKETHOUGH
	8. Push working branch out to remote repository
	9. Go to github
	10. Locate working branch that was pushed and create new pull request
	11. Fill out template for pull request details, use trello ticket when possible
	12. Paste trello url in "Supporting Info" part of pull request template
	13. Create pull request 
	14. Attach pull request to trello ticket
	15. Move card in trello to "In review" channel
	16. Go to pull requests slack channel and post brief description and url to pull request in github
	17. 
	18. 
	19. When pull request is approved, in github merge pull request and confirm merge
	20. Delete branch


	1. Back in sourcetree, pull production STRIKETHOUGH
	2. Merge master into production in sourcetree STRIKETHOUGH
		a. Got to production STRIKETHOUGH
		b. Right click on master STRIKETHOUGH
		c. Merge master into production STRIKETHOUGH
	3. Push production to origin STRIKETHOUGH

	1. in github create pull request to merge master into production
	2. merge master into production

	1. post "@here deploying #BRANCH#" in developers channel
	2. Go to lendio cloud controller
	3. Do 2 authentication
	4. Click on production
	5. Click on play button to the right of changed repository
	6. Add comment
	7. Job will start running, progress will be at the bottom of the screen
	8. Post in changeset slack channel
	
	
	#### PULL MASTER AND MERGE IT INTO YOUR FEATURE BRANCH LOCALLY EVERY DAY, AND E S P E C I A L L Y BEFORE YOU PUSH YOUR BRANCH OUT AND MERGE IT ON GITHUB!!! ###
	
	
	 MAKING CHANGES TO PHPSTANDARDS
	
	branch api/lp/phpstandards
	in composer.json files point api/lp to dev phpstandards (dev-#feature branch name#)
	create api/lp/phpstandards prs
	code changes 
	push out to github
	get approval in all 3
	
	!!! YOU ARE NOW DEPLOYING !!!
	
	merge feature branch into master in github phpstandards
	pull master in. phpstandards
	bump version locally, the new phpstandards version will be pushed out to github automatically
	immediately update composer.json from dev-#feature branch name# to the new phpstandards version locally in api/lp and run composer update-standards in both
	commit and push to github
	tests will run again
	when tests are finished merge feature branches into master
	merge master into production
	deploy production
	 
