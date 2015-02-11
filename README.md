# key2debug
- - - - - - - - - - - -

Introduction
--------------------

key2debug is a small script used to transform any android keystore to debug
one. Which can be imported as custom debug key in Eclipse.

This is very usefull if you want to test your application agains keystore-dependent services during application development.
This way developers can be 100% sure that things like Google Maps and similar will work.

The script will __not__ overwrite the exiting keystore, it will create __new__
one, with .debug suffix.


Requirements
--------------------

* Any linux distribution.
* Installed and available keytool (commes with android SDK)
* You must also know
	* Passphrase of the key
	* Alias and its password


Usage
--------------------

#### With root access
1. Download the script to your /usr/bin folder
2. Type `chmod +x /usr/bin/key2debug`
3. Type `key2debug <path_to_the_keystore>`
4. When promprted, supply with passphrase, alias and its password


#### Without root access
1. Download the script to your system
2. Type `chmod +x /path/to/key2debug`
3. Type `/path/to/key2debug <path_to_the_keystore>`
4. When promprted, supply with passphrase, alias and its password


Applying custom debug keystore in eclipse
--------------------
1. Open eclipse
2. From the menu select Windows -> Prefenrences
3. From the left menu select Android -> Build
4. To the right of the __Custom debug keystore__ input field click on the__Browse__ button
5. Find the generated file and click OK
6. You are done, just close the window

To remove custom debug keystore, simply select and delete the __Custom debug keystore__ input field

Credits
--------------------
Script has been written by the [Intellex](http://intellex.rs/en) team.
