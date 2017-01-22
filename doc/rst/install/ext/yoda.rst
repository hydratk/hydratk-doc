.. install_ext_yoda:

Yoda
====

You have 2 options how to install Yoda extension.

Package
^^^^^^^

Install it via Python package managers PIP or easy_install.

Filename after PIP download contains version, adapt sample code.

  .. code-block:: bash
  
     $ sudo pip download hydratk-ext-yoda
     $ sudo pip install hydratk-ext-yoda.tar.gz 
     
  .. code-block:: bash
  
     $ sudo easy_install hydratk-ext-yoda
     
  .. note::
  
     Use PIP to install package from local file for correct installation.
     When installed from remote repository, PIP sometimes doesn't call setup.py.       

Source
^^^^^^

Download the source code from GitHub or PyPi and install it manually.
Full PyPi URL contains MD5 hash, adapt sample code.

  .. code-block:: bash
  
     $ git clone https://github.com/hydratk/hydratk-ext-yoda.git
     $ cd ./hydratk-ext-yoda
     $ sudo python setup.py install
     
  .. code-block:: bash
  
     $ wget https://python.org/pypi/hydratk-ext-yoda -O hydratk-ext-yoda.tar.gz
     $ tar -xf hydratk-ext-yoda.tar.gz
     $ cd ./hydratk-ext-yoda
     $ sudo python setup.py install
     
  .. note::
  
     Source is distributed with Sphinx (not installed automatically) documentation in directory doc. 
     Type make html to build local documentation however is it recommended to use up to date online documentation.     
     
Requirements
^^^^^^^^^^^^     
     
Several python modules are used.
These modules will be installed automatically, if not installed yet.

* hydratk
* lxml
* pytz
* simplejson

Module lxml requires several libraries which will be installed via Linux package managers, if not installed yet.

lxml

* apt-get: python-lxml, libxml2-dev, libxslt1-dev
* yum: python-lxml, libxml2-devel, libxslt-devel   
     
Installation
^^^^^^^^^^^^

See installation example, Python 2.7.

  .. code-block:: bash
  
     **************************************
     *     Running pre-install tasks      *
     **************************************

     *** Running task: install_libs_from_repo ***

     Installing package python-lxml
     Installing package libxml2-devel
     Installing package libxslt-devel

     *** Running task: install_pip ***

     Installing module hydratk
     Requirement already satisfied: hydratk in /usr/lib/python2.7/site-packages/hydratk-0.4.0-py2.7.egg
     Installing module lxml>=3.3.3
     Installing module pytz>=2016.6.1
     Installing module simplejson>=3.8.2
     
     running install
     running bdist_egg
     running egg_info
     creating src/hydratk_ext_yoda.egg-info
     writing src/hydratk_ext_yoda.egg-info/PKG-INFO
     writing top-level names to src/hydratk_ext_yoda.egg-info/top_level.txt
     writing dependency_links to src/hydratk_ext_yoda.egg-info/dependency_links.txt
     writing entry points to src/hydratk_ext_yoda.egg-info/entry_points.txt
     writing manifest file 'src/hydratk_ext_yoda.egg-info/SOURCES.txt'
     reading manifest file 'src/hydratk_ext_yoda.egg-info/SOURCES.txt'
     reading manifest template 'MANIFEST.in'
     writing manifest file 'src/hydratk_ext_yoda.egg-info/SOURCES.txt'
     installing library code to build/bdist.linux-x86_64/egg
     running install_lib
     running build_py
     creating build

     creating build/bdist.linux-x86_64/egg/EGG-INFO
     copying src/hydratk_ext_yoda.egg-info/PKG-INFO -> build/bdist.linux-x86_64/egg/EGG-INFO
     copying src/hydratk_ext_yoda.egg-info/SOURCES.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
     copying src/hydratk_ext_yoda.egg-info/dependency_links.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
     copying src/hydratk_ext_yoda.egg-info/entry_points.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
     copying src/hydratk_ext_yoda.egg-info/not-zip-safe -> build/bdist.linux-x86_64/egg/EGG-INFO
     copying src/hydratk_ext_yoda.egg-info/top_level.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
     creating dist
     creating 'dist/hydratk_ext_yoda-0.2.2-py2.7.egg' and adding 'build/bdist.linux-x86_64/egg' to it
     removing 'build/bdist.linux-x86_64/egg' (and everything under it)
     Processing hydratk_ext_yoda-0.2.2-py2.7.egg
     creating /usr/lib/python2.7/site-packages/hydratk_ext_yoda-0.2.2-py2.7.egg
     Extracting hydratk_ext_yoda-0.2.2-py2.7.egg to /usr/lib/python2.7/site-packages
     Adding hydratk-ext-yoda 0.2.2 to easy-install.pth file
     Installing yoda script to /usr/bin

     Installed /usr/lib/python2.7/site-packages/hydratk_ext_yoda-0.2.2-py2.7.egg
     Processing dependencies for hydratk-ext-yoda==0.2.2
     Finished processing dependencies for hydratk-ext-yoda==0.2.2
    
     **************************************
     *     Running post-install tasks     *
     **************************************

     *** Running task: copy_files ***

     Creating directory /etc/hydratk/conf.d
     Copying file etc/hydratk/conf.d/hydratk-ext-yoda.conf to /etc/hydratk/conf.d
     Creating directory /var/local/hydratk/yoda/db_testdata
     Copying file var/local/hydratk/yoda/db_testdata/db_struct.sql to /var/local/hydratk/yoda/db_testdata
     Creating directory /var/local/hydratk/yoda/lib/yodalib
     Copying file var/local/hydratk/yoda/lib/yodalib/__init__.py to /var/local/hydratk/yoda/lib/yodalib
     Creating directory /var/local/hydratk/yoda/yoda-tests/test1
     Copying file var/local/hydratk/yoda/yoda-tests/test1/example1.yoda to /var/local/hydratk/yoda/yoda-tests/test1
     Creating directory /var/local/hydratk/yoda/helpers/yodahelpers
     Copying file var/local/hydratk/yoda/helpers/yodahelpers/__init__.py to /var/local/hydratk/yoda/helpers/yodahelpers
     Copying file var/local/hydratk/yoda/db_testdata/db_data.sql to /var/local/hydratk/yoda/db_testdata

     *** Running task: set_access_rights ***

     Setting rights a+rwx for /var/local/hydratk
     Setting rights a+r for /etc/hydratk

     *** Running task: install_manpage ***


     *** Running task: install_db_testdata *** (takes longer time)

     Creating testdata database with dsn: sqlite:/var/local/hydratk/yoda/db_testdata/testdata.db3
     

