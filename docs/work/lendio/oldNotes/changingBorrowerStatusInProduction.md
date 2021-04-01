ssh api1.production.lendio.net
sudo -u deploy -I
export PATH=/usr/local/php/7.3.3/bin:$PATH
cd /var/www/api/current
php artisan tinker
$b = Borrower::find(#BORROWERID#)
$u = User::find(992232)
$b->changeStatus(#NEWSTATUS#,$u)