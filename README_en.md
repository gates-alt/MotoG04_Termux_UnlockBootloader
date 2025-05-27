# MotoG04_Termux_UnlockBootloader

**Unlock the Bootloader of Moto G04/G04S devices using only another Android phone with Termux and an OTG cable — no computer needed.**

> [**Leia esta página em português**](https://github.com/gates-alt/MotoG04_Termux_UnlockBootloader/blob/main/README.md)

---

## **⚠️ Disclaimer ⚠️**

> **IMPORTANT NOTICE:**  
> I, [@gatesgsm](https://t.me/gatesgsm), the creator and maintainer of this project, **am not responsible** for any damage caused to your device when using the scripts or methods provided here.  
>  
> **Use at your own risk.** Be sure you fully understand the process before proceeding.

---

## **Need Help?**

If you experience issues or need help restoring your bootloaders, feel free to contact me via **Telegram**:  
**[@gatesgsm](https://t.me/gatesgsm)**

> Tip: The `restore_boot.sh` script usually resolves most boot-related issues.

---

## Compatibility

This project is **fully compatible with all models, variants, regions, and types** of **Moto G04 and Moto G04S**.

> Whenever I mention “Moto G04,” I’m also referring to the **Moto G04S**, as they share the same hardware and software base.

---

## **Requirements**

You will need:

- A **secondary Android phone** (host), where Termux will run
- Apps:
  - [**Termux**](https://f-droid.org/en/packages/com.termux/)
  - [**Termux:API**](https://f-droid.org/en/packages/com.termux.api/)
- An **OTG cable**
- A **USB data cable** (USB-A to USB-C)
- **Tweezers or other metal object (such as a paper clip) with two ends**

Optional:

- Suction cup
- Plastic spatula
(to remove the plastic cover)

---

## **Preparing the Testpoint**

To unlock your device (or connect it in **interactive FDL2 mode**), you must perform a **testpoint**, which involves opening the phone and touching a specific spot on the motherboard.

### **Helpful Videos:**

- [**Removing the Moto G04/G04S back cover**](https://youtube.com/shorts/x3WhoOhb4js?feature=shared)  
- [**How to do the testpoint on Moto G04/G04S**](https://youtu.be/QMFQPKndK64?feature=shared)

---

## **Installation and Usage**

### **1. Install the required apps**

Download [**Termux**](https://f-droid.org/en/packages/com.termux/) and [**Termux:API**](https://f-droid.org/en/packages/com.termux.api/) via **F-Droid** to ensure you're using the safest and most updated versions.

### **2. Grant Termux:API permissions**

Open **Termux:API** and grant any permissions it requests so that Termux can interact with your phone’s hardware.

### **3. Download and install the project**

In Termux, run:

```bash
curl -sL https://raw.githubusercontent.com/gates-alt/MotoG04_Termux_UnlockBootloader/main/install.sh | bash && cd MotoG04_Termux_UnlockBootloader
```

---

### **4. Prepare the connection**

- Plug the **OTG cable** into the host phone (the one running Termux).
- Plug the **USB-A** end of the data cable into the OTG adapter.
- **Do not connect the USB-C end to the Moto G04/G04S yet!**

---

### **5. Run the desired script**

Run any available script from the project. For example, to unlock the bootloader:

```bash
./unlockbootloader.sh
```

---

### **6. Perform the testpoint and connect the G04**

- After running the script in Termux, it will wait for the Moto G04 to be connected.
- Do the **testpoint** as shown in the videos above.
- **While holding the testpoint**, connect the USB-C cable to the Moto G04.
- A USB permission prompt may appear on the host phone — **grant it**.
- Wait for the process to finish.

---

## **Recovery with `restore_boot.sh`**

The `restore_boot.sh` script **does not use saved backups**.  
It uses **reliable bootloaders from the original firmware**, located in the `uboot_spl/` folder.

This approach avoids restoring potentially corrupted files and improves safety.

---

## **How to use `restore_boot.sh`**

Use this script to **recover a bricked Moto G04**, meaning a phone that **won’t boot or enter fastboot mode**.

### **Recovery Steps:**

1. Connect the OTG cable to the host phone and plug in the USB-A end of the data cable.
2. **Keep the USB-C end disconnected.**
3. Run the script in Termux:

```bash
./restore_boot.sh
```

4. **While the script is waiting:**
   - Connect the USB-C end to the Moto G04.
   - **Holding Volume Down may help**, but it's not mandatory.

5. If prompted, grant USB permissions and wait for completion.

---

## **Credits**

This project was made possible thanks to [**TomKing062**](https://github.com/TomKing062), who created the tools used here.

- The programs were **compiled and organized by me, [@gatesgsm](https://t.me/gatesgsm)**.
- Authorship and development belongs to TomKing062.

### **Original Repositories:**

- [spreadtrum_flash](https://github.com/TomKing062/spreadtrum_flash)  
- [CVE-2022-38694_unlock_bootloader](https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader)

---

## **Final Recommendations**

- Use **high-quality cables** to avoid connection issues.
- Never disconnect the phone or close Termux while a script is running.
- If something goes wrong, always try `restore_boot.sh` before attempting anything else.

---

## **Contact**

Need support or want to contribute?

- Telegram: [@gatesgsm](https://t.me/gatesgsm)
- GitHub: [github.com/gates-alt/MotoG04_Termux_UnlockBootloader](https://github.com/gates-alt/MotoG04_Termux_UnlockBootloader)
