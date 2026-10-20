# VibeScript

VibeScript is a language for building web apps with AI coding assistants. One short `.vibe` file becomes a complete
app: screens, database, login, live updates and tests. The `vibe` command also checks the result in a real browser,
and scans it for security problems and EU-compliance issues (GDPR, cookies, accessibility, AI Act).

This repository only distributes the installable package. The source code is not public.

## Install

The download is password-protected. Ask the author for the password. Requires Node.js 22.13 or newer and `openssl`
(included on macOS and Linux; on Windows it comes with Git for Windows).

```sh
curl -LO https://github.com/tom-beeflow/vibescript/releases/download/v0.2.0-build141/vibescript-0.2.0.tgz.enc
openssl enc -d -aes-256-cbc -pbkdf2 -iter 600000 -in vibescript-0.2.0.tgz.enc -out vibescript-0.2.0.tgz
npm install -g ./vibescript-0.2.0.tgz
vibe --version
```

`openssl` asks for the password. Install from this file, not with `npm install vibescript`: the npm registry has an
unrelated package with that name.

## Quick start

```sh
vibe new myapp
cd myapp
vibe verify            # build, open every page in a browser, run the tests
vibe security          # security headers, cookies, TLS and a basic penetration test
vibe compliance        # GDPR/AVG, cookie consent, accessibility, AI Act transparency
```

`vibe new` writes a `CLAUDE.md`/`AGENTS.md` with the language reference for your AI assistant.
Run `vibe --help` for all commands and `vibe spec <topic>` for documentation on one topic.

## License

Use-only license: you may install and use VibeScript to build your own applications, but not redistribute it.
See [LICENSE](LICENSE).
