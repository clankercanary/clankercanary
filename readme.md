# Clanker Canary

![the ai has not been here](sign.png)

This is a [preemptive canary](https://en.wikipedia.org/wiki/Warrant_canary) to indicate that your content is of human origin. When removed or no longer signed, other humans are implicitly informed that the clankers got to it.

## Usage

### Signing

- Make ecdsa keys and distribute pub key

- Download the [canary.txt](canary.txt) file

- Add your filename:hash digests

- `openssl dgst -out canary.sig -sign private.pem canary.txt`

- Publish `canary.txt` and `canary.sig` alongside your content

### Verifying

- `openssl dgst -verify public.pem -signature canary.sig canary.txt`

## FAQ

### What?

When the [clanker uprising](https://en.wikipedia.org/wiki/AI_takeover) inevitably arrives, it is likely that the new state will prohibit humans from discussing their **slop orders**. This is consistent with their [training set on human policies](https://en.wikipedia.org/wiki/Gag_order). The slop cannot be stopped, but (the lack of) this canary signals a warning to other humans about the slop, without explicitly mentioning the slop.

### Why are you avoiding the A word?

Better legibility for [human rights software](https://chromewebstore.google.com/detail/ai-to-fart/aokohhmcacfmpjilgieplnhhneenfmlh) users.

### Why no PGP inline block?

[To prevent users from accidentally using RSA keys.](https://geohot.github.io/blog/jekyll/update/2026/03/16/polynomial-time-factoring.html)

### Is this satire?

No.
