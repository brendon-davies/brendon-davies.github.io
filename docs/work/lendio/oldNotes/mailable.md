you can test a mailable by making an api call to this url:

local.lendio.com/api/mailable/your-mailable-name/123

the 123 is required to allow you to be able to pass something in to be used by the test funciton

for this to work your mailable has to have a test function in it like this:

public static function test($id)
{
    return (new NotificationFired())->to('blah@blah.com', 'joe blah');
}

if your route is nested list the folders and then a period (.) and then the name of the mailable, all in studly case, like this

local-ls.lendio.com/api/mailable/lp-notification.new-comment/907333

local-ls.lendio.com/api/mailable/notification-fired/907333
