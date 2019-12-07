###  Adb uninstall failed


[android - adb uninstall failed - Stack Overflow](https://stackoverflow.com/questions/13534935/adb-uninstall-failed/17240552)


 

```shell
# gain shell access
$ adb shell

# check who you are
$ whoami
shell

# obtain user id
$ id
uid=2000(shell) gid=2000(shell)

# list packages
$ pm list packages | grep google                                                                                                                                                         
package:com.google.android.youtube
package:com.google.android.ext.services
package:com.google.android.googlequicksearchbox
package:com.google.android.onetimeinitializer
package:com.google.android.ext.shared
package:com.google.android.apps.docs.editors.sheets
package:com.google.android.configupdater
package:com.google.android.marvin.talkback
package:com.google.android.apps.tachyon
package:com.google.android.instantapps.supervisor
package:com.google.android.setupwizard
package:com.google.android.music
package:com.google.android.apps.docs
package:com.google.android.apps.maps
package:com.google.android.webview
package:com.google.android.syncadapters.contacts
package:com.google.android.packageinstaller
package:com.google.android.gm
package:com.google.android.gms
package:com.google.android.gsf
package:com.google.android.tts
package:com.google.android.partnersetup
package:com.google.android.videos
package:com.google.android.feedback
package:com.google.android.printservice.recommendation
package:com.google.android.apps.photos
package:com.google.android.syncadapters.calendar
package:com.google.android.gsf.login
package:com.google.android.backuptransport
package:com.google.android.inputmethod.latin

# uninstall gmail app
pm uninstall --user 0 com.google.android.gms
```
