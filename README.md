# Mission-Planner-Installation-using-Mono
This guide provides step-by-step instructions for installing Mission Planner on Ubuntu 20.04 using Mono.

Reference: [Ardupilot.org](https://ardupilot.org/planner/docs/mission-planner-installation.html)

## Mission Planner Installation
### Step 1: Install Mono

For Ubuntu 20.04 (amd64, armhf, arm64, ppc64el) you can follow these steps. For all other installations and additional references, visit [mono-project.com](https://www.mono-project.com/download/stable/#download-lin)

#### a. Add the Mono repository to your system
```bash
sudo apt install ca-certificates gnupg

sudo gpg --homedir /tmp --no-default-keyring --keyring /usr/share/keyrings/mono-official-archive-keyring.gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF

echo "deb [signed-by=/usr/share/keyrings/mono-official-archive-keyring.gpg] https://download.mono-project.com/repo/ubuntu stable-focal main" | sudo tee /etc/apt/sources.list.d/mono-official-stable.list

sudo apt update
```
#### b. Install Mono
```bash
sudo apt install mono-devel
```
Ensure that the mono-devel package is installed to compile code.

### Step 2: Download and Install Mission Planner

There are two options for installation.

#### Option 1:

```bash
mkdir ~/missionplanner

cd ~/missionplanner

wget https://firmware.ardupilot.org/Tools/MissionPlanner/MissionPlanner-latest.zip

unzip MissionPlanner-latest.zip

mono MissionPlanner.exe
```
Mission Planner should now be running.

#### Option 2:

Download Mission Planner as a zip file from [here](https://firmware.ardupilot.org/Tools/MissionPlanner/MissionPlanner-latest.zip) and unzip to a directory.

Go to that directory where MissionPlanner extracted and open the terminal from the same directory. Then, execute:

```bash
mono MissionPlanner.exe
```
Mission Planner should now be running.


## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
