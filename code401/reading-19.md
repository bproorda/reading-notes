# Intro to Identity
- ASP.NET Core Identity is a membership system that adds login functionality to ASP.NET Core apps
- Users can create an account with the login information stored in Identity or they can use an external login provider. Supported external login providers include Facebook, Google, Microsoft Account, and Twitter.
- AddDefaultIdentity was introduced in ASP.NET Core 2.1. 
- when creating a web application Select an ASP.NET Core Web Application, then select Change Authentication
- then Select Individual User Accounts and click OK.
- The generated project provides ASP.NET Core Identity as a Razor Class Library. The Identity Razor Class Library exposes endpoints with the Identity area. 
- use update-database in package manager console
- run the app and register a user
- go to SQL explorer and look for the AspUsers Table
- add new settings to configuresettings in start up, check reading there is a lot.
- add ` app.UseAuthentication();` to configure
- When a user clicks the Register link, the `RegisterModel.OnPostAsync` action is invoked. The user is created by `CreateAsync` on the `_userManager` object
- ` var result = await _userManager.CreateAsync(user, Input.Password);` see reading for more
- When the form on the Login page is submitted, the `OnPostAsync` action is called. `PasswordSignInAsync` is called on the `_signInManager` object.
- `var result = await _signInManager.PasswordSignInAsync(Input.Email, Input.Password, Input.RememberMe, lockoutOnFailure: true);`
- The Log out link invokes the LogoutModel.OnPost action. 
- SignOutAsync clears the user's claims stored in a cookie.