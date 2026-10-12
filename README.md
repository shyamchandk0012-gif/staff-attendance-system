# Staff Attendance Register starter

## Upload
Upload `index.html` to the root of your GitHub repository, named exactly `index.html`.

## Firebase setup
1. Authentication > Sign-in method: enable Email/Password.
2. Authentication > Users > Add user: create your own admin email/password.
3. Copy that user's UID.
4. Firestore > Data > Start collection `users`; use the UID as document ID and add:
   - `name` string
   - `username` string
   - `email` string
   - `role` string = `admin`
   - `active` boolean = `true`
5. Firestore > Rules: replace the rules with the contents of `firestore.rules`, then Publish.

Do not use real attendance data until you have tested the security rules.

## Publish
GitHub repository > Settings > Pages > Build and deployment > Deploy from a branch > `main` > `/(root)` > Save.

## Notes
This starter includes login, admin employee creation, check-in/out, monthly totals and CSV export. Google Sheets sync is not yet connected; we should add it after authentication/rules are tested. The browser code uses Firebase's public web configuration, not a password. Security must be enforced by Firebase rules. For a production deployment, employee account provisioning should be moved to a trusted backend, and check-in/out timestamps should be validated server-side.
