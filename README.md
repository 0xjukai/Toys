# Add custom CA to system trusted CA

  Here is how to do it :https://code.google.com/p/android/issues/detail?id=32696#c5
  ```
  1 - add your cert normally, it will be stored in your personal store and android will ask you a pin/password... Proceed
  2 - With a file manager with root capabilities, browse files in /data/misc/keychain/cacerts-added. You should see a file here, it's the certificate you have added at step 1. If you can not find it in that path, look in /data/misc/user/0/cacerts-added/
  3 - Move this file to system/etc/security/cacerts (you will need to mount the system partition r/w)
  4 - Reboot the phone
  5 - You are now able to clear the pin/password you have set to unlock the device.
```
