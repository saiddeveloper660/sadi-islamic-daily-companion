# Security Notes

- Never commit `.env`, API keys, access tokens, passwords, signing keys, or service-account files.
- Keep Android signing files (`.jks`, `.keystore`) outside the repository.
- Use environment variables or your CI secret store for private build credentials.
- A key embedded in an Android APK can usually be extracted. Do not treat a client-side API key as secret.
- If a private key was ever committed, revoke/rotate it with its provider; deleting it in a later commit is not enough.
- `google-services.json` is ignored by default. Review Firebase rules and API restrictions before deciding whether to distribute Firebase configuration.
