# Snort Installation Guide on Amazon Linux 2
---

## Prerequisites
1. Launch an Amazon Linux 2 EC2 instance.
   - **Instance Type**: t2.micro or larger
   - **Security Group**:
     - Allow SSH (port 22) for remote access.
2. Connect to the instance using SSH.

--- 

## Step 1: Update the System
Run the following command to ensure the system is up-to-date:
```bash
sudo yum update -y
```

## Step 2: Install Required Dependencies
Install all the necessary tools and libraries for building and running Snort:
Snort relies on various libraries and tools to function properly. These dependencies provide the necessary components for building, compiling, and running Snort
```bash.
sudo yum install -y gcc libpcap libpcap-devel pcre pcre-devel bison flex zlib zlib-devel make wget
```

## Step 3: Download Snort 
Download the Snort source code from the official Snort website:
```bash
wget https://www.snort.org/downloads/snort/snort-2.9.20.tar.gz
```

## Step 4: Extract the Downloaded Archive
Extract the Snort archive: The Extract Downloaded Archive step unpacks the Snort source code file so you can access its contents. This is needed to prepare the files for installation.
```bash
tar -xvzf snort-2.9.20.tar.gz
cd snort-2.9.20
```
![Snort Install](../screenshots/snort-install.png)

## Step 5: Install Libdnet
The libdnet library is required by Snort for low-level networking functionality. If it’s missing, Snort will not compile. Follow these steps to install libdnet:
1. Download libdnet source code: 
```bash 
wget https://github.com/dugsong/libdnet/archive/refs/tags/libdnet-1.12.tar.gz -O libdnet-1.12.tar.gz
```
2. Extract The Archive: 
```bash
tar -xvzf libdnet-1.12.tar.gz ##Then CD into it. 
cd libdnet-libdnet-1.12
```
3. Install Necessary Compilers: 
Compilers are like translators for your computer. Programs like libdnet and Snort are written in a language humans can understand (like C or C++), but your computer can’t directly use that. A compiler converts this human-readable code into something the computer can run.
```bash
sudo yum install -y gcc gcc-c++
```
4. Configure and Build libdnet:
	•	Why Configure?
The ./configure command prepares libdnet to work on your specific system. It checks if all required tools and libraries are available and sets everything up for the building process. Think of it as customizing the library for your computer.
	•	Why Build?
The make command compiles the source code into a usable library. This step translates the human-readable code into machine code that your system can run.
```bash 
./configure
make
sudo make install
``` 
5. Update the Library Cache: This lets the system know the library 
```bash 
sudo ldconfig
``` 
![Libdnet Process](../screenshots/Screenshot%202025-01-17%20at%2021.23.56.png)