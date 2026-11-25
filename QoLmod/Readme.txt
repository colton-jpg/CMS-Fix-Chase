Quality of life MOD for game Car Mechanic Simulator 2021.
	https://www.nexusmods.com/carmechanicsimulator2021/mods/105
 
Main idea of this MOD is make gameplay smoother, not faster or more easy.
	Philosophy is also not break gaming experience.
	This includes rules:
	- not break save games
	- not modify game files anyway
	With those rules, I try to keep this modification quite safe. 
	This means, you can anytime disable this modification and game will run as is, without any problem.
	Easiest way to temporary disable all 3rd party mods loaded by MelonLoader is disable MelonLoader by renaming file "version.dll" to different name.
	(Please note, version.dll is MelonLoader file and it does not come with the game. File will be removed if you uninstall MelonLoader)

Installation:
	Install MelonLoader (using MelonLoader Automated Installer) https://melonwiki.xyz/#/?id=automated-installation	
	Download the QoLmod .zip from Files page
	Unzip the file into your Mods directory (eg. \SteamLibrary\steamapps\common\Car Mechanic Simulator 2021\Mods\) 
	You do not need create Mods directory, if there is no Mods directory it means your MelonLoader installation was not successful.
	Run the game, MOD default values should work quite nicely with most players	

File notes:
	AuthenticCarNames.cfg file have new names of cars and their brands. (file only need included names that need to be modified)
	ExtraCarLoaderPlaces.cfg have spots where extra cars will be loaded. (default file has 12 extra car places)
	QoLmod.cfg Please note, MOD will create file after first sucessfully game load with MOD.
	PartConfigData.cfg does not exist by default. With this file you can replace any part brand to different brand
	GenerateThumbnails.txt does not exist by default. With this file you can generate thumbnails easily for multible parts inside Car Editor

Controller specific buttons:	
	Car lights: press gear up and down buttons exact same time

Keyboard specific buttons:
	ALT-key quick switch between mount and unmount modes
	L-key car lights
	ESC during game load will cancel savegame autoload
	CTRL and SHIFT keys control speed with Flycam
	(F1 button 3 times quickly. soft-lock recovery by load last savegame)

CarEditor notes:
	If you make a car mod, following features required QoLmod from end user also. (Car will work, but just without these features)	
	- brand logo (if its not any of game default brand)
	- lights
	- default install of bonusparts
	- engine audio pitch modifier

You can contact me at:
	Discord meitzi
	cms2021qolmod@outlook.com


-------------------
A little more details of some features:
-------------------

AuthenticCarNames
	I think this is quite self self-explanatory, just set this to false and base car names and brands will stay original.	

showCameraDuringGarageLoad
	This feature will show garage with cinematic camera during extra loading time when cars are loaded from parking.
	Just set this false for regular garage entry. (this will save roughly 5 second of loading time)

loadTexturesFromFolder	
	All .png files inside Textures_brand\ folder will be added game as a new brands. (replacing current game brands are no longer necessary)
	Also this will load other Textures folders if you have additional textures.
	I recommend settings this true even when you dont use AuthenticCarNames. Because this will allow show real brands on car mods. 

loadBrandlogosfromMods
	This allow load extra brand defined by car MOD maker and show them on cars		
	MOD owner does only need include brand logo on brand\ directory at png format. Then use same name as filename on car config brand

enableGarageDecorationWithBonusparts
	Allow decoration of garage with bonusparts.
	Because of extra car and extra bonusparts this might have slight impact on performance

SearchWithoutEnter
	This setting allows searching just by typing when shopping. This setting only affect shop screen.
	Due to focus / unfocus logic, it is possible to find this "extra mouse click" after search un-intuitive when this is enabled. 

spawningCarshaveAdditionalConfigData
	If car MOD have configured bonusparts and they are enabled to install, this will install those parts.

enableCarLightsAndBindLbutton
	This will enable light-feature and bind keyboard L-button to turn them on and off
	Please note, car lights location need to configured on every car config (using CarEditor)

