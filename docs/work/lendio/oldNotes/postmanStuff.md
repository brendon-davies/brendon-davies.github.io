for local pipeline api calls
URL: http://local-ls.lendio.com/api/<route>
auth url: http://local-ls.lendio.com/api/authorization/login
body(x-www-form-urlencoded):
username: 	brendon.davies@lendio.com
password:	my password
post

for local lender-portal calls
http://local-api.lendio.com/l/v2/<route>
auth URL: http://local-api.lendio.com/oauth/token
body (raw): 

{
	"client_id": 1,
    "client_secret": "cdd3ae298079a4e05968af73c8c8b101c155a012",
    "grant_type": "client_credentials"
}
get details from optimus.oauth_clients
post


for production public lender api calls:
URL: https://api.lendio.com/l/v2/<route>
auth url: https://api.lendio.com/oauth/token



staging api calls
URL: https://staging-api.lendio.com/l/v2/deals/1204701/offers
auth url: https://staging-api.lendio.com/oauth/token
