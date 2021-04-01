when you merge master into production for ng, you need to let stuff process before you can deploy production

on the pull request page on github where you merged master into production, click on the checkmark next to the merge statement toward the bottom of the page

this takes to circle, then click on workflows on the left hand pane


then click on the workflow that is at the top that should be running

this should take you to the actual workflow view that shows all of the jobs running

wait for all of the jobs to finish. the specific job you need to let finish is the publis-github-release one, but it's a good idea to wait for all of them before you deploy production