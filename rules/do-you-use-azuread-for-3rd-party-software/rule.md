---
type: rule
title: Do you use Azure AD to authenticate and provision users for 3rd-party software?
uri: do-you-use-azuread-for-3rd-party-software
authors:
  - title: Warwick Leahy
    url: https://www.ssw.com.au/people/warwick-leahy
created: 2022-10-25T12:53:03.789Z
guid: 7dd32509-f2a5-4d1d-96d9-b16a1c2c498c
---
If you are already using Azure AD as your main authentication then it makes a lot of sense to use your Azure AD as the source of truth for 3rd party software as well.  Many providers are already providing and encouraging this using a protocol called SAML for authentication and SCIM for provisioning users.          
            
<!--endintro-->

There are some great reasons to use Azure AD as a source of truth for provisioning and authenticating your users.

### Security  
1. Auto provisioning users with SCIM means that users who are in the right group will get an account and access to the relevant areas of the software as soon as a sync occurs.  Admins only need to add the user to a group in 1 place and the rest automatically happens.  
2. It is easy to forget all the 3rd party software that a user has access to.  Auto provisioning with SCIM also automatically disables a user in the 3rd party software when their Azure AD account is disabled.  This plugs a lot of leaks.  
4. Using SAML for authentication with Azure AD allows access to conditional access and all of the AI associated such as Location, Trusted Devices and Risk Policies.  

### Reduces manual work
1. Although some software provides it's own conditional access policies such as valid locations.  If you are already running Azure AD then you already have access to those features.  Using SAML means that you won't need to replicate the same rules in more than 1 place.
2. Auto provisioning (and de-provisioning) reduces workload significantly as there is no requirement to add and delete users from multiple places.  

3. Groups can also be auto provisioned which removes the requirement to manually maintain groups and roles in multiple places.