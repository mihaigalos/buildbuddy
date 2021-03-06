<!--
{
  "name": "Auth",
  "category": "5eed3e2ace045b343fc0a328",
  "priority": 300
}
-->
# Auth Configuration

Auth is only configurable in the [Enterprise version](enterprise.md) of BuildBuddy.

## Section

```auth:``` The Auth section enables BuildBuddy authentication using an OpenID Connect provider that you specify. **Optional**


## Options
* ```oauth_providers:``` A list of configured OAuth Providers.
  * ```issuer_url: ``` The issuer URL of this OIDC Provider.
  * ```client_id: ``` The oauth client ID.
  * ```client_secret: ``` The oauth client secret.
* ```enable_anonymous_usage:``` If true, unauthenticated build uploads will still be allowed but won't be associated with your organization.
## Google auth provider

If you'd like to use Google as an auth provider, you can easily obtain your client id and client secret [here](https://console.developers.google.com/apis/credentials).

## Example section

```
auth:
  oauth_providers:
    - issuer_url: "https://accounts.google.com"
      client_id: "12345678911-f1r0phjnhbabcdefm32etnia21keeg31.apps.googleusercontent.com"
      client_secret: "sEcRetKeYgOeShErE"
```