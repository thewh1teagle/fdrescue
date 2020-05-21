# fdrescue
## using ddrescue to recover folders recursively



ddrescue is a great tool. It helps us to recover files from damaged hard drive.

The problem with ddrescue is that we can only recover files with it, so we cannot

recover folders with all the contents. 

Because of that i decided to write my own script to make the job of finding the files

and then recover them with ddrescue to another directory.



## Requirements

ddrescue python3 git

```
sudo apt-get install gddrescue git python3
```

## Installation
```
git clone https://github.com/thewh1teagle/fdrescue.git
cd fdrescue && chmod +x fdrescue
```

## Usage: 
```
./fdrescue <INFOLDER> <OUTFOLDER>
```
