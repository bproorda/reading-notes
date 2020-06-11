# Authorization by Roles and Claims

## Role Authroization

If you have different levels of access, such as admin, owner, customer, you can create a table for each kid of user. As Keith would say
"Gross." The other, much better option is create one table/database of users and give the users different *Roles*. These can be used to identity the access level of each user.

When you are adding the attribute of Authorize, expand it to reflect a given role such as: `[Authorize(Roles = "Administrator")]`.
If the action requires to be one of multiple roles use commmas `[Authorize(Roles = "HRManager,Finance")]`. They are required to have *all* of a set roles, write out more than one attribute 
```
   [Authorize(Roles = "PowerUser")]
   [Authorize(Roles = "ControlPanelUser")]
```
These attributes can be added at the controller of the action level.

An alternative to use the Roles Attribute is use the policy attribute `[Authorize(Policy = "RequireAdministratorRole")]`. For these to work they must be defined in configures services in start up 
```
  public void ConfigureServices(IServiceCollection services)
{
    services.AddControllersWithViews();
    services.AddRazorPages();

    services.AddAuthorization(options =>
    {
       options.AddPolicy("RequireAdministratorRole",
             policy => policy.RequireRole("Administrator"));
    });
}
```

## Claim Authorization

When an identity it created, a trusted party can issue it one more claims, value pair that represents what the subject is. Claims based authorization, at its simplest, checks the value of a claim and allows access to a resource based upon that value.

To check if a claim exists or the claim of a claim that policy must be registered in startup.
```
   public void ConfigureServices(IServiceCollection services)
{
    services.AddControllersWithViews();
    services.AddRazorPages();

    services.AddAuthorization(options =>
    {
        options.AddPolicy("EmployeeOnly", policy => policy.RequireClaim("EmployeeNumber"));
    });
}
```
In this case the EmployeeOnly policy checks for the presence of an EmployeeNumber claim on the current identity.

Then apply the attribute to the action or controller `[Authorize(Policy = "EmployeeOnly")]`
