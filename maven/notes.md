## Maven notes

### Why maven
* our project depend on several 3rd party libraries. To download and add those libraries to our project we use maven
* library means jar file
* one jar file depend on another and another jar depend on some other
* another jar - dependency
* some other jar - transitive dependency
* we declare dependency in `pom.xml`

## From where depndencies download?
* Maven central repository - public repository maintained by maven team
* Remote repository
    * Maintained by companies
    * we need to give remote repo details in pom.xml if we have company specific dependencies
* Local repository
    * local machine `.m2` folder
    * all dependencies which already downloaded will be stored in local repository
* whenever we add dependency maven will check in the following order to get dependency
    * local repo
    * remote repo (if we specify any in pom.xml)
    * central repo
* some companies may block connecting to central repo due to security issues
    * In this case we may need to specify proxy details
    * proxy details we will sepcify in `settings.xml` file in local repo