teiid
=====

[![Build Status](https://travis-ci.org/teiid/teiid.svg?branch=master)](https://travis-ci.org/teiid/teiid-wildfly)
[![Join the chat at https://gitter.im/teiid](https://badges.gitter.im/teiid/teiid.svg)](https://gitter.im/teiid?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Teiid is a data virtualization system that allows applications to use data from multiple, heterogeneous data stores.

## Useful Links
- Website - http://teiid.org
- Latest Documentation - http://teiid.github.io/teiid-documents/master/content/
- Documentation Project - https://github.com/teiid/teiid-documents
- JIRA Issues -  https://issues.jboss.org/browse/TEIID
- User Forum - https://community.jboss.org/en/teiid?view=discussions
- Wiki - https://community.jboss.org/wiki/TheTeiidProject

## To build Teiid-Wildfly
- install JDK 1.8 or higher
- install maven 3.2+ - http://maven.apache.org/download.html
- Create a github account and fork teiid-wildfly

Enter the following:

	$ git clone https://github.com/<yourname>/teiid-wildfly.git
	$ cd teiid-wildfly
	$ mvn clean install -P dev -s settings.xml
	
you can find the deployment artifacts in the "teiid-wildfly/build/target" directory once the build is completed.

## Travis Builds

Teiid-wildfly includes a travis build config.  By default it performs only an "install" on every commit.  It allows for a
cron based build to be configured as well for deploying snapshots.  The snapshot build requires add the environment
variables SONATYPE_USERNAME and SONATYPE_PASSWORD that should set to the user access token values of an
authorized sonatype account.

## To start Teiid

Once built you can start up the Wildfly server with Teiid by extracting "build/target/teiid-<version>-wildfly-server.zip" and running:

	{server-dir}/bin/standalone.sh -c=standalone-teiid.xml

In order to be able to access the Wildfly console you need to setup a user by running "./bin/add-user.sh" or "bin/add-user.bat" from the server directory.

You should be able to access the Wildfly console at http://localhost:9990 and the Teiid console at http://localhost:9990/console/App.html#teiid.

For more info see [Installation Guide](http://teiid.github.io/teiid-documents/master/content/admin/Installation_Guide.html).

Licenses
-------

The default license for all submodules is the [Apache Software License (ASL) v2.0][1]

Where applicable individual submodules will provide additional copyright and license information.

[1]: view-source:https://www.apache.org/licenses/LICENSE-2.0
