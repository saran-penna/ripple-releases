# Ripple for macOS

Official binary downloads and release notes for Ripple.

Ripple is a private-source, local-first clipboard, file shelf, and dictation
utility for macOS 26 Tahoe. This public repository intentionally contains no
application source code.

## Download

Download the latest disk image from [Releases](https://github.com/saran-penna/ripple-releases/releases), drag
**Ripple.app** into `/Applications`, and open it.

The current 0.4.0 build is a public preview signed with an Apple Development
certificate, not a notarized production build. On first launch, macOS will block
it. Choose **Done**, then open **System Settings → Privacy & Security**, scroll
to Security, and choose **Open Anyway**. This exception is required once.

## Ripple 0.4.0

### Meta Muse Voice Transcribe

- Select Muse in **Settings → Transcription** or from the dictation HUD.
- Store and test your own Meta Model API key in the macOS Keychain.
- Receive live partial transcripts with keyword biasing from Ripple's dictation
  dictionary.
- Request Meta Zero Data Retention for every Muse session.
- Fall back to Apple Speech if Meta cannot start.

The release passed a real Meta file-transcription request, a real realtime
WebSocket handshake, and the complete macOS suite: 409 tests, zero failures.

## Privacy

Clipboard history, files, OCR, and local transcription stay on the Mac. Google
Gemini and Meta Muse are optional: audio leaves the Mac only while the owner has
explicitly selected that cloud engine and supplied its API key. Ripple contains
no telemetry and never logs clipboard payloads, microphone audio, API keys, or
transcript contents.

## Requirements

- macOS 26 Tahoe
- Accessibility permission for global shortcuts and paste-back
- Microphone permission only for dictation
