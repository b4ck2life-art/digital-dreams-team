# Privacy Policy — Podsetnik za lekove

**Effective and last updated:** 2026-10-27

Podsetnik za lekove is an Android medicine-reminder app that reminds you to take the medicines you entered and records what you did. This policy explains what the app does with information when you use it.

Contact for privacy questions: [b4ck2life@gmail.com](mailto:b4ck2life@gmail.com).

## Local health data

Medicines, schedules, dose history and the app's settings are stored in app-private storage on your device. The app has no account and no server of ours, so this information is not sent to us. Manual entry is always available and does not depend on a catalogue.

## Photos you choose

You select a photo through Android's system photo picker. The app copies and downscales the selected image into app-private files and addresses it by path, never by a persisted `content://` URI. It does not need a broad storage permission.

The app does not upload the photo and excludes it from exports. The private copy is used as the medicine's picture.

## Notifications and lock-screen privacy

The lock-screen content of a reminder is your choice. The default is GENERIC. FULL may show the medicine and amount; GENERIC shows only "Time for your medicine" with a redacted public version; HIDDEN keeps the content off the lock screen entirely. Before the first unlock after a reboot, a delivered alarm is always generic and has no action buttons.

## Optional screenshot protection

Screenshot protection is one optional setting, OFF by default. When it is ON, the app applies Android's `FLAG_SECURE` to its window, which blocks screenshots of medicine screens and hides those screens from the recent-apps preview.

When it is ON, protection covers Home, the medicine list, medicine details (including schedule and history), archived medicines, the medicine editor, catalogue search, the intake sheet and the ringing screen. Settings, Diagnostics and onboarding are not protected by this setting.

The choice is stored locally as the ASCII code OFF or ON. It is not sent anywhere, stores no health content and needs no permission. If the stored value cannot be read, the app applies protection (ON) for safety, selects no option in Settings and leaves the stored bytes unchanged until you choose again. The setting does not alter notification content, lock-screen privacy, alarm delivery or saved state.

## Catalogue searches

The app offers two catalogue providers. Searching is optional, manual entry is always available, and the region you choose decides which provider is used.

### RxNav / RxTerms (United States)

When you search the United States catalogue, the app sends your explicit search text to RxNav/RxTerms, a service of the U.S. National Library of Medicine (NLM). The request also carries this app's own User-Agent, `PodsetnikZaLekove (Android; com.digitaldreamsteam.podsetnikzalekove)`, and a standard `Accept: application/json` header.

The region and the locale stay on the device. The app does not send an account or a device identifier. The result is cached locally for 12 hours.

### ALIMS (Serbia)

The Serbian ALIMS medicines register is published as open data and is re-exported daily. It has no query endpoint, so the app downloads the whole register (about 4.5 MB) and searches it on your phone. Neither your search text nor your locale leaves the device.

The app makes that download at most once a day. Nothing about the user is sent; the only identifying header is this app's own User-Agent, and the request also carries a standard `Accept: application/json` header. The fully validated register revision is cached locally and replaced only by a validated successor. An imported medicine keeps its own immutable snapshot.

## Voice input

Voice input is optional and always starts with one explicit tap on the microphone. After the runtime permission, if it is needed, that tap starts one bounded recognition attempt. You may stop or cancel it; a final result or failure ends it. There is no continuous, background or hotword listening.

The sound is handled by the speech-recognition service Android selects. That service may use the network and has its own terms. This app creates no audio file, stores no transcript and logs no transcript. The recognition result lives in memory for that one attempt. If you use a phrase as a catalogue search, it becomes ordinary query text and follows the catalogue rules above, including the 12-hour local cache for a United States search.

Typing always works instead, and you can deny or revoke the microphone at any time.

## Spoken reminders (text to speech)

If you turn on the voice alert mode, the app hands the spoken phrase to the text-to-speech service installed on your device. The phrase includes the medicine name and amount when the "speak medicine names" setting is on. The text-to-speech provider may use its own network service, so we cannot promise that speech never leaves the device.

The app does not log the phrase or medicine values. If no usable engine is available, the alarm falls back to the bundled chime. You can switch the voice mode and "speak medicine names" off.

## Exports

Exports happen only when you start one. The app can write:

- a JSON backup of your medicines, schedules and dose history;
- a CSV history report.

The app writes the export only to the destination you choose and does not upload it. The export does not include your photos. The resulting file is yours, and you can delete it.

## Backup and device transfer

Cloud backup of your medicine data is switched off. Moving the app to a new phone with Android's device-to-device transfer keeps your data. The app's cloud-backup rules exclude its database, preferences and files; device-to-device transfer includes them.

## No account, backend, analytics or advertising

The app needs no account. There is no analytics, no crash reporting and no advertising. We do not sell your data, and we do not operate a backend that receives it. When you explicitly use catalogue search, voice input, spoken reminders, exports or support email, information is handled only by the provider or destination described in this policy.

## Support email and external actions

"Write to us" opens the user's mail composer addressed to b4ck2life@gmail.com. It pre-fills only the app version, Android release and API level, and interface language. It adds no medicine, schedule, transcript, catalogue query, attachment, stream or content URI. Nothing is sent unless the user chooses to send the message. The selected mail provider and recipient then handle the message under their own terms.

Rating and privacy-policy actions only open their external destination; the app adds no medicine data. Share remains unavailable while PLAY_LISTING_URL is null.

## Your choices

- Enter a medicine manually instead of using a catalogue, and choose the catalogue region.
- Start voice input only by tapping the microphone, stop or cancel an attempt, deny or revoke the microphone, or type instead.
- Switch the voice alert mode and "speak medicine names" off.
- Choose the notification and lock-screen content: FULL, GENERIC or HIDDEN.
- Leave screenshot protection off or turn it on.
- Choose whether to add a photo to a medicine.
- Choose whether to export, where to save the file, and whether to delete it.

## Medical-device disclaimer

This app is not a medical device. It reminds and records; it does not replace your doctor, pharmacist or the leaflet that came with your medicine. It does not diagnose, treat, recommend or adjust doses, and it does not check interactions. If you are unsure about a dose, ask a healthcare professional.

## Changes to this policy

This policy is effective and last updated on 2026-10-27. If the app's data practices or this policy change, the published policy will be updated and its last-updated date will change. The date at the top identifies the current version.

## Contact

For questions about this policy or the app's privacy practices, contact [b4ck2life@gmail.com](mailto:b4ck2life@gmail.com).
