# WSL2Windows-FolderPathConverter

Convert Windows and WSL2 folder addresses into clean, relative Linux paths (`./folder/subfolder`) for AI, research and dev work.

<img width="1032" height="615" alt="WSL2Windows-FolderPathConverter UI" src="https://github.com/user-attachments/assets/120d9894-b16b-4157-beee-14060ada8706" />

## Example

| You select | Start directory (`./`) | Output |
|---|---|---|
| `\\wsl.localhost\Ubuntu-26.04\home\llm\ACE-Step-1.5\dataset\samples\drum` | `\\wsl.localhost\Ubuntu-26.04\home\llm\ACE-Step-1.5` | `./dataset/samples/drum` |

## Features

- Lists all folders inside a directory you choose, in a dropdown
- Pick any parent folder as the `./` start directory
- Converts `\` to `/` and adds the `./` prefix
- One-click **Copy** to clipboard
- Works with WSL2 network paths (`\\wsl.localhost\...`) and normal Windows paths
- Modern dark UI

## Installation

1. Download `WIN2WSL_PathConverter.ps1` and save it as `C:\WIN2WSL_PathConverter.ps1`.
2. Use `launchPathConverter.ps1` to start the program. It runs:

```powershell
powershell -STA -ExecutionPolicy Bypass -File C:\WIN2WSL_PathConverter.ps1
```

> **App won't start?** Create a shortcut to the launcher and run it **as administrator**.

## Usage

1. **Set the root folder to scan.**
2. **Select the folder you want.**
3. **Select the start `./` folder.**
4. **Copy the address.**

old version but same steps:
#1. set root folder to scan:
<img width="933" height="635" alt="{362396E3-179D-4E18-A06C-C29131904F96}" src="https://github.com/user-attachments/assets/c39b8963-ecc1-4225-a53e-84dbf2f903a2" /> 

#2. select folder you want: 
<img width="929" height="438" alt="{6B59B883-4554-4534-9700-89A926071D22}" src="https://github.com/user-attachments/assets/5bded460-c301-4f73-8fe7-554d26b06ab1" /> 

select the start ./ folder dir: <img width="928" height="434" alt="{15B40D71-61C8-41D6-BCBF-3BD3D511B404}" src="https://github.com/user-attachments/assets/47302834-44c5-431f-b7a9-253173957d83" />
#5. Copy the adress:
<img width="929" height="444" alt="{9D9AD751-51C2-4AB2-9414-46EE7D9688A3}" src="https://github.com/user-attachments/assets/6326aae3-da87-46b1-96b7-7dc79378a223" /> 

<details>
<summary>Screenshots of the steps (older UI, same workflow)</summary>

**1. Set the root folder to scan**

<img width="933" height="635" alt="Step 1: set root folder" src="https://github.com/user-attachments/assets/c39b8963-ecc1-4225-a53e-84dbf2f903a2" />

**2. Select the folder you want**

<img width="929" height="438" alt="Step 2: select folder" src="https://github.com/user-attachments/assets/5bded460-c301-4f73-8fe7-554d26b06ab1" />

**3. Select the start `./` folder**

<img width="928" height="434" alt="Step 3: select start directory" src="https://github.com/user-attachments/assets/47302834-44c5-431f-b7a9-253173957d83" />

**4. Copy the address**

<img width="929" height="444" alt="Step 4: copy the address" src="https://github.com/user-attachments/assets/6326aae3-da87-46b1-96b7-7dc79378a223" />

</details>

## ⚠️ Warning

**Do not scan a whole `C:\` drive or other system drives.** The app lists every folder path and keeps it all in RAM, so a huge scan will crash it. Scan a specific project folder instead, or untick **Include all subfolders (recursive)** to scan one level only.

## Use cases

- Fast directory scanning and sample loading for training in apps like **ACE-Step 1.5** and other AI tools
- Linux developers who work on Windows through WSL

## Disclaimer

This program was made with AI. Use at your own risk.
