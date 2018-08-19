# FilterQuest
Filterquest is a powerful script which uses the No-Intro and Redump naming conventions to filter out any potential games which you wouldn't want, saving you space on your drives and giving you more clarity within your collections.

## Results
Filterquest **won't delete any files**. The script will output a folder named "Removed" in which all the filtered games which FilterQuest thinks you don't want will be moved. You can easily recover your original collection by moving these files back into the original folder.

### FilterQuest will filter:
 - Foreign releases:
Any game which isn't from an English-speaking country - e.g "Game (Japan)".
 
 - Foreign languages:
English only! Any games in a foreign language will be removed - e.g "Game (Europe) (Fr,De,Es)".
 
 - Non-full-retail reases:
This includes demos, unlicensed games, betas and much more - e.g "Game (Beta)".
 
 - Regions
If you have several versions of the same game with different regions, Filterquest will prioritize in the order: USA > Europe > UK > Australia > Everything Else! - e.g if "Game (USA)" exists "Game (Europe)" will be removed. This also covers combined regions - e.g if "Game (USA, Brazil)" exists, "Game (Europe)" will be removed.
 
 - Languages
Versions of the same game with fewer languages will be prioritized - e.g if "Game (Europe)" exists "Game (Europe) (En,De,Fr)" will be removed. Different versions with the same amount of languages will be evaluated for the best languages possible - e.g if "Game (Europe) (En,Fr,De)" exists "Game (Europe) (Pt,Sv,Ru)" will be removed.

- Versions & Reversions
Lower versions of the same game will be removed - e.g if "Game (USA) (v1.2)" exists "Game (USA) (v1.1)" will be removed. If "Game (USA) (Rev A)" exists "Game (USA) (Rev B)" will be removed.

- Manual Region Duplicates
Not all games have the same names in different regions and so can't automatically be filtered. To tackle this, Filterquest has reguarly updated built in "lists" which it uses to identify that a "primary" game is present and then subsequently removes the region duplicate. If no primary version is present it is left alone.

- Manual Demos
Uses a manual "list" to identify demos which for one reason or another haven't been marked with the "(Demo)" tag in the filename - e.g "Best Games Ever 1"

- Manual Others
Uses a manual "list" to identify games in the full redump collections which aren't really playable and are more "utilities" - e.g "Network Access Disc"



## Prerequesits
- Filterquest is a PHP script which requires a POSIX environment with PHP installed. On Windows, this is most easily achieved by installing Cygwin (https://www.cygwin.com/) with PHP checked during installation. On Linux, you'll just need to make sure you have PHP installed.

- FilterQuest relies on games being named in the popular Redump/No-Intro naming conventions, for example "Game (USA)". These games must all be in the same directory.

## Usage
- Click the green "Clone or download" button and "Download ZIP". Extract the archive and place the entire "FilterQuest" folder into the same directory as your games. Remember to keep the entire contents of FilterQuest in it's own folder. You can call it what you like - as long as the FilterQuest folder is in with all your games you should be good.
- On Windows, using the Cygwin Terminal navigate to the same directory and then use `php FilterQuest` to run. On Linux use the same method except use the Linux Terminal.
- Filterquest will create a "Removed" folder in your games directory in which it will put all the games it thinks need removing. If manual lists are used, a "Logs" folder will also be created within the "Removed" folder with logs of what has been removed in regards to the manual lists.
- Remember, FilterQuest is looking for games one directory up from where the script is run from, so make sure you paste the FilterQuest folder into your games directory, and not just all the files!
