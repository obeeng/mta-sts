Oberon Engineering Pty Ltd
==========================

Misc DNS configuration documentation.

# Setup MTA-STS & TLS-RPT

Add the following two `TXT` records to the DNS Zone file:

```
_mta-sts.obeeng.com.au. 	14400 	TXT 	v=STSv1; id=1718959647
_smtp._tls.obeeng.com.au. 	14400 	TXT 	v=TLSRPTv1; rua=mailto:c8291de2@in.mailhardener.com
```

and the following `CNAME` record to the DNS Zone file:

```
mta-sts.obeeng.com.au. 	14400 	CNAME 	obeeng.github.io
```

That's it!

--
Author: Edward O'Callaghan.
