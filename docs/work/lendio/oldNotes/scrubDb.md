if you ever get this error:



you just need to run this inside vagrant:

sudo service ntp stop && sudo ntpd -gq && sudo service ntp start