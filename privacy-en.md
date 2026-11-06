# Privacy Policy

*Version 0.1 · Effective 2026-11-07 · Requires macOS 15 or later*

Lectern does not collect personal data. The app has no network permission: its sandbox profile grants read access to files you select, and nothing else. There is no account, and no server for it to report to. Everything the app remembers stays on your Mac.

## What is not collected

None of the following is collected, transmitted, or sold:

- Your name, email address, or any account details. The app has no accounts.
- The contents of the PDFs you open, their file names, or their paths.
- Reading progress, bookmarks, notes, and search terms.
- Device identifiers, usage statistics, diagnostics, crash reports.
- Location, contacts, photos, camera, microphone.

The App Store privacy label for Lectern is **Data Not Collected**. It matches the code: no network requests, no analytics framework, no crash reporter, no third-party SDK.

## What Lectern writes on your Mac

To draw the bookshelf and to reopen a document at the page you left, the app writes one small file and a set of cover thumbnails inside its own sandbox container:

```
~/Library/Containers/com.lectern.reader/Data/Library/Application Support/Lectern/library.json
~/Library/Containers/com.lectern.reader/Data/Library/Application Support/Lectern/Covers/*.png
```

A self-built copy of the app that runs outside the sandbox writes to the folder one level up, `~/Library/Application Support/Lectern/`.

`library.json` holds one record per book:

| Stored | Why it is there |
|---|---|
| A random identifier | Matches a book to its cover file |
| A bookmark for the file | Reopens the document after you move or rename it |
| Title and author | Displayed on the shelf; both optional |
| Page count, file size | Shown in the book's details |
| Date added, last opened, last page | Sorts the shelf and restores your reading position |
| Favourite flag, collection name | Your own shelf organisation |

A cover thumbnail is a rendering of the document's first page, saved as `Covers/<identifier>.png`. If you add a document with a name or title you would rather not keep, delete it and the cover is deleted with it.

## Who can see this

Only you, and anyone with access to your Mac or your account folder. The data is not encrypted at rest, which is the same protection your documents have. A Time Machine backup includes these files; a Mac shared with others will show your shelf to anyone who opens it.

## Removing it

Removing a book from the shelf deletes its record and its cover thumbnail. Quitting and deleting the app, or moving its container folder to the Trash, removes everything the app has ever written. Nothing is left on a server, because nothing was ever sent to one.

## Children

Lectern is a document reader for adults, and collects nothing that would put it under children's privacy rules.

## Apple

If you buy Lectern through the App Store, that transaction, along with refunds and subscriptions, is handled by Apple under Apple's own terms and privacy policy.

## Changes

If this policy changes, the version and date at the top of this page change with it, and the new page ships in the next release.

## Contact

Questions about this policy: [[support email — to be filled]].

Written by [[your name — to be filled]].
