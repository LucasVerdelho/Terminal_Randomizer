# Terminal_Randomizer
A script that changes the appearance of a Windows Terminal, randomly selecting background, foreground colors as well as the background gif


## Example

<p align = "center">
    <img src="https://github.com/LucasVerdelho/Terminal_Randomizer/blob/main/readme_assets/hello_there.gif" width="630" height=auto/>
    <img src="https://github.com/LucasVerdelho/Terminal_Randomizer/blob/main/readme_assets/general_kenobi.gif" width="630" height=auto/>
</p>
                                                                                                                                   
                                                                                                                                  
## How to Use

1. Make sure you have installed the Windows Terminal from the Microsoft Store.

2. You will also need to have python installed and to have this repository downloaded somewhere on your pc where you will be able to remember it's location.

3. Excute the following command in order to install necessary libraries:
```
pip install pillow colorthief
```

4. Go to the input.txt file on this repository and change the user to your own.

5. Open your Windows Terminal and change the directory to:
```
%The_Path_To_The_Repository%\Terminal_Randomizer\src
```
where you change the Path to wherever you downloaded the repository.

6. Run the following command:
```
python terminal_randomizer.py
```

7. If it changed, means everything is probably working. In case it didn't work, check the following segment: **"How to Find the Paths"**


Note : 
>To add your own gifs, just copy them to the photos folder

Yes, Another Note :
> I am using the font Source Code Pro, which i really recommend you have installed for better legibility on the terminal. It is a free font found on google fonts: ```https://fonts.google.com/specimen/Source+Code+Pro```. To add this, simply open the settings.json of your windows terminal, go to the defaults and add 
```            
"font": {
    "face": "Source Code Pro",
    "size": 20,
    "weight": "light"
},
```


## How to Find the Paths
To find the settings.json file, this path usually works:
(You will have to change the user to your own)
```
C:\Users\{user}\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\
```

If you find the settings.json file using this path, just go over to the input.txt file, and change the user there as well.


I recommend using the voidtools' **Everything Search** for this, but the terminal executable is generally located in the path i have included in the **WinTerminal_Run.bat file**, being called **"wt.exe"**. 

For the retro shader effects on the terminal just change the path of the .hlsl file to where you downloaded the repository.



## How do i make it go brr every time i open the terminal?
Unfortunately there is no clean solution that I have found to this problem, so we will have to do with a janky Windows type beat ugly fix.

1. Open the batch file that is included in this repository.

2. Make sure the **"cd"** command will place you in the right path

3. Change the wt.exe path to where the Windows Terminal is installed on your pc

4. Open Task Scheduler and make a new folder named "WinTerminal" inside the Task Scheduler Library folder.

5. Create a new Task and also name it "WinTerminal" 

6. Select the option "Run with the highest privileges" and on the "Configure for:" select "Windows 10"

7. Go to the Actions tab and make a new action, it will default to Start a Program which is what we want.

8. Browse to the WinTerminal_Run.bat file and save the action

9. Save the task and close Task Scheduler

10. Go to your Desktop and create a new shortcut

11. If you followed the naming convention the location of the item shall simple be:
```
C:\Windows\System32\schtasks.exe /RUN /TN "WinTerminal\Winterminal"
```
Else, make sure to reopen the TaskScheduler and check the path to your task

12. Name the Shortcut and you are all set!


Note: 
>You can also change the icon to the terminal.ico from Windows, I will include a copy of it in the repository



