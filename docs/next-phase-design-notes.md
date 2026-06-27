# Next Phase Design Notes

## Notifications

- Start with local opt-in reminders using the Web Notifications API and a service worker.
- Keep reminder rules local first: unfinished daily checks, sleep cutoff reminder, and streak recovery reminder.
- Add server push only after account sync exists, because cross-device notification state needs a stable user identity.

## Account Linking

- Introduce account sync after the local-only MVP is stable.
- Keep local storage as the offline-first source and sync a versioned user profile, task list, daily checks, and future-self settings.
- Use a managed auth provider or OAuth-based sign-in, then migrate anonymous local data into the signed-in account with an explicit confirmation step.
