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
      allow read : if request.auth.id != null
      allow write : if request.auth.id != null
    }
  }
}
```
