# ChromeOS-Linux
Builds of chromeos-linux with codecs and build optimizations.

In general follow https://chromium.googlesource.com/chromium/src/+/refs/heads/main/docs/chromeos_build_instructions.md#Chromium-OS-on-Linux-linux_chromeos

Use the args in args.gn i.e. https://www.chromium.org/developers/gn-build-configuration

Set the PGO profile data with the command 'python tools/update_pgo_profiles.py --target=linux update --gs-url-base=chromium-optimization-profiles/pgo_profiles'

Copy BUILD.gn to $HOME/chromium/src/build/config/compiler/ and overwrite.
