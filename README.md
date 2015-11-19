# TYPOTxSolrTry
Vagrant recipe to provsion a box with TYPO3 6.2.15 and 7.5.0 to try TYPO3 and tx_solr

How to start:

1. vagrant up

2. add to you hosts file:

192.168.144.120   6.2.15.local.typo3.org
192.168.144.120   7.6.0.local.typo3.org

3. Login into TYPO3 6.2.15 or 7.6.0:

http://6.2.15.local.typo3.org/typo3/
http://7.6.0.local.typo3.org/typo3/

Username: admin
Password: supersecret

4. Check solr:

ssh -NL 127.0.0.1:8081:127.0.0.1:8081 vagrant@6.2.15.local.typo3.org
ssh -NL 127.0.0.1:8082:127.0.0.1:8082 vagrant@7.6.0.local.typo3.org


