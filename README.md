# riff — releases

This repo exists only to host downloadable install packages for [riff](https://riff-site-chi.vercel.app). It has no source code — riff's source lives in a private repository.

## Install

Download the latest release tarball from the [Releases page](https://github.com/knaig/riff-releases/releases/latest), then:

```
npm install -g riff-<version>.tgz
riff config set openrouter <your-key>
riff room
```

Node 22+ required. `riff config set` also accepts `openai`, `deepseek`, `nvidia`, or `perplexity` — or skip it and open `riff room` → `/settings` in the browser. No key at all still works: the cast runs on a deterministic mock so you can see the room before spending anything.

## What's in each release

A packed npm tarball (`npm pack` output) — the compiled-equivalent install package, not a git checkout. No commit history, no internal docs, no issues.
