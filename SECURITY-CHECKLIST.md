# Security Checklist Before Publishing

Everything in a public GitHub repository can be downloaded by anyone. Treat your portfolio folder as public before you push it.

## Quick Safe Publishing Checklist

Before you commit or push, check these places:

```txt
Config/userinformation.txt
Config/summary.txt
Config/productions.txt
Projects/
Projects/Photography/
Articles/
Resources/
```

## Do Not Commit These Unless You Intentionally Want Them Public

- Personal phone numbers.
- Home address or exact private location.
- Private email addresses you do not want online.
- Resume PDFs with phone, home address, birth date, or private references.
- Government IDs, school IDs, bank documents, invoices, contracts, or offer letters.
- Client work that is under NDA or not approved for public display.
- Raw photo originals with sensitive EXIF/GPS metadata.
- `.env` files.
- API keys, access tokens, passwords, private keys, or certificates.
- Large source files such as `.psd`, `.ai`, `.fig`, `.sketch`, or raw video files unless you truly want them public.

## Search For Personal Text

Use your editor search, or run commands like these:

```bash
rg -n -i "your real name|your email|your phone|your address|api key|token|password|secret"
```

Search for old placeholder names too. If you forked this from someone else, search for their name and links.

## Check Files By Type

Look for risky files before committing:

```bash
rg --files | rg -i "\.(pdf|docx|env|key|pem|p12|pfx|psd|ai|fig|sketch|zip)$"
```

## GEO And Metadata Are Public

`llms.txt`, `sitemap.xml`, `robots.txt`, and HTML meta tags are designed to be read by crawlers. Do not put private phone numbers, private addresses, hidden emails, client-confidential names, unpublished work, private document links, passwords, API keys, or secrets in those files.

## Photos And EXIF Metadata

Photos can contain camera, date, and sometimes GPS information. If privacy matters, export smaller web copies or strip metadata before adding photos.

Common safe workflow:

1. Keep original photos outside this repository.
2. Export web-size copies.
3. Remove metadata if needed.
4. Put only the web copies in `Projects/Photography/`.

## Git History Warning

Deleting a private file later does not automatically erase it from Git history. If you accidentally commit a secret or private file, rotate the secret and clean the repository history before pushing.

If you are unsure, stop and ask someone experienced before publishing.

## This Template Release Audit

This template release was prepared from a clean template history, not from a personal portfolio history. The release intentionally uses placeholder profile, project, photography, and article content.
