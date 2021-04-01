caching:
	- only caches if stateSubscriptionService has subscribers
	- if event size is > $this->pusher->maxPayloadBytes

how much data will be sent to the cache

plan
	1. cache all borrowers assigned to non system account reps 
	2. make sure cache is always up to date (possibly remove if check in calculateAndPush function in apprequirements listener)
	3. cache no matter how big or small (handle maxPayloadBytes check in statesubscriptionservice) 
	4. make sure cache gets deleted when no longer needed (possibly in handle function in apprequirementlistener)



eager loading:
some code is bypassing relationships
	borrowerAttributes 20 21   fix by singleton service
	borrowerValues join borrowerAttributes twice for each borrower = 40   2 points in code
	contacts each borrower 4 times = 80  4 points in code
	bankStatementAccounts (eager loading does work but something is bypassing that relationship) 21 1 point in code
	documents 20 1 point in code
	ignoredAppRequirementWarnings 20
	users 20
	=== PAIN IN THE BUTT


something else: