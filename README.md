Here's a clear and complete list of **native** and **non-native but supported** extension formats for the 3 main platforms: **VirtualBox**, **VMware**, and **Hyper-V**.

---

## 🔰 VIRTUALBOX

### ✅ Native Formats:
| Type | Extension | Description |
|------|-----------|-------------|
| Virtual Disk | `.vdi` | Native VirtualBox virtual hard disk |
| Virtual Appliance | `.ova` | Standard virtual appliance archive |
| Config | `.vbox`, `.vbox-prev` | VM configuration files |
| Snapshot | `.sav` | Saved VM state |
| Logs | `.log` | VM logs |

### 🔄 Supported (Non-native but compatible):
| Extension | Used by | Notes |
|-----------|---------|-------|
| `.vmdk` | VMware | Can use as virtual disk |
| `.vhd` / `.vhdx` | Hyper-V | Can be used, but limited support |
| `.iso` | All | CD/DVD installation image |
| `.ovf` | All | Can import/export with OVF descriptor |

---

## 🔰 VMWARE (Workstation, Fusion, ESXi)

### ✅ Native Formats:
| Type | Extension | Description |
|------|-----------|-------------|
| Virtual Disk | `.vmdk` | Native virtual hard disk |
| Config | `.vmx`, `.vmxf` | Main VM config |
| Snapshot | `.vmsn`, `.vmsd` | Snapshot and metadata |
| Log | `.log` | VM logs |
| VM State | `.nvram` | BIOS/UEFI saved state |
| Virtual Appliance | `.ova` | OVF archive (often includes VMDK) |
| Descriptor | `.ovf` | OVF descriptor file |

### 🔄 Supported (Non-native but compatible):
| Extension | Used by | Notes |
|-----------|---------|-------|
| `.iso` | All | OS image |
| `.vhd` / `.vhdx` | Hyper-V | Can be converted using VMware Converter or OVF Tool |
| `.vdi` | VirtualBox | Can be converted to .vmdk with `VBoxManage` |
| `.img`, `.raw` | Linux disk formats | Needs conversion |

---

## 🔰 HYPER-V (Windows)

### ✅ Native Formats:
| Type | Extension | Description |
|------|-----------|-------------|
| Virtual Disk | `.vhd`, `.vhdx` | Native disk formats (vhdx is newer) |
| Config | `.xml` | Old VM config format |
| VM State | `.bin`, `.vsv` | Save state files |
| Checkpoints | `.avhdx` | Differencing disks (snapshots) |

### 🔄 Supported (Non-native but compatible):
| Extension | Used by | Notes |
|-----------|---------|-------|
| `.iso` | All | OS installation image |
| `.vmdk` | VMware | Needs conversion to `.vhd` (StarWind V2V, QEMU, etc.) |
| `.vdi` | VirtualBox | Not directly supported, must convert to `.vhd` |
| `.ova`, `.ovf` | VirtualBox/VMware | Not supported directly — must extract and convert disks manually |

---

## 🧰 Conversion Tools (Cross-platform support)

| Tool | Purpose |
|------|---------|
| `VBoxManage` | Convert VDI ↔ VMDK/VHD |
| `StarWind V2V Converter` | GUI tool for converting VMDK, VDI, VHD, etc. |
| `OVF Tool` (VMware) | Convert OVF/OVA to/from VMware |
| `QEMU` | Advanced disk conversion between almost any format |
| `VirtualBox Import/Export` | File > Export Appliance for cross-platform OVA sharing |

---

