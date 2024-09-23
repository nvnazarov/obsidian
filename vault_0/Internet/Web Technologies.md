## Internet

[How does the Internet work? - Learn web development | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work)
## DNS

Domain Name System

>The DNS was created because the original system for mapping names to address, the “hosts” file, was quickly becoming unsustainable.

Hosts file

Anycast addresses

gTLDs - generic TLDs (associated with a theme: com, edu, mil)
ccTLDs - country code TLDs

Root zone = `.`

- registrant
- registrar - works with the registry to create the NS records.
- registries - databases of DNS names under each TLDs. Each registry is operated by a different organization.
- ICANN - oversees Internet root zone, grants accreditation to registrars.

Domain names are leased (yearly), not outrighted.

[How DNS works. What is a DNS resolver and a DNS resolution?](https://howdns.works/ep1/)
[Website to IP Lookup (nslookup.io)](https://www.nslookup.io/learning/)

Web-server
Web-hosting [What Is Web Hosting? Explained (youtube.com)](https://www.youtube.com/watch?v=htbY9-yggB0)

```
%SystemRoot%\System32\drivers\etc\hosts
/etc/hosts
```

```powershell
ping <site>
nslookup <site>
dig <site>

nslookup -type=a <site>
```

DNSBL - DNS block list

## Web Server


Server push

## Virtual Networking

VPN
VLAN
VXLAN
