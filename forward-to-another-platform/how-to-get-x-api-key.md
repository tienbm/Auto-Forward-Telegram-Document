# How to Get X API Key

Use this guide to connect an **X** account to AutoForward. The current X Developer Console labels the credentials below under **OAuth 1.0 Keys**.

### The four values AutoForward needs

| AutoForward field     | Label in X Developer Console             |
| --------------------- | ---------------------------------------- |
| `Consumer Key`        | Consumer Key (also called API Key)       |
| `Consumer Secret`     | Consumer Secret (also called API Secret) |
| `Access Token`        | Access Token                             |
| `Access Token Secret` | Access Token Secret                      |

All four values are required. They must come from the same X App and the X account that will publish posts.

### Get the credentials

1. Open [console.x.com](https://console.x.com/) and sign in with the X account that will be used for publishing.
2. Create an App if you do not already have one, or select the existing App you want AutoForward to use.
3. Open **Apps**, choose the App, then open **Keys & Tokens**.
4. In **OAuth 1.0 Keys**, copy the **Consumer Key** and **Consumer Secret**.
5. In the same section, generate the **Access Token** for the publishing X account. Copy both the **Access Token** and **Access Token Secret** that X displays.
6. In AutoForward, open **Platform Accounts → Add Account → X**, then paste each value into the matching field and save.

X may show a **Regenerate** button instead of **Generate**. Regenerating a credential replaces the old value, so update the matching value in AutoForward immediately.

### Allow posting before generating tokens

Open your App's **Settings** and set its permissions to **Read and write** before generating the Access Token. If you change permissions later, regenerate the Access Token pair and replace both values in AutoForward; existing tokens can keep the old permissions.

### Do not use these values

AutoForward uses OAuth 1.0a credentials. Do **not** paste any of these values into the four fields above:

* Bearer Token
* Client ID
* Client Secret
* OAuth 2.0 Access Token

They belong to a different X authentication method and cannot replace the four OAuth 1.0 values listed in the table.

### Troubleshooting

* **Connection or publishing fails:** confirm that all four values were copied from the same App, and that the Access Token belongs to the X account that should publish.
* **You changed permissions or regenerated a value:** generate a fresh Access Token pair and update AutoForward before verifying again.
* **X reports no credits or API access:** open **Billing → Credits** in the X Developer Console, add credits or confirm your App has access to the required API endpoint, then retry.

### Keep credentials secure

Treat every value as a password. X may display generated credentials only once; store them in a secure password manager, never share them in screenshots or support tickets, and regenerate them immediately if exposed.
