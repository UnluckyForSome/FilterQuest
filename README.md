# FilterQuest
Filterquest is a powerful script which can take any game directory and remove region duplicates (prioritising USA releases), foreign language and non-retail release games, leaving you only the good stuff!

## Prerequesits
Filterquest is a PHP script which requires a POSIX environment with PHP installed. On Windows, this is most easily achieved by installing Cygwin (https://www.cygwin.com/) with PHP checked during installation. On Linux, you'll just need to make sure you have PHP installed.

FilterQuest relies on games being named in the popular ReDump/TOSEC naming conventions, for example "Crash Team Racing (USA)". These games must all be in the same directory.

## Usage
On Windows, place the "filterquest" script file into the same directory of the files you want to filter, then using the Cygwin Terminal navigate to the same directory and use "php filterquest" to run.

On Linux use the same method except use the Linux Terminal ;-)

## Results
Filterquest **won't delete any files**. The script will output a folder named "Removed" in which all the filtered games which FilterQuest thinks you don't need will be moved. You can easily recover your original collection by moving these files back into the original folder.

### Filterquest will filter:
 - Region Duplicates - USA will take priority, if a USA version of a game exists any other region will be removed.

 - Inferior versions:
Lower versions of the same game will be removed. For example Crash Team Racing (USA) (v1.0) will be removed if Crash Team Racing (USA) (v1.1) exists.

 - Foreign language releases
English only! Any games in a foreign language will be removed.

 - Non-retail releases
Demos, unlicensed games and betas will all be removed.