# 🚀 Ubuntu Maintenance Tool

A powerful CLI tool to clean, update, and optimize Ubuntu systems.

---

# 📦 Installation (Manual)

Clone the repository:

```bash
git clone https://github.com/SfAtRhl/ubuntu-maintenance.git
cd ubuntu-maintenance
````

Make the script executable:

```bash
chmod +x ubuntu-maintenance
```

Move it to system path:

```bash
sudo mv ubuntu-maintenance /usr/local/bin/
```

Run the tool:

```bash
sudo ubuntu-maintenance
```

---

# 🛠️ Create a `.deb` Package

Follow these steps to package your tool like a real Ubuntu application.

---

## 1. Create Folder Structure

```bash
mkdir -p ubuntu-maintenance/DEBIAN
mkdir -p ubuntu-maintenance/usr/local/bin
```

---

## 2. Add Your Script

Copy your script:

```bash
cp ubuntu-maintenance ubuntu-maintenance/usr/local/bin/
```

Make sure it's executable:

```bash
chmod 755 ubuntu-maintenance/usr/local/bin/ubuntu-maintenance
```

---

## 3. Create Control File

Create the control file:

```bash
nano ubuntu-maintenance/DEBIAN/control
```

Paste:

```text
Package: ubuntu-maintenance
Version: 1.0
Section: utils
Priority: optional
Architecture: all
Maintainer: Ait Rehail <soufyane.aitrehail@gmail.com>
Description: Ubuntu maintenance and cleanup CLI tool
 A command line tool to update, clean, and maintain Ubuntu systems.
```

---

## 4. Build the Package

```bash
dpkg-deb --build ubuntu-maintenance
```

Output:

```bash
ubuntu-maintenance.deb
```

---

## 5. Install the Package

```bash
sudo dpkg -i ubuntu-maintenance.deb
```

---

## 6. Run the Tool

```bash
sudo ubuntu-maintenance
```

---

## 7. Uninstall

```bash
sudo apt remove ubuntu-maintenance
```

---

# ⚙️ Usage Options

```bash
sudo ubuntu-maintenance --help
```

Available options:

* `--help` → Show help
* `--dry-run` → Simulate actions
* `--security` → Security updates only
* `--remove-kernels` → Remove old kernels

---

# 🧪 Example Commands

```bash
sudo ubuntu-maintenance
sudo ubuntu-maintenance --dry-run
sudo ubuntu-maintenance --security
sudo ubuntu-maintenance --remove-kernels
```

---

# ⚠️ Notes

* Requires `sudo` privileges
* Designed for Ubuntu/Debian systems
* Use `--dry-run` before running destructive actions

---

# 📌 Tips

* Place your tool in `/usr/local/bin` for global access
* Use versioning in the control file for updates
* Keep your script lightweight and safe

---

# 📄 License

MIT License
