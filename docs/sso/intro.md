# Introduction
# 介绍
## What is the SSO
## 什么是SSO
Simply put, SSOs are a way for users to log into one web site using their username and password from another web site. For example, if go to [https://www.goodreads.com/](https://www.goodreads.com/) and try to sign in they will ask you if you want to sign in with Facebook, Twitter, Google, or even Amazon. For Goodreads this is great because it means they don't have to worry about trying to manage your username and password information. It also has the nice advantage of making it a lot easier for you as a user to sign into their site as you don't need to register or keep track of multiple extra account names and passwords.
简单来说，SSO是用户通过一个网站的用户名与密码来登录另一个网站的一种方法。举例来说，当我们访问[https://www.goodreads.com/](https://www.goodreads.com/) 并尝试登录时，网站会问你是否需要使用Facebook，Twitter，Google或者甚至是Amazon账户来登录，对于Goodreads来说，让你使用第三方账号登录无疑是很棒的选择——这意味着他们不再需要再担心在管理你的账号密码时所可能产生的问题了。同时，对你来说，这也意味着免去了注册一个新账户并管理其信息的麻烦。

For EVE Online, the SSO means that you can sign into a web site that has integrated the EVE SSO and confirm you are a specific character. While signing into a site you will be asked which character you wish to authenticate with and the web site that let you sign in with the EVE SSO will get confirmation from CCP that you own that character. The original web site will only ever get your character, they never see your account name or password. The original web site will not know what account that character is on or have any way, from us at least, of linking that character to any other character on the same account.
那么，对于EVE Online来说，SSO系统意味着您可以登录任何已集成EVE SSO系统的网站并让网站确定你的身份。登录站点时，系统将询问您希望使用哪个角色进行身份验证，网站将从CCP确认您拥有该角色。 原始网站只会获得您的角色信息而不会看到您的帐户名或密码。 原始网站将不知道该角色在哪个帐户上，至少无法通过本系统获知你的角色关联。

## Registering for the SSO
## SSO的注册
To use the SSO in your app, you must first register it at [the developers site](https://developers.eveonline.com/). When you create a new application here it will give you a client ID and secret key, which are used in the authentication flow.
若想要为你的应用继承EVE SSO系统，请访问[开发者站点](https://developers.eveonline.com/). 并进行注册来创建应用，创建完成应用之后你将会获得你的客户端ID和密钥，这些信息将会在之后的认证流程中用到。

You are required to supply the following:
你必须提供下述信息:
- Name: Name of the application, will be displayed to the users when asked to authorize your app.
- 名称：你的应用的名称，当用户被要求登录你的应用时，这将会被展示给他们
- Description: Description of the application, will be listed under your app in [Third Party Applications](https://community.eveonline.com/support/third-party-applications/).
- 描述：应用的描述，将会被列在[第三方应用](https://community.eveonline.com/support/third-party-applications/). 中你的应用下面
- Connection type: Can be API Access or Authentication Only. If API Access is selected, you will also need to select the scopes your app will use.
- 链接类型：API权限或者只是用于验证身份。如果有API权限需要被获取，你同时也要选定你的应用的使用范围
- Callback URL: Callback URL, which is the only location the login server will redirect back to after the user has authorized the login (See [Authentication flow](authentication.md) for details.)
- 回调地址：用户在完成操作后将会被重定向到此地址，详情：[认证流程](authentication.md)

### Errors
### 错误
Please note:
请注意：

If too many HTTP requests are done to an SSO endpoint within a set time interval the SSO will return a HTTP 409 response (being vague on the number of requests and time on purpose as we will be tuning these values).
如果你在设定的时间阈值内进行了太多的HTTP请求，则SSO将返回HTTP 409（由于我们会调整这个阈值，所以无法在此说明其确切值）。

### Test Server
All instances of https://login.eveonline.com can be swapped for https://sisilogin.testeveonline.com when trying to use Sisi.

### Login Images
When creating a button to direct users to login to your site or application with the EVE SSO please use one of the following images for the button. This helps create consistency for EVE players and when they view your site or application will more easily be able to quickly identify that it supports the EVE SSO.

![EVE SSO Login Buttons Large White](https://web.ccpgamescdn.com/eveonlineassets/developers/eve-sso-login-white-large.png)

![EVE SSO Login Buttons Large Black](https://web.ccpgamescdn.com/eveonlineassets/developers/eve-sso-login-black-large.png)

![EVE SSO Login Buttons Small White](https://web.ccpgamescdn.com/eveonlineassets/developers/eve-sso-login-white-small.png)

![EVE SSO Login Buttons Small Black](https://web.ccpgamescdn.com/eveonlineassets/developers/eve-sso-login-black-small.png)
