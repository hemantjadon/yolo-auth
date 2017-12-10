# \<yolo-auth\>

`yolo-auth` is wrapper around Google OneTap YOLO implementation. It notifies the successful authentication and provides user information and handles Google YOLO implementaion.

## OpemYOLO

[OpenYOLO](https://github.com/openid/OpenYOLO-Web) for Web is an OpenID Foundation project to provide in-context credential exchange and management. By using this API, a requesting page can directly retrieve existing credentials in the user's preferred credential manager.

## Google YOLO (One-Tap Sign Up and automatic sign in)

[Google YOLO](https://developers.google.com/identity/one-tap/web/overview) is Google's implementaion for **One-Tap** Sign Up and **automatic** Sign In using **OpenYOLO** protocol.

## Usage

```html
<yolo-auth
	id="auth"
	user="{{user}}"
	client-id="your-google-oauth2-client-id">
</yolo-auth>
```

Javascript sign-in calls can then be made to the `yolo-auth` object to attempt Sign Up/Sign In

```javascript
this.$.auth.signIn()
	.then((user) => {
		// Successful response
	})
	.catch((error) => {
		// Unsuccessful Response
	});
```

By this users are prompted to create an account with a dialog that's inline with your page's content, so they're never taken out of context by a sign-up page. With just one-tap they get secure, token-based, passwordless account with your service, protected by their Google Account.