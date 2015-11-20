# TYPOTxSolrTry

Vagrant recipe to provsion a box with TYPO3 6.2.15 and 7.5.0 to try TYPO3 and tx_solr

## How to start

1. Run 

```bash
vagrant up
```

2. add to you hosts file (/etc/hosts):

```bash
192.168.144.120   6.2.15.local.typo3.org
192.168.144.120   7.6.0.local.typo3.org
```

3. Login into TYPO3 6.2.15 or 7.6.0:

* http://6.2.15.local.typo3.org/typo3/
* http://7.6.0.local.typo3.org/typo3/


Username: admin
Password: supersecret

Afterwards in the backend requeue all pages and re index and then check the frontend.


4. Check solr:

Create an ssh tunnel to your box:

```bash
ssh -NL 127.0.0.1:8081:127.0.0.1:8081 vagrant@6.2.15.local.typo3.org
ssh -NL 127.0.0.1:8082:127.0.0.1:8082 vagrant@7.6.0.local.typo3.org
```

ant then check:

localhost:8081

or

localhost:8082


## Thx

This box is based on and build with TYPO3.packer (https://github.com/Tuurlijk/TYPO3.Packer).
Thx to Michiel Roos for starting this.

This project was created by using my working time @dkd. If you want to support this join or
continue your sponsoring @ http://www.typo3-solr.com/en/sponsors/our-sponsors/


