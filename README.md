# moon-phase-background
Change background picture to high resolution picture of the current moon phase from NASA

I wrote a bash script which takes a high resolution image of the current moon phase from NASAs Dial-A-Moon website "https://svs.gsfc.nasa.gov/vis/a000000/a004800/a004874/", adds it onto a background image of stars, labels the image with the Illumination % and the Age of the Moon Cycle  and sets it as a background image on Linux Mint Cinnamon.

best.tif is an example picture. (Resolution 5641x3650 by default, 8192x5641 is possible too.)

This script won't automatically update your background, only when excecuted. But if you want it to update automatically just set a Cron Job or add moonback.sh to startup applications.

Also the downloaded images are deleted again immediately, so they don't clog up your storage.

# Requirements:
If you have cinnamon these are most likely pre-installed.
 - bash
 - curl
 - ImageMagick
 - Linux Mint Cinnamon (although if you know how to replace the background image on your current Computer you only need to replace 2 lines in the script.)
 - year 2021 (the code only works until the end of 2021, then it needs to be updated)


# Installation:
 1. Download the repository and extract the files in some new folder, anywhere you want. 
 2. Navigate to your new folder in terminal
 3. Make the script executable by entering 
```chmod u+x moonback.sh```

That's it! You can then run the script using ```./moonback.sh```. It will download a 5MB image file and change your desktop background and then delete the downloaded image again. The file back.tif is your new background image now. Let me know if you encounter any errors.

You can add this script moonback.sh to startup applications to automatically load the new moon phase background on startup.

Or you can have it automatically update in certain time intervalls. To do this you can set a cron job. You should read up on how to do that online. It's pretty easy.

# Configuration:
 - Resolution: There is an option to get a higher resolution image(8192x5641, default is 5641x3650), it is commented in the code if you want to turn it on. You just have to set isbig=true. You can also set an even lower resoltion but you're going to half to do the work yourself. It's possible though and fairly easy.

- If your display size is different from mine you might have to play around with some settings, (like the text field position).

- You can customize anything you want, including the background image, the text, anything! I have added comments to make the code easy to understand. It is very short and simple.

