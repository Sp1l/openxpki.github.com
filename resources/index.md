---
layout: page
title: "Resources"
group: navigation
tags: [Resources]
category: Resources
---
{% include JB/setup %}


<ul class="nav nav-tabs">
<li class="active"><a href="index.html" data-toggle="tab">Recources</a></li>
<li><a href="wwwmirrors.html" data-toggle="tab">WWWMirrors</a></li>
<li><a href="links.html" data-toggle="tab">Links</a></li>
</ul>


<a href="http://www.sourceforge.net">
          <img src="http://www.sflogo.sourceforge.net/sflogo.php?group_id=150124"
               width="125" height="37" alt="SourceForge.net Logo"/>
</a>
<p>OpenXPKI is hosted on SourceForge.net and uses its services
	  for communication and project management.</p>
<ul>
<li><a href="http://www.sf.net/projects/openxpki/">
	      OpenXPKI at SourceForge</a></li>
<li><a href="http://www.sf.net/mail/?group_id=150124">
	      Mailing Lists</a></li>
<li><a href="http://www.sf.net/tracker/?group_id=150124">
	      Tracking system:</a>
<ul>
<li>Bugs</li>
<li>Support Requests</li>
<li>Patches</li>
<li>Feature Requests</li>
</ul>
</li>
<li><a href="http://www.sf.net/svn/?group_id=150124">
Subversion (SVN) Version Control System</a>. Main SVN repository of the OpenXPKI source code.</li>
<li><a href="http://www.openxpki.svn.sf.net/viewvc/openxpki/">
	      ViewVC</a>. Web viewer of the OpenXPKI's SVN repository. 
              Hosts at SourceForge. Updates with each commit.</li>
<!--
<li><a href="http://www7.openxpki.org/svn/openxpki">
	      WebSVN</a>. Another web viewer of the OpenXPKI's SVN repository. 
              With RSS feed. Hosts at www7. Updates every 10 min.</li>
-->
</ul>
<h2>Source code repository structure</h2>
<p>
	  OpenXPKI uses Subversion as its main revision control system.
	  The primary repository is hosted at SourceForge, containing
	  releases as well as bleeding edge development code.
          The directory structure is layed out as follows:</p>
<dl>
<dt class="sourcecode">/trunk/</dt>
  <dd><dl>
  <dt class="sourcecode">perl-modules/core/trunk/</dt>
    <dd>Server Core modules</dd>
  <dt class="sourcecode">clients/perl/</dt>
    <dd><dl>
    <dt class="sourcecode">OpenXPKI-Client/</dt>
      <dd>Base class for perl-based clients</dd>
    <dt class="sourcecode">OpenXPKI-Client-HTML-Mason/</dt>
      <dd>Web interface to a locally running OpenXPKI daemon</dd>
    <dt class="sourcecode">OpenXPKI-Client-SCEP/</dt>
      <dd>SCEP interface</dd>
    </dl></dd>
  <dt class="sourcecode">deployment/</dt>
    <dd>Deployment tools</dd>
  <dt class="sourcecode">i18n/</dt>
    <dd>Internationalization of the user interface</dd>
  <dt class="sourcecode">package/</dt>
    <dd><dl>
    <dt class="sourcecode">debian/</dt>
      <dd>Tools to build fresh Debian Linux package</dd>
    <dt class="sourcecode">freebsd/</dt>
      <dd>FreeBSD ports and tools to update them</dd>
    <dt class="sourcecode">suse/</dt>
      <dd>SuSE package creation tools</dd>
    </dl></dd>
  </dl></dd>
<dt class="sourcecode">/www.openxpki.org/trunk/</dt>
  <dd><dl>
  <dt class="sourcecode">src/</dt>
    <dd>Web site source code</dd>
  <dt class="sourcecode">htdocs/</dt>
    <dd>Static HTML generated from the source code (can directly be 
      published by a web server)</dd>
  <dt class="sourcecode">update_www_openxpki_org</dt>
    <dd>A script to update the web servers</dd>
  </dl></dd>
</dl>


<h2>Web Site Mirrors</h2>
<p>
  This web site is mirrored on several web servers across the world.
  You can find a 
  <a href="/resources/wwwmirrors.html">
    list of WWW Mirrors here
  </a>.
</p>
<h2>Wiki</h2>
<p>
  We also have a <a href="http://wiki.openxpki.org">Wiki</a> (hosted on www4), where the documentation effort takes place and everyone can contribute their knowledge.
</p>
