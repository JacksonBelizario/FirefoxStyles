# My Custom Styles

My custom styles to organize my Firefox and improve my productivity with a focused sidebar.

## Addons

- [Sidebery](https://github.com/mbnuqw/sidebery)

## How to

### Inspect an addon

- Enter "about:debugging" in the URL bar
- In the left-hand menu, click This Firefox (or This Nightly)
- Click Inspect next to Sidebery extension 
- Select frame to inspect
  - Click on the rectangular icon (with three sections) in top-right area of the debugger page
  - Select "/sidebar/index.html" for sidebar frame
  - Select "/group/group.html" for group page frame
- Browse "Inspector" tab

### Use Custom CSS in Firefox

To modify UI is necessary add custom CSS code to **userChrome.css** and **userContent.css** files inside browsers profile folder.  

- Unlock custom CSS usage in Firefox 69 and newer
  - `about:config` > `toolkit.legacyUserProfileCustomizations.stylesheets` > `true`  
- Find Firefox profile folder. The correct location for user styles.

  - Find your profile folder ('profile names are different for everyone').  
   `about:support > Profile Folder > Open Folder`  
   or `about:profiles > Root Directory > Open Folder`  
  - User styles belong into `\chrome\` folder. Create it, if there is none yet. It should look like this afterwards:  
   `\ PROFILE FOLDER NAME \chrome\`  
  - Copy `userChrome.css`, `userContent.css` and `\config\`, `\css\`, `\image\` folders into `\chrome\` folder. It should look like this afterwards:  
   `\chrome\config\`  
   `\chrome\css\`  
   `\chrome\image\`  
   `\chrome\userChrome.css`  
   `\chrome\userContent.css`  
  - (Optional) Profile folders location on drive:  
   `C:\Users\ USERNAME \AppData\Roaming\Mozilla\Firefox\Profiles\ PROFILE FOLDER NAME \`  
   Hidden files must be visible to see `AppData` folder. Alternatively open `%APPDATA%\Mozilla\Firefox\Profiles\` from explorers location bar.  

### How to find item ids and attributes?
Enable once:  
- Tools > WebDeveloper > Toggle Tools > Toolbox Options > Enable browser chrome and add-on debugging toolboxes
- Tools > WebDeveloper > Toggle Tools > Toolbox Options > Enable remote debugging

Hit `Ctrl+Alt+Shift+I` or open 'Tools > WebDeveloper > Browser Toolbox'. 

### How to view the changes?

Restart Firefox after every modification for changes to take effect.  