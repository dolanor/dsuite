# DSuite

Like your GSuite :envelope: :calendar: :file_folder: + :octocat: + CI, but on Docker :whale:

This contains work from these projects:

* [tomav/docker-mailserver](https://github.com/tomav/docker-mailserver)
* [mholt/caddy](https://github.com/mholt/caddy)
* [osixia/docker-openldap](https://github.com/osixia/docker-openldap)
* [osixia/docker-phpLDAPadmin](https://github.com/osixia/docker-phpLDAPadmin)
* [docker/distribution](https://github.com/docker/distribution/)
* [go-gitea/gitea](https://github.com/go-gitea/gitea)
* [drone/drone](https://github.com/drone/drone)
* [nextcloud/server](https://github.com/nextcloud/server)

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
