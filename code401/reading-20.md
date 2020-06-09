# Authentication

## JWT Authentication
- JSON Web Token, a way for securely transmitting information between parties as a JSON object
- contains three parts: Header, Payload, Signature
- Header
 - one part is signing algorithm, the other is type of token
 - ```
        {
        “alg”: “HMAC”,
        “typ”: “JWT”
        }
    ```
- Payload: contains the claims. Claims are statements about an entity (typically, the user) and additional data
- Signature: For the signature created you need to use encoded header, encoded payload, and secret with the algorithm specified at the header.
- ```
        HMAC(
        base64UrlEncode(header) + “.” +
        base64UrlEncode(payload),
        secret)
    ```
**Setting up JWT**    
- install Microsoft.AspNetCore.Authentication.JwtBearer
- Update Startup.cs ConfigureService() to register JWT authentication scheme see https://medium.com/@vaibhavrb999/jwt-authentication-authorization-in-net-core-3-1-e762a7abe00a
- change appsettings.json with required details for JWT authentication scheme
- call app.UseAuthentication in Configure() method
- Update Startup.cs file ConfigureService() method to add authorization code
- create a new API controller called LoginController and defined Login() method inside it
- mark this method as AllowAnonymous attribute to bypass the authentication this method expects the User model object with a username and password parameter.
- define one more method called AuthenticateUser(), to be called inside Login()
- JwtSecurityTokenHandler.WriteToken method is used to generate the JWT
- We have to create UserController which contains the method according to Roles i.e User and Admin. If you want to restrict the method access we can do this with Authorize attribute.