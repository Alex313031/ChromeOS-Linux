# ChromeOS-Linux
Builds of linux-chromeos with codecs and build optimizations. Based off of my other repo, Thorium > https://github.com/Alex313031/Thorium
- linux-chromeos runs the ChromiumOS system UI within a X11 window on linux.

In general follow > https://chromium.googlesource.com/chromium/src/+/refs/heads/main/docs/chromeos_build_instructions.md#Chromium-OS-on-Linux-linux_chromeos

Use the args in the *args.gn* file as per > https://www.chromium.org/developers/gn-build-configuration
Copy .gclient to //chromium/ (not in //chromium/src/).

Set the PGO profile data with the command 'python tools/update_pgo_profiles.py --target=linux update --gs-url-base=chromium-optimization-profiles/pgo_profiles' and add the location of the *.profdata file at the end of args.gn.

Copy *BUILD.gn* to '$HOME/chromium/src/build/config/compiler/' and overwrite.

