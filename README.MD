ADBSS 
===========

ADBSS is a simple convenience shell script that uses adb to capture screenshots on an Android device and immediately transfer the files to the attached computer.

Usage
===========
<pre>
$ adbss [-s DeviceID]
</pre>

Screenshots are automatically named with a timestamp in YMD_HMS format (e.g. screen_2021-12-29_03-50-43.png) and downloaded to the current directory.

When only a single device is connected, `adbss` can be used by itself. If there are multiple devices, use the `-s` flag along with a device serial number to identify which device should be used. Use `adb devices -l` to see a list of serial numbers for connected devices.

Loop mode: When run normally, the script takes a single screenshot, then exits. If used with the `-l` flag, this mode allows the user to take multiple screenshots without repeatedly running the script. Each screenshot is taken with a press of the spacebar. To exit loop mode and the script, press the `q` key.

Note: Screenshot files are temporarily stored with the same filename at /sdcard/ on the device they're taken on. If something prevents files from being written there, the script will fail.

Requirements
------------

 * Current version of adb must be installed and included in your system or user path.
 * adbss must be executable - `chmod +x adbss`
 * [Optional] adbss should also be added to your path so it can be easily used from any location.

License
------------
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