Application installs following (paths depend on your OS configuration)

* yoda command in /usr/local/bin/yoda
* modules in /usr/local/lib/python2.7/dist-packages/hydratk-ext-yoda-0.2.2-py2.7egg
* configuration file in /etc/hydratk/conf.d/hydratk-ext-yoda.conf 
* application folder in /var/local/hydratk/yoda
       
Run
^^^

When installation is finished you can run the application.

Check hydratk-ext-yoda module is installed.

  .. code-block:: bash
  
     $ pip list | grep hydratk-ext-yoda
     
     hydratk-ext-yoda (0.2.2)
    
Check installed extensions

  .. code-block:: bash
  
     $ htk list-extensions
     
     Yoda: Yoda v0.2.2 (c) [2014 - 2016 Petr Czaderna <pc@hydratk.org>, HydraTK team <team@hydratk.org>]
     
Type command htk help and detailed info is displayed.
Type man yoda to display manual page. 

  .. code-block:: bash
  
     $ htk help
     
     Commands:
        yoda-create-test-results-db - creates database for storing test results base on specified dsn configuration
           Options:
              --yoda-db-results-dsn <dsn> - test results database access definition

        yoda-create-testdata-db - creates database for test data
           Options:
              --yoda-db-testdata-dsn <dsn> - test data database access definition

        yoda-run - starts the Yoda tester
           Options:
              --yoda-db-results-dsn <dsn> - test results database access definition
              --yoda-test-path <path> - test scenario path
              --yoda-test-repo-root-dir <path> - test repository root directory
              --yoda-test-results-output-create <state> - activates/deactivates native test results output handler
              --yoda-test-run-name <name> - test run identification
              -a, --yoda-test-results-output-handler <type> - set the test results output handler type

        yoda-simul - starts the Yoda tester in test simulation mode
           Options:
              --yoda-db-results-dsn <dsn> - test results database access definition
              --yoda-test-path <path> - test scenario path
              --yoda-test-repo-root-dir <path> - test repository root directory
              --yoda-test-results-output-create <state> - activates/deactivates native test results output handler
              --yoda-test-run-name <name> - test run identification
              -a, --yoda-test-results-output-handler <type> - set the test results output handler type

                  
You can run Yoda also in standalone mode.

  .. code-block:: bash
  
     $ yoda help
     
     Yoda v0.2.2
     (c) 2014 - 2016 Petr Czaderna <pc@hydratk.org>, HydraTK team <team@hydratk.org>
     Usage: yoda [options] command

     Commands:
        create-test-results-db - creates database for storing test results base on specified dsn configuration
           Options:
              --db-results-dsn <dsn> - test results database access definition

        create-testdata-db - creates database for test data
           Options:
              --db-testdata-dsn <dsn> - test data database access definition

        help - prints help
        run - starts the Yoda tester
           Options:
              --db-results-dsn <dsn> - test results database access definition
              -oc, --test-results-output-create <state> - activates/deactivates native test results output handler
              -oh, --test-results-output-handler <type> - set the test results output handler type
              -tn, --test-run-name <name> - test run identification
              -tp, --test-path <path> - test scenario path
              -tr, --test-repo-root-dir <path> - test repository root directory

        simul - starts the Yoda tester in test simulation mode
           Options:
              --db-results-dsn <dsn> - test results database access definition
              -oc, --test-results-output-create <state> - activates/deactivates native test results output handler
              -oh, --test-results-output-handler <type> - set the test results output handler type
              -tn, --test-run-name <name> - test run identification
              -tp, --test-path <path> - test scenario path
              -tr, --test-repo-root-dir <path> - test repository root directory

     Global Options:
        -c, --config <file> - reads the alternate configuration file
        -d, --debug <level> - debug turned on with specified level > 0
        -e, --debug-channel <channel number, ..> - debug channel filter turned on
        -f, --force - enforces command
        -i, --interactive - turns on interactive mode
        -l, --language <language> - sets the text output language, the list of available languages is specified in the docs
        -m, --run-mode <mode> - sets the running mode, the list of available modes is specified in the docs
                                         
Upgrade
=======

Use same procedure as for installation. Command options --upgrade (pip, easy_install) or --force (setup.py) are not necessary.
If configuration file differs from default settings the file is backuped (extension _old) and replaced by default. Adapt the configuration if needed.

Uninstall
=========    

Run command htkuninstall yoda.                                            