here's what you have to do to create stuff in nova

for reference look at claimborroweripwhitelist files

NOTE: when you create a model include this `use` statement:
  use \LendioPHPStandards\Models\Model;  
if you don't then when you try to add records in nova it will give you an error that it can't find a column like 'created_at'


	1. create the resource as defined here: https://nova.laravel.com/docs/1.0/resources/
	2. running the command above should create a resource in api/app/nova (you need to look at an existing resource and make changes to your new resource)
	3. then create the policy in api/app/policies
	4. then add a reference in api/app/providers/AuthServiceProvider.php
	5. then run npm run build in ng because the only way to access nova locally is through local-ls.lendio.com
	6. then you have to create a permission in nova by clicking on "Permissions" on the left hand side of nova and creating the permission. 

whenever you make changes to permissions locally (like adding or removing a permission from a role or user) you have to run Cache::flush() in tinker in api in vagrant+

this is what you need to use to make it so the resource doesn't show in the side pane public static $displayInNavigation = false;

in the nova resource, in the `fields` function which defines what columns will be displayed, if you have a column where the name consists of 2 words like `colorDescription` laravel automatically grabs that name and tries to look for a column named `color_description`. to override this so you can display your camel case column you have to have 2 arguments passed, so the value in the array that would be returned would be `Text::make('Color Description', 'colorDescription'),`
  

environments.php change and deploy
tenants
attach config
deploy or refresh config


Step by step instructions for creating a nova resource:

	1. in api locally run php artisan nova:resource ResourceName (should be proper case and singular, like Borrower)
	2. resource will now be in api/app/nova
	3. in resource change the path for `public static $model = ` from `App\MODEL_NAME` to  `App\Models\MODEL_NAME` because it defaults to the incorrect path
	4. in api/app/policies copy an existing policy and create one for your resource. should be proper case and have "Policy" after the name
	5. in policy change class name accordingly
	6. in api/app/providers/AuthServiceProvider.php create a record for your new resource/policy
	7. in ng run npm run build so you can re-build local-ls.lendio.com so you can access nova
	8. in nova create a permission for your resource (should be camel case and singular IE: borrower.write
	9. in resource in api\app\Nova add a label() function like in an existing resource that will define the name the resource will show as
	10. figure out what fields you want to display
	11. figure out what use statements you need to include to be able to display these values (IE: use Laravel\Nova\Fields\Text;) and include them in your resource
	12. in your resource make changes to the fields function to define the values you want to display
