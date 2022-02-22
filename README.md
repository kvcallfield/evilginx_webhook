# evilginx_webhook
Adds a Slack webhook to evilginx

Instructions:

1) Swap this file in to your evilginx's core/ directory, replacing the old http_proxy.go
2) Find line 447 and change the fake Slack webhook url to match your valid webhook url
3) Go up to the evilginx/ directory
4) rm bin/evilginx; make
5) Before running evilginx you'll want to proxy the curl request to Slack through a seperate opsec-safe system, so run "nohup ssh -oStrictHostKeyChecking=no -N -D 43004 user@opsec_safe.com &"
6) You may want to sanity check that just a plain "ssh user@opsec_safe.com" doesn't ask to approve a new hostkey, etc
7) Run evilginx with the -debug option
8) Enjoy not having to stare at Evilginx output while you wait for a victim session!
