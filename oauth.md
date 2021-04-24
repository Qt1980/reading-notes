# What is OAuth? How the open authorization framework works

Since the beginning of distributed personal computer networks, one of the toughest computer security nuts to crack has been to provide a seamless, single sign-on (SSO) access experience among multiple computers, each of which require unrelated logon accounts to access their services and content. Although still not fully realized across the entire internet, myriad, completely unrelated websites can now be accessed using a single physical sign-on. You can use your password, phone, digital certificate, biometric identity, two-factor authentication (2FA) or multi-factor authentication (MFA) SSO solution to log onto one place, and not have to put in another access credential all day to access a bunch of others. We have OAuth to thank for much of it.

## OAuth definition

OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

## OAuth history

Created and strongly supported from the start by Twitter, Google and other companies, OAuth was released as an open standard in 2010 as RFC 5849, and quickly became widely adopted. Over the next two years, it underwent substantial revision, and version 2.0 of OAuth, was released in 2012 as RFC 6749. Even though version 2.0 was widely criticized for multiple reasons covered below, it gained even more popularity. Today, you can add Amazon, Facebook, Instagram, LinkedIn, Microsoft, Netflix, Paypal and a list of other internet who’s-whos as adopters.

## OAuth examples

The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.

Another common example OAuth scenario could be a user sending cloud-stored files to another user via email, when the cloud storage and email systems are otherwise unrelated other than supporting the OAuth framework (e.g., Google Gmail and Microsoft OneDrive). When the end-user attaches the files to their email and browses to select the files to attach, OAuth could be used behind the scenes to allow the email system to seamlessly authenticate and browse to the protected files without requiring a second logon to the file storage system. Another example, one given in the OAuth 2.0 RFC, is an end-user using a third-party printing service to print picture files stored on an unrelated web server.

In all cases, two or more services are being used for one transaction by the end-user, and every end-user would appreciate not being asked to log in a second time for what they feel is a single transaction. For OAuth to work, the end-user’s client software (e.g., a browser), the services involved and authentication provider must support the right version of OAuth (1.0 versus 2.0).

## OAuth explained

When trying to understand OAuth, it can be helpful to remember that OAuth scenarios almost always represent two unrelated sites or services trying to accomplish something on behalf of users or their software. All three have to work together involving multiple approvals for the completed transaction to get authorized.

## Authentication and Authorization Flows

In this article
Auth0 uses the OpenID Connect (OIDC) Protocol and OAuth 2.0 Authorization Framework to authenticate users and get their authorization to access protected resources. With Auth0, you can easily support different flows in your own applications and APIs without worrying about OIDC/OAuth 2.0 specifications or other technical aspects of authentication and authorization.

While often used interchangeably, authentication and authorization represent fundamentally different functions. In this article, we compare and contrast the two to show how they protect applications in complementary ways.

In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.

Comparing these processes to a real-world example, when you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.

-----------------------------------------------------------
Content for this page are from online resources found under 301 Resources Class 11 at [Resources](/Resources.md)

[Back to Table of Contents](/README.md)