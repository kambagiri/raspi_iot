
## Commands: 

>> grim (hit-enter) => takes a screenshot of current screen. 

>> scrot (hit-enter) => takes a screenshot in X11 mode. 


# Install DOTNET SDK in Raspi: 
## Commands: 
1. wget https://dot.net/v1/dotnet-install.sh -O dotnet-install.sh
//GRANTS RUNTIME PERMISSIONS
2. chmod +x ./dotnet-install.sh 
//INSTALL LATEST VERSION: 
3. ./dotnet-install.sh --version latest
//install .NET Runtime instead of the SDK, use the --runtime parameter
4. ./dotnet-install.sh --version latest --runtime aspnetcore
//TO INSTALL SPECIFIC VERSION
5. ./dotnet-install.sh --channel 9.0

## POST INSTALL: 
dotnet command doesn't work immediately. to get it work follow below instructions; 
//Create a symlink to the dotnet file: 
sudo ln -s ~/.dotnet/dotnet /usr/bin/dotnet

## Add to PATH Environment variable: 
export PATH=$PATH:$DOTNET_ROOT:$DOTNET_ROOT/tools
