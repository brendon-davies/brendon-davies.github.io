# Brendon Davies Personal Documentation

How these docs work technically:

The repo is https://github.com/brendon-davies/brendon-davies.github.io that contains the code for the docs.

The docs live in the docs directory within the repo.

The main page is the index.html file within there. 

The index.html is encrypted using staticrypt which makes it password protected.

The docs are served up on netflify at this url: https://seivadnodnerb.netlify.app

To push changes all you need to do is merge into the master branch in the repo on github and the changes should reflect.


How to encrypt these docs:

You shouldn't need to re-encrypt this unless you make any changes to the index.html because that is the only file that is encrypted

and all of the other pages are not accessible unless you go through the index.html.

To encrypt the index.html go here: https://robinmoisson.github.io/staticrypt/

put the password you want to use to encrypt the page with in the box labeled `Passphrase`

then just take the entire contents of the index.html, paste them inside the box labeled `HTML/string to encrypt`

then click on the button on the bottom right hand side labeled `Generate passphrase protected HTML`

this then gives you a big long junk string in the last box on the page.

Click the `Download html file with password prompt` button and you download an encrypted html file 

Open this file, take the contents and put them inside the index.html before you push it up

When you merge into master, the encrypted index.html will then force you to enter the password before you can 

browse to any of the pages within these docs.

The `indexUnEncrypted.html` and `indexUnEncryptedBackup.html` contain the un-encrypted index.html code

The `indexEncrypted.html` contains the encrypted index.html

if you don't make any changes to the index.html you can just swap these around, using the un-encrypted for dev work

and then switch it to the encrypted version to deploy

On your Lendio mac the alias `pdsdev` sets this up to use the un-encrypted index.html

the alias `pdsdep` swaps in the encrypted index.html so you can deploy



Here's a list of my repos on Github:

angularStuff: https://github.com/brendon-davies/angularStuff

asanaStuff: https://github.com/brendon-davies/asanaStuff

assemblyStuff: https://github.com/brendon-davies/assemblyStuff

&nbsp;  
&nbsp;  

bashStuff: https://github.com/brendon-davies/bashStuff

batchStuff: https://github.com/brendon-davies/batchStuff

bootstrapStuff: https://github.com/brendon-davies/bootstrapStuff

brendon-davies.github.io: https://github.com/brendon-davies/brendon-davies.github.io
- **this is my docs repo for these docs**
&nbsp;  
&nbsp;  

cards: https://github.com/brendon-davies/cards
- **repository to keep track of card (project) data from Lendio**
&nbsp;  
&nbsp;  

cSharpStuff: https://github.com/brendon-davies/cSharpStuff
&nbsp;  
&nbsp;  

excelStuff: https://github.com/brendon-davies/excelStuff

javaStuff: https://github.com/brendon-davies/javaStuff

javaScriptStuff: https://github.com/brendon-davies/javaScriptStuff

&nbsp;  
&nbsp;  

luaStuff: https://github.com/brendon-davies/luaStuff

&nbsp;  
&nbsp;  

miscStuff: https://github.com/brendon-davies/miscStuff
- **miscellaneous stuff I couldn't think of where to put**
&nbsp;  
&nbsp;  

mySQLStuff: https://github.com/brendon-davies/mySQLStuff

&nbsp;  
&nbsp;  

oracleStuff: https://github.com/brendon-davies/oracleStuff

&nbsp;  
&nbsp;  

phpStuff: https://github.com/brendon-davies/phpStuff

prs: https://github.com/brendon-davies/prs
- **repository to keep track of PRs I reviewed from Lendio**
&nbsp;  
&nbsp;  

pythonStuff: https://github.com/brendon-davies/pythonStuff

&nbsp;  
&nbsp;  

rubyStuff: https://github.com/brendon-davies/rubyStuff

&nbsp;  
&nbsp;  

sqlServerStuff: https://github.com/brendon-davies/sqlServerStuff

&nbsp;  
&nbsp;  

typeScriptStuff: https://github.com/brendon-davies/typeScriptStuff

&nbsp;  
&nbsp;  

vueStuff: https://github.com/brendon-davies/vueStuff

&nbsp;  
&nbsp;  

writing: https://github.com/brendon-davies/writing

