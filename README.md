# FirebasePushRestApi
python enhanced example  project to make firebase notification request


```

cred = credentials.Certificate("serviceAccountKey.json")
firebase_admin.initialize_app(cred)


messaging = firebase_admin.messaging


registration_token = "fDDmVgKjQsqCW3XLnfDJMg:APA91bE2pi2X-nXJ1KYD51aGm7yXXpflM-gFlVwElPPeRrvoHJJ1TDlgaChaO43GxZJQAXESj_qI2bApYsRD_DZs0KbEaHdGlgBpk3Gc8oOQYhNNoHWS0BkIkoOkfNXAKtC0v-3Uda2l"


message = messaging.Message(
    data={
        "title": "Astopia",
        "body": "Astopia",
        "deeplink":"astopia://Page=discovery"
    },
    token=registration_token,
)


response = messaging.send(message)
```
