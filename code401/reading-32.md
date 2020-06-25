# React Login and Auth

## ROLE-BASED ACCESS CONTROL (RBAC)
- restricts network access based on a person's role
- Employees are only allowed to access the information necessary to effectively perform their job duties
- can be based on several factors, such as authority, responsibility, and job competency.
- By adding a user to a role group, the user has access to all the roles in that group.
- best practices 
  - status: keep track of what kind of security, physical or digital, each system has and who has access to them.
  - Roles: organize roles to optimize security and not impede the work culture
  - write a policy
  - implement system/make changes
  - keep adapting/improving

## react-cookies
- need to use a cookie to store JWT received from API for authorization and authentication
- there is a handy react-cookie library
- `By adding a user to a role group, the user has access to all the roles in that group.`
- `import cookie from 'react-cookies'`
- inside the component class
  ```
   onLogin(userId) {
    this.setState({ userId })
    cookie.save('userId', userId, { path: '/' })
  }
    onLogout() {
    cookie.remove('userId', { path: '/' })
  }
  ```
- 
