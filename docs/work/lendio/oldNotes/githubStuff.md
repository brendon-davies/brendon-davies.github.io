today I had trouble pushing a branch to github. I was able to push to all repos except 2 specific ones. come to find out what happened was those repos configs locally changed to be using https instead of ssh. all I did to fix it was to open the repo settings in sourcetree (go into the repo and click on the gear icon in the top right hand corner of the screen) and modify the settings for remotes to match the settings in a repo I was able to push to. problem solved

if you are trying to push a local branch to github that does not exist on github yet and you are having problems (like with the ng repo) use this command to push the branch out:

	git push -u origin fix-teams-admin-page-is-not-saving-changes
	
	
	here is the command you can run in phpstandardds to get the latest tag
	
	git tag | grep "^v[0-9]\{1,\}\.[0-9]\{1,\}\.[0-9]\{1,\}" | sort --version-sort -r | head -n 1
	
git reset --soft HEAD~1

git reset --hard HEAD~1