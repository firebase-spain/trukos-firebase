# Trukos-Firebase

Comandos
```
firebase logout
firebase login
firebase login --reauth
```



Comandos para dar permisos a cloud firestore
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
       allow read, write: if request.auth != null;
    }
  }
}
```
