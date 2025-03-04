# kde-hdr-toggle

All credit goes to SysGhost on discuss.kde.org.   
Link to original thread: https://discuss.kde.org/t/toggle-screen-hdr-on-or-off-automatically-with-this-script/29253

I'm merely hosting it on github for future reference. 

>Got a fancy nice HDR monitor?   
>
>Love that KDE plasma desktop helps utilise HDR?   
>
>Tired of manually toggling HDR on or off depending on what you’re doing?   
>
>Can’t stand editing a bunch of custom launch options or PRE/POST scripts for each game/application each time the screen setup changes? (i.e. laptop docking stations or KVM switches)   
>
>And yeah… having your ICC profile erased each time an HDR title is launched is another annoyance we solve here. (Optional)   
>
>…
>
>Fret no more. Here’s a lil helper-script to automate this. It utilises kscreen-doctor and makes implementing it a lot easier in Steam, Lutris and/or other launchers/wrappers. One place to edit/change instead of the hundreds!
>
>This script can also be used as a simple command in the CLI if one so desires. It only requires the plasma-desktop environment to be active. (Because it uses kscreen-doctor. I know of no other commands that independently can change hdr and wide gamut settings outside of plasma)
>
>How it works:
>>Usage:
>>hdr-toggle [enable|disable|toggle|help] [output] [ICC profile]
>>
>>KDE plasma desktop HDR toggler.
>>Utilises kscreen-doctor.
>>To be used with launch wrapper scripts or command lines such as Steam, Lutris and others.
>>
>>ICC profile is only applied when HDR mode is disabled.
>>Omit all options to simply toggle HDR on or off depending on the current status. It will then use the internal defaults. These defaults can be changed by editing this script.
>>
>>Steam:
>>Add this to the games command line: 'hdr-toggle enable; %command%; hdr-toggle disable'
>>This will enable HDR, launch the game, and once the game quits, disable HDR.
>>
>>Lutris:
>>Right-click and choose 'Configure'. Switch to tab 'System options'.
>>In the field 'Pre-launch script', add 'hdr-toggle enable'. In the field 'Post-exit script, add 'hdr-toggle disable'
>>
>>You can also add hdr-toggle as a command in your wrapper scripts. See 'Usage' above.
>>
>>Tip: Edit ~/.bin/hdr-toggle and change the variables at the top to customize the defaults to your setup.   
>>See 'kscreen-doctor -o' to list available outputs and their capabilities.   
>>   
>>To disable this script from toggling anything, a global system variable can be used: 'export DISABLE_HDR_TOGGLING=true'.   
>>Unset the variable or set it to false to resume normal operation.   

>'nuf babbling. Here’s the script.   
>Name it “hdr-toggle” and make it executable.   
>Save it under ~/.bin/, or your preferred user executable path.   
>then run ‘hdr-toggle help’ to see how it works.   
>It depends on kscreen-doctor to properly operate.   
>
