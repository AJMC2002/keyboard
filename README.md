# keyboard
Custom keyboard layout based on The Primeagen's "Real Programmer's Dvorak" in Linux Mint.

Made as a variant of the Spanish Latin American layout, it gives a better access to common symbols used in programming.
Unlike The Primeagen's setup, it uses the QWERTY layout which, despite being slower in comparison to other layouts when typing, has more compatibility
at the moment of using keyboard shortcuts. Of course, shortcuts with special symbols probably will change but it's not as drastic as completely using another layout.

## Install
### Ubuntu
Before doing anything, please add another layout (the us one for example) in case something doesn't go right at the moment of configuration.
Also, the following instructions require you to open these files as super user with any editor you like (VSCode usually is problematic about using it as super user, so try with Vim or Nano).

Copy the `latam-prog` file's contents and paste them at the end of at the end of `/usr/share/x11/xkb/symbols/latam`.

Next, open `/usr/share/x11/xkb/rules/evdev.xml`, find where it says latam and add the Latin American Programmer variant as one of the variants.
It should look something like this:

```xml
<layout>
  <configItem>
    <name>latam</name>
    ...
  </configItem>
  <variantList>
    <variant>
      <configItem>
        <name>latam-prog</name>
        <description>Spanish (Latin American, Programmer)</description>
      </configItem>
    </variant>
  </variantList>
```
