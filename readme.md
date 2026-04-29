# Clanker Canary

![the ai has not been here](sign.png)

This is a [preemptive canary](https://en.wikipedia.org/wiki/Warrant_canary) to indicate that your content is of human origin, which removal implicitly informs viewers that clankers got to it.

## Usage

### Creating and signing

- Make ecdsa keys and distribute pub key

- Download the [canary](canary.txt) text file

- Add your digest list

- `openssl dgst -out canary.sig -sign private.pem canary.txt`

- Publish `canary.txt` and `canary.sig`

### Verifying

- `openssl dgst -verify public.pem -signature canary.sig canary.txt`
