# CakePHP Application Skeleton

A skeleton for creating applications with [CakePHP](http://cakephp.org) 3.x. The skeleton has been preloaded with the [Acl](https://github.com/cakephp/acl), [AclManager](https://github.com/ivanamat/cakephp3-aclmanager) plugins. Manages groups, roles, users and ACL.

## Loaded plugins
* The framework source code can be found here: [cakephp/cakephp](https://github.com/cakephp/cakephp).
* The Acl plugin source code can be found here: [cakephp/acl](https://github.com/cakephp/acl).
* The AclManager plugin source code can be found here: [ivanamat/cakephp3-aclmanager](https://github.com/ivanamat/cakephp3-aclmanager).


## Installation

```bash
composer create-project --prefer-dist stevenmybarra/cakeapp [app_name]
```

You should now be able to visit the path to where you installed the app and see
the setup traffic lights.

## Configuration

### MySQL

Import the `config/schema/cakeapp.sql` file to your database.

### APP
Read and edit `config/app.php` and setup the 'Datasources' and any other
configuration relevant for your application.

Uncomment `$this->Auth->allow();` from initialize function on `AppController`. This lets you create Groups, Roles and Users.

Uncomment `return true;` from isAuthorized function on `AppController`. This allows you to access the Acl Manager plugin.

    
## Create the first group, the main role and the first user.

* Now go to the Groups area and create your first group.
* Access Roles area and create a new role for the group you created. It is recommended to create the first role with the name 'Root'. The role you have created with id 1 will always have all permissions.
* Create a user with the group and role you just created.
* Log in on `/Users/login` as the user created, go to `/AclManager` and click on `Restore to default` to create ACOs and AROs automatically. 

## Comment the uncommented

Comment `$this->Auth->allow();` from initialize function and `return true;` from isAuthorized function on `AppController`.


## Enjoy!

Now you can start customizing your permissions and Develop your app. Do not forget to update the ACOs when creating new functions.
