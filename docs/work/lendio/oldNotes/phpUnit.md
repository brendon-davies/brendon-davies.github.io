here is how to run an individual method in a test

in the root of api run:

phpunit --filter testCreateOfferAfterDealInactive  tests/PublicLenderApi/OfferController/OfferControllerPostTest.php

testCreateOfferAfterDealInactive is the method name, the other part is the path to the file


./vendor/bin/phpunit --filter testMissingBorrower tests/Unit/Http/Controllers/Leads/LeadsTest.php


./vendor/bin/phpunit --filter CircleIncludedOnDeckApiTest