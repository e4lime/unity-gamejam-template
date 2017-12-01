# Unity project template for gamejams

## Summary
Project template without premade assets (except for placeholders and fonts). Ludum dare compo friendly.
Doesn't contain 3d party libraries, will a package manager in the future (Unity seems to be making one atm).
Works for Unity 2017.02

## Structure
/unity-project-folder/ is the unity project folder. Create or use the folders outside /unity-project-folder/ to store your asset editor files (blender or photoshop files etc).

## Guide
* Clone or fork it
* Go through the checklists below
* Import DefaultScene.unitypackage for each new scene
* Import MainMenu.unitypackage for a mainmenu scene template

## IMPORTANT Checklist
### In the beginning

#### Per User
* (Optional) Move content in "GameEngine Data" to your Unity installation to override default C# script

#### Per Team 
- [ ] Change /unity-project-folder/ name
- [ ] Decide folder structure (!_Game_ByAssetType vs !_Game_ByEntity) Rename to !_Game, delete unwanted one   
- [ ] Decide what thirdparty libraries to use      
- [ ] Update .gitignore in /unity-project-folder/ to include or exlude third party libraries. Prefix with ! to flip folders
- [ ] Don't commit PAID libraries if going open source     
- [ ] Set Company name in "Project Settings > Player Settings" to team name   
- [ ] Set Product name in "Project Settings > Player Settings" to project name   
- [ ] Decide Time Settings (Default timestep is 0.02, project is set to 0.04)    
- [ ] Decide script structures (Update default c# monobehaviour-script if needed)
- [ ] If you're using a newer unity version, check if .gitignore is still valid; 
 
### At the end

#### Per Team Before Final build
- [ ] Backup project     
- [ ] Set final Company name in "Project Settings > Player Settings"     
- [ ] Set final Product name in "Project Settings > Player Settings"      
- [ ] Remove paid tools      
- [ ] Double check paid tools from commit history if going public    
- [ ] Remove placeholders       
- [ ] Add Unity version used to the readme
- [ ] Add Third party tools versions to the readme
- [ ] WebGL: Remove exceptions handling

### Optimization Checklist
- [ ] Remove empty Update methods
- [ ] Cache components
- [ ] Profile
- [ ] Merge meshes    
- [ ] Texture atlases    
- [ ] Share materials
--------

## Content ##

## Folders

### unity-project-folder
The root of the unity project, rename it

### Unity .gitignore
The .gitignore for the Unity project structure is in /unity-project-folder/

### Templates/Default scripts
Default monobehaviour scripts to copy into your unity engine installation folder (not the project folder!) so it will affect all your projects using that engine. Contains default script-templates and such.

### Templates/Scenes
Default scene packages (Main menu, credits, default level etc).

### unity-project-folder/Assets/Placeholders TBA
Premade placeholders, must be removed and replaced before the last build.

### Settings
#### Project Settings > Editor
- Version Control > Mode: Visible Meta Files
- Asset Serialization > Mode: Force Text

#### Project Settings > Time
- Fixed Timestep: 0.04 (Default: 0.02)
- Maximum Particle Timestep: 0.04 (Default: 0.02)
-----

## List of Thirdparty Libraries and tools
Recommended thirdparty libraries and tools. All thirdparty folders SHOULD (double check) be listed in the .gitignore file. Comment out those you want to commit or flip with an exclamation mark (!). 

DON'T commit PAID content, remember that paid content will still exist in git-history after you remove them.

### DOTween Pro
An Animation and tweening library.   
PAID  
https://www.assetstore.unity3d.com/en/#!/content/32416   
Or Use the Free version (below)  

* Demigiant/DOTweenPro
* Resources/DOTweenSettings.asset

### DOTween
An Animation and tweening library.  
Free   
https://www.assetstore.unity3d.com/en/#!/content/27676    
Or use the paid version (above)  

* Demigiant/DOTween
* Resources/DOTweenSettings.asset

### ProBuilder Basic
3D Level tool.   
Free    
https://www.assetstore.unity3d.com/en/#!/content/11919    

* ProCore/ProBuilder


### Unity Toolbag
Scripting Tools   
Free   
https://github.com/nickgravelyn/UnityToolbag     
Omitted: SimpleSpriteAnimation, SortingLayer, SyncSolution    
 
* UnityToolbag-master/CacheBehaviour
* UnityToolbag-master/Dispatcher
* UnityToolbag-master/Future
* UnityToolbag-master/SnapToSurface
* UnityToolbag-master/StandardPaths
* UnityToolbag-master/UnityConstants

###  Consolation
View console ingame    
Free    
https://github.com/mminer/consolation    

* consolation-master/

---------

## Todo
* Add fonts (Fonts are allowed!)
* Add Package manager (unity seems to be making one atm)
