# @expo-apple-2fa/twilio

## Usage

1. Put your Twilio SID and auth token into your Github Secrets.

1. In your Github Action, pass in your Twilio credentials as environment variables
   alongside the standard action inputs.

   ```
   - uses: jakemwood/expo-apple-2fa@plugins
     with:
       expo_apple_id: ${{ secrets.APPLE_ID }}
       expo_apple_password: ${{ secrets.APPLE_PASSWORD }}
       tfa_phone_number: ${{ secrets.TWO_FACTOR_PHONE_NUMBER }}
       app_specific_password: ${{ secrets.APP_SPECIFIC_PASSWORD }}
     env:
       TWILIO_ACCOUNT_SID: ${{ secrets.TWILIO_ACCOUNT_SID }}
       TWILIO_AUTH_TOKEN: ${{ secrets.TWILIO_AUTH_TOKEN }}
       TWILIO_FROM_NUMBER: ${{ secrets.TWILIO_PHONE_NUMBER }}
    ```

1. Add a configuration file **2fa.config.json** to the root of your repo to enable the plug-in.

   ```
   [ { name: '@expo-apple-2fa/twilio', async: false }]
   ```
