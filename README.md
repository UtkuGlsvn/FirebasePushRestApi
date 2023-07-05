# FirebasePushRestApi
python enhanced example  project to make firebase notification request


```


cred = credentials.Certificate("serviceAccountKey.json") #  your service account key -> Get firebase console
firebase_admin.initialize_app(cred) 

messaging = firebase_admin.messaging


registration_token = "your device id"

#example message data

message = messaging.Message(
    data={
        "title": "Notif Title",
        "body": "Notif body",
        "deeplink":"myapp://..."
    },
    token=registration_token,
) 


response = messaging.send(message)
print("Message ID:", response)

```
