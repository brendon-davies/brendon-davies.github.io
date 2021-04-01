in the top of the cron's php file there should be a schedule that looks like this:

protected $signature = 'schedule:check-jobs';

to run this cron you would run this command in api in vagrant:

php artisan schedule:check-jobs

you need to make some changes locally to get this to run

in the opsgenie.php file, comment out these lines (this is an environment check):

if (!is_array($payload) || env('APP_ENV') != 'LIVE' ) {
     return false;
}

then back in your cron's php file there should be a line that looks like this:

protected $cron = '*/10 8-23 * * *';

change it to look like this (this will make  the cron run every minute):

protected $cron = '*/1 * * * *';

 then in the cron php file, where it's calling opsgenie post alert add this to the array it passes:

'details' => ['test' => 'true'],

last but not least in the array that is passed to the opsgenie post function change the priority to be a p3, so change this:

'priority'    => 'P2',

to this:

'priority'    => 'P3',

so you can run the command and generate the opsgenie alert. the alert will show in the #alert-spam slack channel. every time you trigger the alert you need to acknowledge it and then close it before you trigger another test

when you trigger the alert you might need to run this to get the alert to post:

php artisan schedule:run

to run a task (command) in api just run this `php artisan task:task-name`
