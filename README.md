# Sublime Merge Patcher

slm.py is a [python script](https://github.com/bousqi/slm-patcher) based on [deyixtan script](https://github.com/deyixtan/slt-patcher) that patches software updates and license checks on Sublime Merge Editors.

## SCRIPT COMPATIBILITY

|         Builds Supported         | Operating System |
| -------------------------------- | ---------------- |
| 1055 onwards                     | Windows 64-bit   |
| 1055 onwards                     | Linux 64-bit     |

## USAGE

> python slm.py <"sublime merge executable file path">

## MANUAL PATCHING

### Replacing Executable

1. Back up your original Sublime Merge Editor executable file. 
2. Download the desired patched executable from the "patched_executables" folder.
3. Copy the downloaded file into your own Sublime Merge directory.
4. Run the executable file.

<br>

# Manual Patching
## Build 1055
### Windows 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x2774D  | 0x00     | 0x01    |
| Initial License Check    | 0x2184E  | 0x38     | 0x08    |
|                          | 0x2184F  | 0x00     | 0x01    |
### Linux 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x28F66F | 0x00     | 0x01    |
| Initial License Check    | 0x28CE13 | 0x38     | 0x08    |
|                          | 0x28CE14 | 0x00     | 0x01    |

<br>