
Backports
---------
	x-caja-desktop fix for Petra and Maya


Mint 17
--------------------
	KDE: 
		The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
		also xfce, mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
		Consider not using oxygen for GTK (check with mintBackup filechooser)	
		mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
		missing mint-mdm-themes-kde
	xfce: 
		doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
		Can't use the trash in live mode
		There are no GTK bookmarks by default
		missing indicator-sound indicator-sound-gtk2

			
	Cinnamon/MATE:		
		unity-greeter pkg
		gedit-plugins pkg
		artwork: backgrounds
		artwork: mdm theme
		mintlocale missing ibus activation support
		https://github.com/linuxmint/mintmenu/pull/89				
		update translations for mintdrivers
		mozo doesn't start
		mate-shares-admin doesn't start
		mate-maximus is in autostart apps - it should be removed

	RFT:
		OK cinnamon has region and languages launcher
		OK improved offline installation of drivers (mintdrivers)
		OK pkexec fr and de translations in /usr/share/polkit-1/actions/com.ubuntu.pkexec.synaptic.policy
		OK cinnamon tooltips sometimes show at 0x0

	done
		mintwelcome redesign
		mintlocale
		mintmenu: panel applet transparency, multiple bug fixes
		hexchat replaces xchat
		mintupdate: handle kernel upgrades (show more info to advanced users)
		mintupdate: redesign, no need to elevate user to root to see updates
		mintupdate: redesign startup delay
		mintdesktop simplified UI, detects Marco
		mintsources: consider changing the way opt-in works for romeo and backport
		regenerate desktop files post-translations
		mint-x: MATE Panel transparency
		mdm shutdown sequence
		mdm recovery

	maintenance:
		reopen LMDE rsyncd

Cinnamon 2.2
---------------------------	 
	
	little things		
		right-click Run/Open with blah in nemo, on executable files		
		applets: Even after setting org.cinnamon.desktop.lockdown.disable-lock-screen to true, the lock button still appears on cinnamon menu applet…
		applets: Can't minimize windows which have a modal dialog (for example: Synaptic while installing a package). It's possible via the titlebar, but not via the window list
		prefs: I miss the working WIN+D keyboard shortcut to go to desktop.
		cinnamon: Onscreen keyboard activates when clicking the menu on the panel because text entry is focused... if onboard is used, entry should not focus when showing the menu 				
		cinnamon panel icon size sometimes show huge icons unless panel-scale-text-icons is set to true..
		cinnamon-settings-daemon sometimes crash when failing to mount and we dismiss the error dialog
		cinnamon hi-dpi autodetection gives false positives

	descoped:
		consider using bernard's theme
		show frequency in displays
		screenshot filenames aren't handy (Screenshot from 2014-02-17 14:46:32.png)
		Add common tiling options to window list context menu - Show Windows Side by Side, Cascade, Show windows stacked
		cinnamon-bluetooth: bring compatibility to GNOME 3.10
		cinnamon-settings-users: add support for nopasswdlogin
		expo: set overview mode to true by default
		expo: lag on dnd
		network applet https://git.gnome.org/browse/gnome-control-center/commit/panels/network?id=63756458b2de0d730763cc2acbd510659e4d00a5
		cinnamon-screensaver dialog is all shrunk in hi-dpi
		Can the upstream fix maybe be included in Mint somehow? Commit at upstream Gnome is https://git.gnome.org/browse/network-manager-applet/commit/?id=c798c40c5dce3bc6d9b615621cefe59660b5a504. 