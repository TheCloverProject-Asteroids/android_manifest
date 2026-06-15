
# ⚡ The Clover Project For Asteroids

An Android Operating System Based On AOSP.  
This guide will help you **set up, sync, and build The Clover Project** for **Nothing 3A / PRO**.  

---

## 📝 Table of Contents
- [Prerequisites](#-prerequisites)  
- [Setup Repository](#-setup-repository)  
- [Sync Local Manifests](#-sync-local-manifests)  
- [Build Instructions](#-build-instructions)  
- [Tips & Notes](#-tips--notes)  

---

## 🛠️ Prerequisites
Make sure your system has the following installed:

- Linux with required build tools  
- `repo` tool  
- `git-lfs`  
- Adequate storage (~400GB free recommended)  

---

## 📂 Setup Repository
Clone and initialize The Clover Project repository:

```bash
mkdir Clover && cd Clover
repo init -u https://github.com/The-Clover-Project/manifest.git -b 16-qpr2 --git-lfs
```

---

## 🔄 Sync Local Manifests
Add device-specific manifest for Nothing 3A / Pro AKA asteroids:

```bash
mkdir -p .repo/local_manifests
wget https://raw.githubusercontent.com/TheCloverProject-Asteroids/android_manifest/refs/heads/16-qpr2/asteroids.xml      -O .repo/local_manifests/asteroids.xml
```

Sync the repository:

```bash
repo sync
```

---

## 🏗️ Build Instructions

### Nothing 3A / PRO (asteroids`)
```bash
. build/envsetup.sh
lunch clover_asteroids-bp4a-userdebug
mka clover
```

---

## 💡 Tips & Notes
- Run `source build/envsetup.sh` before building.   

--- 
