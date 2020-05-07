# workstation_config
A repository to keep track of various configuration files for my software tools. 

Work in progress. 

I've made this repository private as of now, I need to check out first that all
data included can be public


## Encrypting passwords/token with GPG

In order to avoid storing passwords/tokens in mutt config files you can encrypt
them with an active gpg key. It's well described
[here](https://pthree.org/2012/01/07/encrypted-mutt-imap-smtp-passwords/)
although in [here](https://gist.github.com/bnagy/8914f712f689cc01c267) some
minor objections about this method made. Both are worth a read.

Quick notes on gpg:
 * To generate gpg keys simply run:
   ```bash
   gpg --full-gen-ke
   ```
 * store a passphrase in keepassx.
 * use gpg-agent to cache passwords on active sessions,
   ```
   #~/.gnupg/gpg-agent.conf
   default-cache-ttl 3600
   ```
 * on Arch `gpg-agent` is controlled by
   ```bash
   systemctl --user start/status/etc gpg-agent.socket
   ```

## Changing authentication to OAuth 2

Neomutt has a [preliminary
support](https://neomutt.org/guide/optionalfeatures.html#oauth) for OAuth 2.
Step-by-step procedure is described
[here](https://luxing.im/mutt-integration-with-gmail-using-oauth/).

*Note: I am sitll not convinced what "protocolar" benefits are offered through
OAuth.*
