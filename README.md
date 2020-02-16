# ChaturbateDownloader

A CLI Chaturbate.com downloader that allows you to download streams as they are live in the highest quality available without the weird layers on top of the screen, upon email notification without further interaction while you are doing other things.

##### Supports the following
* Download streams without weird overlay (DMCA and other stickers taking up more screen estate than they should -> not anymore)
* Save the stream to your local storage
* Never miss a stream again

##### How does it work?
It works by scanning your email inbox for email notifications from Chaturbate and then visiting the links in those emails (automatically logging in as well) and downloading the stream until the model goes offline again.

This means that it NEEDS email access so be sure to create a new email account somewhere dedicated for just this purpose.

This program doesn't take any flags other than where to find the settings.json file, all settings are in there and there will be a settings.json file created on the first run if it doesn't exist.

Depends on FFmpeg (static).

IMAP configuration guides:
* [Outlook](https://support.office.com/en-us/article/pop-imap-and-smtp-settings-for-outlook-com-d088b986-291d-42b8-9564-9c414e2aa040)
* [GMail (may need to enable insecure app access or per app passwords as well)](https://support.google.com/mail/answer/7126229?hl=en)
* [ProtonMail](https://protonmail.com/bridge/outlook2013)

##### Examples

Imagine the link of stream being: ``https://chaturbate.com/mykinkydope/``

Then the command to download indefinitely (until the stream goes private or stops) would be:

``chaturbate-watcher.exe``

As long as you subscribed to email notifications from that model, and of course Chaturbate decides to send you an email notification to begin with.

## Installation

First install FFmpeg, on windows this is a little less straightforward than on linux

#### Windows
* Download the STATIC windows package that suits your platform (32 or 64 bit) from https://ffmpeg.org/download.html and then unzip this package.
* When you unzip this package you will find a sub folder called ``bin`` that contains `ffmpeg.exe`
* Now there are 2 options:
    * Take note of the file location of ``ffmpeg.exe``, copy it somewhere as you will need it later
    * Add the contents of the ``bin`` folder to your environment variable called `PATH`
* Download the repository contents
* Run the executable that fits your platform (32 bit: `_386`, 64 bit: `_amd64`)
    * If you added ffmpeg to your environment variables ignore this
    * `chaturbate-watcher.exe`
    * Because you did not add ffmpeg to your environment variables this program can't find the ffmpeg executable so be sure to put right path to the ffmpeg executable in the settings.json file

#### Linux

Run your OS's version of:
`sudo apt install ffmpeg`

After that you can run the executable that fits your platform perfectly without the ffmpeg flag

## Disclaimer

Use at own risk.

##### My experience

I had to create a new account linked to a new email address to start receiving email notifications again. I stopped receiving them right before January as did a lot of other people and that is because of Chaturbate.

My recommendation is to get a new account linked to an email address dedicated to only that anyways because of how this program works.

While this program can watch multiple streams as your account I don't recommend having it watch a lot of streams at the same time for that is an easy way to detect a bot which may result in a ban.

##### Future

I don't plan to maintain this unless something breaks due to chaturbate site updates or if a crucial feature is missing

##### Unsupported
* Private streams

Why? Unlike the PHDownloader I have no account to test this feature with therefore had no way of implementing it.

Want them to be implemented? I will need to be able to do some testing, donating money or an account with tokens towards that goal would allow me to implement those cool things.

Simply open up an issue and we will figure it out from there. 
