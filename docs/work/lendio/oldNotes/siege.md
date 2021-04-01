siege is a tool that allows you to stress test a url or endpoint

https://linux.die.net/man/1/siege

you specify a file with the -f switch. all you do is navigate to the directory where that file is and then run `siege -v -f YOUR_FILE_NAME`

if you are wanting to hit staging you need to call siege like this

siege -v -H "authorization:Bearer TOKEN" -f YOUR_FILE_NAME

to get the bearer token just log into staging pipeline and copy an api call as cURL, plug that into postman and get the bearer token from there

siege -v -H "authorization:Bearer TOKEN" -f YOUR_FILE_NAME -t2M

this command executes siege for 2 minutes (-v is for verbose, -H is for header, -f is the file that contains your urls to hit and -t specifies the time to run it for)
siege -v -H "authorization:Bearer D3qDb6kFuSqBhBC5SrFTqFoAWMubyoOP0iLtWNJC" -f siege_urls.txt -t2M