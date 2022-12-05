# moodle401-plugins


## Disable Notifications

```php
// Moodle configuration file
 
// Use the following flag to completely disable the installation of plugins
// (new plugins, available updates and missing dependencies) and related
// features (such as cancelling the plugin installation or upgrade) via the
// server administration web interface.
$CFG->disableupdateautodeploy = true;
// Disabling update notifications
$CFG->disableupdatenotifications = true;

// Some administration options allow setting the path to executable files. This can
// potentially cause a security risk. Set this option to true to disable editing
// those config settings via the web. They will need to be set explicitly in the
// config.php file
$CFG->preventexecpath = true;

// Force result of checks used to determine whether a site is considered "public" or not (such as for site registration).
$CFG->site_is_public = false;
```

## Plugins List

```bash
mkdir moodle
cd moodle
```





## Git commands

```bash
git submodule add -b branch https://urltoplugin.git path/to/submodule
git add .
git commit -m "Some update info here..."
git push
```

```bash
SUBMPATH="moodle/path/to/submodule"
git submodule deinit $SUBMPATH
git rm $SUBMPATH
git commit -m "Removed submodule $SUBMPATH"
rm -rf .git/modules/$SUBMPATH
git push
```



