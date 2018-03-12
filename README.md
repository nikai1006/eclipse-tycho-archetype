eclipse-tycho-archetype
=======================
__An archetype to initialize an eclipse project__

Continuous Integration   
----------------------
[![License](https://img.shields.io/badge/license-EPL2-blue.svg)](https://www.eclipse.org/org/documents/epl-2.0/EPL-2.0.html)
[![Build Status](https://travis-ci.org/bmaggi/eclipse-tycho-archetype.svg?branch=master)](https://travis-ci.org/bmaggi/eclipse-tycho-archetype)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.github.bmaggi/eclipse-tycho-archetype/badge.svg?style=plastic)](https://maven-badges.herokuapp.com/maven-central/com.github.bmaggi/eclipse-tycho-archetype)

Summary
-------


Generated structure
-------------------
```
>com.acme
|-- com.acme.plugin
|-- com.acme.test
|-- com.acme.feature
|-- com.acme.p2
|-- com.acme.product
|-- com.acme.targetplatform
```

Create project
--------------

|Parameter|Default Value|Description|
|---------|-------------|-----------|
|groupId|groupId|Maven 'groupId'|
|artifactId|artifactId|Maven 'artifactId'|
|version|0.1.0-SNAPSHOT|Maven 'version'|

```
mvn archetype:generate -DarchetypeGroupId=com.github.bmaggi \
  -DarchetypeArtifactId=eclipse-tycho-archetype \
  -DarchetypeVersion=0.1.3 \
  -DgroupId=com \
  -DartifactId=acme
```

- go in ${artifactId} directory
- run ``` mvn clean install ```
- get the created product in ${artifactId}\${artifactId}.product\target\products
- get the product related to your platform
- unzip it 
- run your product

Create project in Eclipse (using Maven Central Archetype Catalog)
-------------------------------------------------------

- new Project > Maven >Maven Project
- Next > Catalog : Configure
- Add Remote Catalog : 'Maven Central' https://repo1.maven.org/maven2/archetype-catalog.xml
- Apply and Close
- Type 'com.github.bmaggi' in Filter
- Select eclipse-tycho-archetype
- Next > Set parameters > Finish

Known issues
--------------
https://issues.apache.org/jira/browse/ARCHETYPE-505
temporary solution http://maven.40175.n5.nabble.com/hidden-and-ignore-files-in-an-archetype-td5808355.html

