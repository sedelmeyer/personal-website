---
layout: post
title: "Upgrade Your Aging Unibody MacBook Pro (circa 2009-2011) with a New SSD"
date: 2017-12-11
categories: apple tech tutorial
---

__Outlined below is my preferred method for swapping out a circa 2009-2011 13-inch Unibody MacBook Pro's aging hard-disk drive (HDD) with a new solid-state drive (SDD).__ While there are a number websites that provide instructions for performing this task, I've found that none follow the exact process that I've come to prefer. This installation tutorial will require absolutely no third-party software and it is written with the assumption that you are performing a clean install of Apple's OS X 10.11 El Capitan operating system onto the new SSD. These instructions also assume that your old HDD is still functioning and that you are swapping out the drive primarily for the performance benefits of switching to an SSD.

[Jump to the Installation Instructions](#drive-replacement-instructions)

# Background

Over this past year, I've upgraded storage drives in two Unibody MacBook Pro laptops. The first was my early-2011 13-inch MacBook Pro (Model 8,1) and the second was my wife's mid-2009 13-inch MacBook Pro (Model 5,5). If you have an aging [second-generation "Unibody" MacBook Pro](https://en.wikipedia.org/wiki/MacBook_Pro#Second_generation_(Unibody)), chances are it has served you well. Chances are you have also run into the performance limitations of its slow internal HDD. Replacing the HDD with an SSD will likely be [the biggest performance boost you can give this machine](https://www.pcworld.com/article/2048120/benchmarks-dont-lie-ssd-upgrades-deliver-huge-performance-gains.html). As for my machines, both were frustratingly slow when booting or performing any read/write intensive task. On top of that, I was ready to update both systems with a clean install of OS X 10.11.6 El Capitan. Considering that their HDDs had been spinning for six and eight years respectively, [I figured it may be time to swap them out lest they fail me sometime soon](https://www.extremetech.com/computing/170748-how-long-do-hard-drives-actually-live-for). I was sold on the idea when I realized the performance boost I'd likely receive by swapping them with SSDs.

I chose to upgrade the aging HDD in each laptop with a new [525GB Crucial MX300 SSD](http://www.crucial.com/usa/en/storage-ssd-mx300). I purchased each of these SSDs for approximately $130. Now, after swapping out drives, both of these MacBook Pros boot in seconds and perform light-years better than they did even when purchased new close to a decade ago. This solution was far less expensive than spending $1000+ on a new high-end laptop. Even better, this solution still provided me all of the [dopamine fueled goodness I'd feel if I had purchased a new computer](https://www.wsj.com/articles/SB113382650575214543). Only the aging batteries (which I plan to replace soon) and the unibody exteriors of these two MacBooks give away their age.

I am pleased to say that I still use the early-2011 model as my primary machine and feel no desire trade it in for something newer. I hope to get at least two to three more years of useful life out of these Unibody MacBook Pros, barring some mechanical failure that can't be easily or affordably fixed.

# Should You Upgrade RAM Too?

If you also run memory intensive applications and find that you often max out your random-access memory (RAM), you could also consider upgrading your RAM to give yourself some additional overhead for multi-tasking. Personally, I chose to upgrade the RAM in my early-2011 MacBook Pro. I replaced my stock 4GB of RAM (2 x 2GB 1333MHz DDR3) with [8GB (2 x 4GB 1333MHz DDR3) of RAM purchased for  approximately $69 from Other World Computing (OWC)](https://eshop.macsales.com/item/Other%20World%20Computing/1333DDR38S08/). It worked wonderfully for this machine and my day-to-day use of it. As for my wife's mid-2009 machine, its stock configuration with 4GB of RAM (2 x 2GB 1066MHz DDR3) was plenty for our day-to-day use of that machine, which we use primarily for online streaming, web-browsing, word processing, and other "lightweight" tasks. So, I had no compelling reason to spend any additional money on RAM for it. The SSD replacement alone was all that it needed.

If you're wondering if you might need any additional RAM, or you're wondering how much RAM is right for you, this [ExtremeTech.com article](https://www.extremetech.com/gaming/222483-how-much-ram-do-you-need-should-you-upgrade-it-and-will-it-speed-up-your-pc) is a good place to start. If you do decide to upgrade the RAM on your laptop, check out OWC's online installation instructions, they're top notch: <https://eshop.macsales.com/installvideos/macbookpro_13_unibody_early11/>

# Drive Replacement Instructions

- [Items You Will Need](#items-you-will-need)
- [Part Zero: Back Up Your Data](#part-zero)
- [Part One: Create Your Bootable USB Install Drive](#part-one)
- [Part Two: Reformat Your SSD and Install Your New Operating System Onto It](#part-two)
- [Part Three: Remove and Replace Your Internal HDD with the SSD](#part-three)
- [Part Four: Configure Your "Like New" MacBook Pro](#part-four)

__DISCLAIMER:__ _This process worked for me. However, I make no guarantees that it will work for you. Do a little research up front to confirm the compatibility of any SSD that you buy. [Other World Computing's](https://www.macsales.com/) and [Crucial's](http://www.crucial.com/) websites provide useful compatibility look-up tools when shopping for components. Also, be certain to check the hardware requirements of any version of Apple's operating systems that you choose to install to ensure it is compatible with your laptop's specs, model, and year. That being said, proceed at your own risk. Your mileage may vary._

# Items You Will Need
[Return to Table of Contents](#drive-replacement-instructions)

1. __Your trusty Unibody 13-inch MacBook Pro, circa 2009-2011__ (This is by far my favorite Apple product ever.)

1. __A New 2.5-inch Solid-state Drive__ (I've been pleased with [my Crucial MX300 525GB SSDs](http://www.crucial.com/usa/en/storage-ssd-mx300).)

1. __An External Drive Enclosure with USB cable__ (Any [cheap model](http://a.co/2QhFS9O) should work.)

1. __An 8GB USB Flash Drive__ (We'll use this for creating a bootable "install" version of Apple's El Capitan operating system.)

1. __A Phillips #00 and a T6 Torx Screwdriver__ (Other World Computing sells [a cheap and durable basic toolkit](https://eshop.macsales.com/item/OWC/TOOLKITMHD/).)

1. __A Small Bowl__ (You'll want this to temporarily store your laptop screws so you don't loose them.)

1. __A Couple Hours To Spend Performing the Installation Process__

# Part Zero
### Back Up Your Data To a Safe Location
[Return to Table of Contents](#drive-replacement-instructions)

If you don't already use Time Machine to backup your Apple laptop on a regular basis, I suggest you start doing so now. If anything goes wrong that results in you losing all of your data now or anytime in the future, you'll wish you had. Trust me. This happened to me on a two-and-a-half-year-old iBook G4 in early-2007. To this day I wish I still had the digital photos that were lost on that drive. Needless to say, it only happened to me once. From then on I made certain to maintain regular redundant (multiple) backups of all my data.

I am not going to cover the specifics of how to perform and manage your backup regimen in these instructions. I'll just assume you already do this and that you have a solid backup and recovery strategy for all of your personal data. If not, a good place to start is by reading up on the "3-2-1" backup principle [(see my footnotes at the end of this article for more detail)](#footnotes) and implement some version of it that works for you.

__So, what I'm trying to say is, prior to starting this SSD installation process, be certain to make a fresh backup of all the data currently on your laptop in case you inadvertently lose everything on your current hard drive.__

# Part One
#### Create a Bootable Version of Apple's Operating System Install File on your 8GB USB Drive
[Return to Table of Contents](#drive-replacement-instructions)

Personally, I chose to install [OS X 10.11.6 El Capitan](https://en.wikipedia.org/wiki/OS_X_El_Capitan) onto my new SSD. If your Unibody MacBook Pro was produced in 2010 or later, you should be able to get away with installing macOS 10.12 Sierra or 10.13 High Sierra. Personally, I'm sticking with El Capitan until it is no longer supported by Apple. Besides, El Capitan is the newest and only supported version of Apple's operating system [even capable of running on a mid-2009 MacBook Pro (Model 5,5)](https://arstechnica.com/gadgets/2016/06/psa-macos-sierra-drops-support-for-many-macs-from-2007-2008-and-2009/). As of my writing these instructions El Capitan is still supported by Apple with regular security updates. My suspicion is that support for El Capitan will cease sometime in late 2018. Whether or not Apple continues to provide download access to El Capitan after it goes "end-of-support" is yet to be seen.

My recommendation is to check the hardware requirements for any Apple OS you hope to install to ensure that your specific model MacBook Pro is supported. Here are the requirements for El Capitan: <https://support.apple.com/kb/sp728?locale=en_US>

#### 1.1. Download OS X 10.11.6 El Capitan

  1. Apple provides a download link (As of my writing this in December 2017) to OS X 10.11.6 El Capitan at this URL: <https://support.apple.com/en-us/HT206886>.

  1. Follow instructions and links on that page to download El Capitan to your laptop.

  1. Once your download is complete, the OS X installer will open. You do not want to proceed with installation yet, so __quit the installer__.

#### 1.2. Transform Your Downloaded OS X File Into a Bootable Image and Transfer It To Your 8GB USB Drive

_This step involves using your Mac's built-in [Terminal application](https://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/). If you're not familiar with or comfortable with command line applications, fret not. Apple provides very clear step-by-step operations on how to do this._

  1. Ensure that the OS X El Capitan download file is currently located in your Applications folder and proceed to the instructions provided by Apple at this URL: <https://support.apple.com/en-us/HT201372>

  1. You need only to concern yourself with the instructions listed in the section titled __"Then use the 'createinstallmedia' command in Terminal"__...

      1. Mount your 8GB USB drive to your computer.

      1. Open the Terminal application, which you can find in the "Utilities" sub-folder within your "Applications" folder.

      1. Copy and paste the following command into your Terminal command line:
```sh
    sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app
```

      1. Hit the `Return` key.

      1. When prompted, type your administrator password and press `Return` again. (Note that terminal won't show any characters as you type your password. This is normal.)

      1. When prompted, type `Y` to confirm that you want to erase the volume, then press `Return`. (Terminal will now show its progress as the bootable installer is created.)

      1. Quit Terminal when done. __Your bootable installer USB drive is now ready to use!__

__Note:__ Apple's instructions insist that you need a 12GB USB drive to store your new bootable operating system. For OS X 10.11 El Capitan, an 8GB USB drive will suffice.

# Part Two
#### Prepare Your New SSD by Reformatting It and Installing the Apple Operating System Onto It
[Return to Table of Contents](#drive-replacement-instructions)

_You can leave your USB drive mounted to your laptop as you follow these next steps. You'll need it attached to your laptop soon enough._

#### 2.1. Reformat your new SSD

  1. Using your external drive enclosure with USB cable, connect your new blank SSD to your laptop via your second USB port.

  1. Open the Disk Utility application which is located in the "Utilities" folder within your "Applications" folder.

  1. Click on the icon for your new SSD in the left-hand window of Disk Utility (be careful not to select your internal Macintosh HD [or the USB drive if it is still attached to your laptop], otherwise you'll risk erasing the wrong drive during the next step).

  1. Select the "Erase" option, change the name of your new SSD to "Macintosh HD", select the "OS X Extended (Journaled)" format option, and select the "GUID Partition Map" scheme.

  1. Hit the "Erase" button, wait for the process to run, and then you should be all set with a properly formatted SSD onto which you can install El Capitan.

#### 2.2 Install OS X El Capitan onto your new SSD

  1. Now, with your newly reformatted SSD and your newly created USB El Capitan install drive both connected to your laptop at the same time, you need to restart your laptop and boot from your connected El Capital Install USB drive.

  1. To do this, select "Restart..." from your Apple menu, and as soon as it shuts down press and hold the `Option/Alt` key through the entire restart process.

  1. When prompted to select the device from which you'd like to boot, select the El Capital install volume.

  1. After agreeing to the Apple license agreement, you will then be presented with an "Install OS X" screen and the installer will ask you to select the drive on which to install El Capitan. Select your newly reformatted external SSD named "Macintosh HD". (Be careful not to accidentally select your laptop's internal HDD, which is probably also called "Macintosh HD"!)

  1. Once the El Capitan operating system is installed on your SSD, you will be presented with the "Select your language" screen. Do not select anything. Instead, hold down your laptop's power button for a few seconds to force it to shut down. You do not want to configure your SSD's new OS settings until the SSD has actually been installed inside our laptop.

  1. Once your laptop has shut down, press the power button again to restart it while also holding down the `Option/Alt` key until you are again presented with the screen asking you to select a boot device.

  1. Select your internal HDD to boot your laptop as it would normally boot.

  1. Once your laptop is booted, eject both your new SSD and your USB drive, then detach them both from your laptop.

  1. Now shut down your laptop. You'll need it powered off and unplugged before proceeding to Part Four of these instructions.

# Part Three
#### Remove Your Old HDD and Replace it with Your New SSD
[Return to Table of Contents](#drive-replacement-instructions)

This is the fun part where you get to take apart your laptop and swap out your old HDD with your new SSD. Other people have created far better photo- and video-based tutorials for doing this than I have any desire to create. So, instead of providing detailed process photos here, I am simply going to provide a link to Other World Computing's Video Tutorial: <https://eshop.macsales.com/installvideos/macbookpro_13_unibody_early11_hd/>

Watch that video. Basically, it shows that you want to use your Philips #00 screwdriver and T6 Torx screwdriver to:

  1. Remove the bottom panel off of your Unibody MacBook Pro. (Place your screws someplace safe so you don't lose any!)

  1. Remove the plastic bracket holding your HDD in place.

  1. Remove and unplug your HDD.

  1. Remove the four torx screws from the outside edges of your HDD.

  1. Attached the four torx screws, following the same configuration, to the outside edges of your SSD.

  1. Plug in your SSD and set it inside your laptop so that it is oriented the same way in which your HDD was originally oriented.

  1. Reattach the plastic holding bracket to secure your SSD.

  1. Reattach the bottom panel back onto your laptop.

# Part Four
#### Configure Your "Like New" Apple Laptop
[Return to Table of Contents](#drive-replacement-instructions)

All right, this is it. This is where you start up and configure your laptop.

1. Power on your laptop.

1. Work your way through the on screen El Capitan configuration instructions.

1. Transfer any data or files you'd like imported from your most recent Time Machine backup.

1. Reinstall your applications.

# Conclusion
Congratulations. Assuming everything went smoothly, you'll likely have what feels like a new Unibody MacBook Pro.

# Footnotes
[Return to Table of Contents](#drive-replacement-instructions)

#### The 3-2-1 Backup Principle
In short, the 3-2-1 principle states that you should maintain three copies of all your critical data. Two of those copies are kept on-site at home or in some location nearby for easy access. Your third copy is stored at a remote location. For your two on-site copies, one copy can be the original data stored on the drive inside your laptop, and the second copy can be an external drive that you update on a regular basis using automated backup processes such as those provided by Apple's Time Machine software. For your one offsite copy, I'd recommend a proper cloud service backup and recovery provider such as iDrive, BackBlaze, or Carbonite. Services like Dropbox and Google Drive are great for syncing files between computers and the cloud, but [they suck as far as true backup and recovery solutions go](https://www.red-gate.com/simple-talk/cloud/cloud-data/stop-relying-on-cloud-file-stores-as-a-backup-strategy/). The bad news is, you'll need to pay for your cloud backup service. The good news is, it will be well worth it, should your house burn down with your laptop and external drive inside, or in the unlikely event that both internal and external drives fail at the same time. Just remember that these low probability events do happen. My sister-in-law lost all of her digital information when both her internal and external disk drives failed at once. So, consider yourself warned.
