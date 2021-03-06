---
layout: post
title: "Automatic generation of random passwords during deployment"
category: core
tags: [core, deployment, configuration, password, random]
---
{% include JB/setup %}

[Mailing list post:](http://permalink.gmane.org/gmane.comp.security.openxpki.devel/121) 


	Martin Bartosch | 22 May 15:46

	Autogenerated passwords

	Hi,

	revision 883 implements feature request #1600234. Previously we were  
	distributing some default passwords in our configuration templates  
	which is obviously not the best way to go.

	This revision introduces an automatic password generation feature  
	that creates random 8 character passwords for each default user in  
	the standard installation. The corresponding passwords are printed  
	out to the console during the deployment step. In addition the  
	password authentication module now supports the RFC2307 schemes  
	'SHA', 'SSHA', 'MD5', 'SMD5', 'CRYPT'.

	It is recommended to use seeded SHA1 hashes (SSHA) for new  
	deployments that use simple passwords.

	Please note that I also changed the semantics of password storage,  
	the <algorithm/> tag is no longer required/supported. Instead the  
	password scheme is now encoded in RFC2307 format.

	To make existing configuration files compatible you can rewrite  
	auth.xml in the following way
	- remove <algorithm/> tags
	- expand existing SHA1 digests to include the {SHA} prefix (see below)

	Hint: In order to generate your own seeded SHA1 hashes you can also  
	use slappasswd -h "{SSHA}" -s "secret"

	Old syntax:
	     <user>
	       <name>root</name>
	       <algorithm>sha1</algorithm>
	       <digest>deadbeef...</digest>
	       <role>CA Operator</role>
	     </user>

	New syntax:
	     <user>
	       <name>root</name>
	       <digest>{SHA}deadbeef...</digest>
	       <role>CA Operator</role>
	     </user>

	cheers

	Martin
