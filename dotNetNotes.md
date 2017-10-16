
# .Net and C# Notes

## Installing on Linux Ubuntu
> https://www.microsoft.com/net/core/#linuxubuntu
### Add dotnet product feed
````
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
````
````
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-trusty-prod trusty main" > /etc/apt/sources.list.d/dotnetdev.list'
````
### Install .NET Core SDK
````
sudo apt-get update
sudo apt-get install dotnet-sdk-2.0.0
````
### Initialize Some code
````
dotnet new console -o hwapp
cd hwapp
````
**dotnet new** creates a new application
**console** is the type of application
**-o hwapp** sets an output directory of hwapp
**cd hwapp** moves into the newly created app directory
### Run the app
````
dotnet run
````
**dotnet run** runs your app

## Download Visual Studio Code
> https://code.visualstudio.com/Download?wt.mc_id=DotNet_Home&dotnetid=1576121558.1503674633
