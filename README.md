# ActivInspireAutoInstaller

The Activ Inspire Almost Intelligent Auto Installer (aiaiai.sh)

This is a truly awful script designed to automate the creation of custom .dmg packages for use with installPKGfromDMG.sh and Jamf Pro.

Requires:

1.  An ActivInspire .dmg file from Promethean (ActivInspire_XX_XX_mac.dmg) where XX_XX is the language code.
2.  A valid installer_choices.xml file (example included).

As one of the objectives of this script's intial deployment was to install the vendor package with the "Resources" choice unselected, the example installer_choices.xml file is configured as such. Simply change the 1s and 0s as desired.

Hopefully this helps someone who has the joy of deploying Promethean software without hindering them inappropriately.

**Use at your own risk** and copy to the left, to the left.

How to use:

1. Drop the Promethean .dmg into the `ActivInspireAutoInstaller` directory
2. cd to same
3. `./aiaiai.sh`
4. Drop the custom output .dmg into Jamf Admin
5. Configure policy with custom .dmg package set to **Cache** and `installPKGfromDMG.sh` set to **After**

Compatible installPKGfromDMG.sh available here - https://github.com/joeselway/jamfpro-scripts/blob/master/installPKGfromDMG.sh - with credit to @smashism and Blake Suggett via Jamf Nation.
