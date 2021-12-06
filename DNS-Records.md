# eNom DNS Records for TamaToledo.org

_eNom_ should now direct DNS to these records as of 5-Dec-2021.

| Host Name | Record Type | Address | Purpose |
| --- | --- | --- | --- |
| ~@~ | ~TXT~ | ~include:_spf.emfwd.name-services.com mx ?all~ | Removed 6-Dec-2021 |
| @ | CNAME | tama-toledo.github.io | Added 6-Dec-2021 |
| ~@~ | ~A~ | ~185.199.108.153~ | Removed 6-Dec-2021. DNS search returned better results with the CNAME record above.  See https://www.whatsmydns.net/#CNAME/tamatoledo.org |
| www | CNAME | tama-toledo.github.io. | Added 6-Dec-2021 just in case it's needed |
| imap | CNAME | mail.tamatoledo.org.cust.a.hostedemail.com. | Required for @tamatoledo.org email to RECEIVE |
| smtp | CNAME | mail.tamatoledo.org.cust.a.hostedemail.com. | Required for @tamatoledo.org email to SEND |
| webmail | CNAME | webmail.tamatoledo.org.cust.a.hostedemail.com. | Required for webmail.tamatoledo.org |
| _github-pages-challenge-tama-toledo | TXT | d6234d584dbcf6660999da8961918b | For GitHub custom domain verification at https://github.com/Tama-Toledo |

# DigitalOcean DNS Records for TamaToledo.org

These should no longer be active after 05-Dec-2021.

| Host Name | Record Type | Address | Purpose |
| --- | --- | --- | --- |
| stc-rec.tamatoledo.org | CNAME | stc-rec-tamatoledo-org-27ggp.ondigitalocean.app. | Points _stc-rec.tamatoledo.org to DO hosted static site |
| tamatoledo.org | CAA | digicert.com | For domain https certs |
| tamatoledo.org | CAA | letsencrypt.org | For domain https certs |
| tamatoledo.org | MX | mx.tamatoledo.org.cust.a.hostedemail.com. | For email to function |
| webmail.tamatoledo.org | CNAME | webmail.tamatoledo.org.cust.a.hostedemail.com. | For webmail to function |
| email.mg.summittservices.com.tamatoledo.org | CNAME | mailgun.org. | For MailGun to send @summittservices.com emails |
| mg.summittservices.com.tamatoledo.org | TXT | v=spf1 include:mailgun.org ~all | More for MailGun |
| mailo._domainkey.mg.summittservices.com.tamatoledo.org | TXT | k=rsa; p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQC5CkyYVjwV47VLrmxKgS3/5vSXHcKJUH0PI7xeYUf1cd63fMWRu9lE3QjF+rzr10Dnyl18NLMsyhJRJQ6xdTv/tTgRy/6pIEOxXcQfr8dsMIiyU77v4Tthep55ynEwzUR98Zjf05n311fSGVitaNhYUHCaUiOkbYB/+RzAmp1F3wIDAQAB |
| imap.tamatoledo.org | CNAME | mail.tamatoledo.org.cust.a.hostedemail.com. | To receive @tamatoledo.org emails |
| smtp.tamatoledo.org | CNAME | mail.tamatoledo.org.cust.a.hostedemail.com. | To send @tamatoledo.org emails |
| tamatoledo.org | NS | ns1.digitalocean.com. | Sets DO as DNS provider |
| tamatoledo.org | NS | ns2.digitalocean.com. | Sets DO as DNS provider |
| tamatoledo.org | NS | ns3.digitalocean.com. | Sets DO as DNS provider |

At 11:39 AM on 6-Dec-2021 I got the following support response from _DigitalOcean_:

```
Hi there,

Thank you for reaching out, and we'll be happy to point you in the right direction here. 

I understand that you are looking to backup your DNS zone for the domain tamatoledo.org as the domain is pointing towards the default registrar nameservers. Since the domain is not pointing towards the DigitalOcean nameservers so queries would not be answered by the DNS zone present on the cloud panel. Rather the queries will be answered by the DNS zone present on the registrar-side for this domain. 

Given the above scenario, the DNS records present on the DigitalOcen cloud panel will not be effective and you can safely remove them or keep the domain added on the cloud panel for future reference. 

If you have any other questions or concerns, please don't hesitate to let us know. We're always here and happy to help.

Swimmingly,
Mubashir
Developer Support Engineer
DigitalOcean
```
