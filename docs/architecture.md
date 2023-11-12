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
1. User creates medication with schedule (e.g., 8:00, 20:00 daily).
2. App registers local notifications using device timezone.
3. User taps **Taken**; log is written to `logs` and adherence % updates.
