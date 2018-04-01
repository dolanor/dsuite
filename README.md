# DSuite

Like your GSuite, but on Docker.

# Installation

```bash
git clone https://github.com/dolanor/dsuite
cd dsuite
# edit obvious placeholders (mydomain.com, dc=mydomain,dc=com, XXXPassword, etc…)
vim docker-compose.yml
# launch the services
docker-compose up -d
# sip a fine beverage in a nice chair
```

# Configuration

Obviously, you need to configure the docker-compose.yml to suit your needs. I might automate even more when I have time.

You also need to have a good DNS configuration, mostly for the mail part (spf, dkim, dmarc) and all the subdomains


## Open ports

I try to open as few ports as possible
There is:

* web: 80 and 443
* ssh for git remote access: 22
* mail: smtp (25, 465 (TLS), 587), imap (143, 993 (TLS)) (I didn't put POP, because I don't personally need it)

## Mail

For all the SPF, DKIM, DMARC configuration (which mostly need DNS entry modifications), go to the
[dockermail documentation](https://github.com/tomav/docker-mailserver/wiki)

## LDAP

TODO
