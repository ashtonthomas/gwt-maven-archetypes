gwt-maven-archetypes
====================

This project contains Maven archetypes for modular GWT projects.

How to use
----------

In order to generate a modular GWT project from the available archetypes, first you need to clone and install this project locally:

    git clone https://github.com/tbroyer/gwt-maven-archetypes.git
    cd gwt-maven-archetypes && maven clean install

### Generate a project

    mvn archetype:generate \
       -DarchetypeGroupId=net.ltgt.gwt.archetypes \
       -DarchetypeArtifactId=<artifactId> \
       -DarchetypeVersion=1.0-SNAPSHOT

where the available `<artifactIds>` are:

* `modular-webapp`
* `modular-requestfactory`


### Start the development mode

Change directory to your generated project and issue the following commands:

1. `mvn clean package -Ddraft`
2. In one terminal window: `cd server && mvn jetty:start -Ddev`
3. In another terminal window: `cd client && mvn gwt:run -Ddev`
