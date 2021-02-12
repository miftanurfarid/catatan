## Could not find path to the mlint executable in the configuration file

1. Open the User Settings by going to File > Preferences > Settings

2. On the right pane, where you have the settings.json file open, add to the json file.

		"matlab.mlintpath" : "/usr/local/Polyspace/R2020b/bin/glnxa64/mlint"

3. Save your settings.json file

4. Now, when you open a Matlab document (.m), VS Code displays warnings and errors.
