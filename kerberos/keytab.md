# Below is how we create keytab file for sys_iahp account 
> A keytab is a file containing pairs of Kerberos principals and encrypted keys (which are derived from the Kerberos password). [link](https://kb.iu.edu/d/aumh) 

### Create Keytab
    - rm sys_iahp.keytab
    - ktutil
    - ktutil:  addent -password -p sys_iahp@AMR.CORP.KAMBINI.COM -k 1 -e rc4-hmac
    - Password for sys_iahp@AMR.CORP.KAMBINI.COM: xxxxxx 
    - ktutil:  wkt /home/sys_iahp/sys_iahp.keytab
    - ktutil:  quit
    - /bin/chmod go-rwx /home/sys_iahp/sys_iahp.keytab

### Test Keytab
	kdestroy 
	kinit -kt /home/sys_iahp/sys_iahp.keytab  sys_iahp@AMR.CORP.KAMBINI.COM
	klist -e