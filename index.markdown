---
layout:      default
title:       Binary packages for SmartOS/illumos, macOS, Linux, and NetBSD
metacontent: Binary dreckly package sets for SmartOS/illumos, macOS, Linux, and NetBSD.
---

<div class="container">
	<div class="row">
		<div class="col-md-4">
			<h3>Install Binary Packages</h3>
			<p>
				We provide the <code>pkgin</code> binary package manager with our bootstrap kits,
				making it easy to search for, install, and upgrade binary packages.  If you are used to
				<code>apt-get</code> or <code>yum</code> on Linux it should feel very familiar.
			</p>
		</div>
		<div class="col-md-4">
			<h3>Build From Source</h3>
			<p>
				If you prefer you can build packages from source, perhaps to use different package
				options or <code>CFLAGS</code>.  No problem!  One simple command automatically
				downloads, builds, and installs everything required - even dependencies!
			</p>
		</div>
		<div class="col-md-4">
			<h3>Create New Packages</h3>
			<p>
				If a package you want isn't available yet, it's easy to create it.  Packages are driven
				by a simple Makefile, tools are available to make creating new packages easy, and there
				is infrastructure built-in to handle many portability issues.
			</p>
		</div>
	</div>
	<div class="row">
		<div class="col-md-4">
{% highlight console %}
# pkgin -y upgrade
# pkgin search ffmpeg
ffmpeg6-6.1.1   Decoding, encoding and streaming software (v6.x)
ffmpeg7-7.0     Decoding, encoding and streaming software (v7.x)
# pkgin install ffmpeg7
{% endhighlight %}
		</div>
		<div class="col-md-4">
{% highlight console %}
# vi /opt/pkg/etc/mk.conf.local
PKG_OPTIONS.ffmpeg7+=   fdk-aac x265
CFLAGS+=                -O3
# cd dreckly/multimedia/ffmpeg7
# bmake install
{% endhighlight %}
		</div>
		<div class="col-md-4">
{% highlight console %}
# mkdir misc/foo
# cd misc/foo
# url2pkg http://si.te/foo-1.0.tar.gz
# vi Makefile
# bmake install
{% endhighlight %}
		</div>
	</div>
	<div class="row">
		<div class="col-md-3">
			<h3>SmartOS/Illumos</h3>
			<p>Our primary platform is SmartOS, but our packages are portable across illumos distributions.  They are built nightly from dreckly trunk for SmartOS, OmniOS, OpenIndiana, and Tribblix.</p>
		</div>
		<div class="col-md-3">
			<h3>macOS</h3>
			<p>For macOS we offer the latest packages built for Monterey or newer.  For those on older releases we have archived package sets built for Big Sur, Sierra, Mavericks, and 32-bit Snow Leopard.</p>
		</div>
		<div class="col-md-3">
			<h3>Linux</h3>
			<p>Our Linux packages are built on CentOS 6 and 7 for distributions based on RedHat Enterprise Linux.  They provide a useful companion to the default set of available RPM packages.</p>
		</div>
		<div class="col-md-3">
			<h3>NetBSD</h3>
			<p>We also offer daily builds of dreckly trunk for NetBSD 10.0/amd64.  They are provided for users and developers to run the latest packages without having to wait for the next branch.</p>
		</div>
	</div>
	<div class="row">
		<div class="col-md-3">
			<p><a class="btn btn-orange" href="/install-on-illumos/" role="button">Install on SmartOS/illumos &raquo;</a></p>
		</div>
		<div class="col-md-3">
			<p><a class="btn btn-orange" href="/install-on-macos/" role="button">Install on macOS &raquo;</a></p>
		</div>
		<div class="col-md-3">
			<p><a class="btn btn-orange" href="/install-on-linux/" role="button">Install on Linux &raquo;</a></p>
		</div>
		<div class="col-md-3">
			<p><a class="btn btn-orange" href="/install-on-netbsd/" role="button">Install on NetBSD &raquo;</a></p>
		</div>
	</div>
</div>