allowMoreCameraMoving
	This will enable couple of features
	- camera zoom using mousewheel when on track
    - more max zoom and moving values on all scenes
	- fluid camera replaced by orbit camera instead of fixed camera

showAllPartsonTrack
	Default, there is no battery and some other internal parts on car when on track.
	This setting will allow all parts and suspension be there. (example because of missing hood or otherwise visible)

firstExtraCarIndexNumber
	This is a little advanced setting to set number, which states where extra cars are loaded.
	Default value is 0 meaning start from car 1. Because all new cars are located always to "first free spot" on parking,
	settings this to example 4 allow a new cars not appearing to scene by default. (if you keep those first parking spots free)

JunkyardAndBarnhelperIconShopList
	Instead of showing items in your warehouse (like WarehousehelperIconInventory and WarehousehelperIconShopList)
	this will show, does any of current scene junk pile have this shoplist part. 

specialData
	This allow use some of developer settings that are not intended to daily use. (you can use multible, just separate by ",")
	if set to "gates" or "doors" then garage gates (main doors) will be removed during garage load
	if set to "fastmount" then game DevSettings.FastMountMode will be activated
	if set to "autoshop" then mod will automatically buy any part you put to the shopping list. (autshop will always buy tuned version)
	if set to "parts" then you will be able to generate thumbnail of anypart inside CarEditor (bonuspart example)
	if set to "clearoffice" then garage office will not have any furnitures inside so you can start office decoration from zero (deocration needs to be enabled to this have an effect)
	if set to "halloween", "christmas" or "easter" then that seasonal decoration will be loaded automatically

loadTexturesFromFolder additional info
	You can replace any texture on the game with new texture. 
	You can export and view texture with UnityExplorer just seach UnityEngine.Texture2D
	Textures names match also with resource file texture names (example tool UABEAvalonia )
	Because cars can load textures on the fly, there is additional "Textures_CarLoader" folder which will be loaded every time car is loaded
	"Textures_CarLoader" need to be used if texture is not static on map/scene, example any car part texture or part thumbnail.
	Also any texture than can change on fly like "garaga customization" need to be under CarLoader folder.
	If you are replacing part textures, you can generate new thumnail. Button "Anypart thumbn" will be visible on editor if you set specialData = "parts"
	You can replace scene specifig textures by using folder Textures_XXX
	where XXX is scenename below.

Modding tools:
	[Asset file extractors] AssetRipper https://github.com/AssetRipper/AssetRipper/releases/
	[Asset file extractors] UABEAvalonia https://github.com/nesrak1/UABEA/releases
	[Universal MOD] UnityExplorer (MelonLoader 0.5.7) https://github.com/sinai-dev/UnityExplorer/releases 
	[Universal MOD] UnityExplorer fork (MelonLoader 0.6.0 and upwards) https://github.com/GrahamKracker/UnityExplorer
	[Unity texture tool] PackedMap handler https://www.reddit.com/r/Unity3D/comments/glkvp2/i_made_another_mask_map_packer_for_hdrp/?rdt=60337

Scenenames:
  0 | init
  1 | IntroPlayWay
  2 | IntroRedDot
  3 | IntroCMS
  4 | saveInfo
  5 | splash
  6 | LoadResources
  7 | Menu
  8 | SceneLoader
  9 | Tutorial
 10 | garage
 11 | Auto_salon
 12 | Junkyard
 13 | Showroom_2
 14 | Barn
 15 | Auctions
 16 | Parking
 17 | Test_track_1
 18 | Race_track_1
 19 | SpeedTrack
 20 | Dragstrip
 21 | Custom_track
 22 | CustomPhotoLocation
 23 | Car_Editor
 24 | ThumbnailsCar
 25 | Thumbnails
 26 | WorkshopUploader
 27 | Halloween *
 28 | Christmas *
 29 | Easter *
 30 | photoLocation1
 31 | photoLocation2
 32 | photoLocation3
 33 | photoLocation4
 -1 | xxx custom scenename  *
* this is not primary scene, only additional scene load

-------------------
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.
