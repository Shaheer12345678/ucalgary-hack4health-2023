# MediTrack — Architecture (Flutter + Firebase)

- **Frontend:** Flutter (Dart), Material UI
- **Auth:** Firebase Auth (email/Google)
- **Data:** Cloud Firestore
- **Notifications:** Firebase Cloud Messaging + local notifications
- **Storage:** Firebase Storage for optional prescription images

## Collections

- `users/{uid}`: profile, timezone
- `users/{uid}/medications/{medId}`: name, dosage, schedule (RRULE-like)
- `users/{uid}/logs/{logId}`: taken/skipped, timestamp, reason

## Reminder Flow
