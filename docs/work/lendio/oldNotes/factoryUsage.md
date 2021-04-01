to use a factory here is an example of the tinker command to do so:

factory(\App\Models\Chat::class,1)->create(['borrowerId' => 3290503])

the above command will create 1 chat record for the borrower id specified

factory(\App\Models\Borrower::class,500)->create(['userId' => 2961507])