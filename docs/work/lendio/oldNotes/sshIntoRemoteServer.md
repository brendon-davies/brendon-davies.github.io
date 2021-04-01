this is the command you need to run to be able to tinker in a remote server

export PATH=/usr/local/php/7.4.12/bin:$PATH

export PATH=/usr/local/php/7.3.3/bin:$PATH

NOTE: i just had an issue with running tinker commands on job1 and the problem was that i was using the wrong version of php in the export command above. make sure the version is correct if you're having issues

this is the command to sudo to deploy

sudo -i -u deploy


rollback plan
monitoring precautions
look into backend permission loading borrower into cache

api-sandbox.production.lendio.net


this is how to create a test deal via tinker

Auth::login(App\Models\User::find(SYS_USER_ID));
App::instance('user', App\Models\User::find(SYS_USER_ID));
$lp=App\Models\LoanProduct::find(386)
Auth::user()->lenderUser->lender->newTestDeal($lp)