* Build cmake - Generating make
folder structure
./
./CMakeLists.txt
./build
./build/CMakeFiles

- ON ./ :
mkdir build
cd build 
cmake ..
cd ..
make -C build 

# Building OGRE3D Sample
$sudo pacman -S boost-libs boost freeimage freetype2 libxaw libxrandr mesa ois zziplib cmake gcc
> Get Compress archive from Ogre.org
> by wget or downloading
> Extract
$unzip ogre-*-*-*.zip
> or tar -xvzf ogre-*-*-*.tar
$mv ogre-*-*-*/  ~/Documents
$cd ~/Documents/ogre-*-*-*/
$mkdir Build && cd Build
$cmake ..
$make -j2
$sudo make install

# Building Ogre Project
## Folder Hierarchy
> Project_Folder
	> Build/ 
	> CMakeLists.txt 
	> srcs/ 
		> headers/ 
## Build
$mkdir Build && cd Build 
$cmake ..
$cmake --build . --config Release
. can be Release or Debug