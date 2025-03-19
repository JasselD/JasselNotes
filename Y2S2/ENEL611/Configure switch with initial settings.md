**Switch Boot Sequence
5 steps before configuring a switch
1. **POST (Power-On Self-Test):** The switch checks the CPU, DRAM, and flash file system.
2. **Boot Loader Loads:** A small program in ROM runs after POST.
3. **CPU Initialization:** Boot loader sets up CPU registers and memory.
4. **Flash File System Initialization:** Boot loader prepares storage.
5. **IOS Loading:** Boot loader loads the IOS and transfers control to it.

**Boot System Command
1. **Boot Process:** The switch uses the BOOT environment variable to locate the IOS image.
2. **Fallback Mechanism:** If BOOT is not set, it loads the first available executable file.
3. **Catalyst 2960 Behavior:** The IOS image is typically stored in a directory named after the image (excluding `.bin`).
4. **IOS Initialization:** The switch loads the `startup-config` (`config.text` in flash) to configure interfaces.
5. **Viewing Boot Settings:** Use `show boot` to check the current IOS boot file.
Commands:
```Command
S1(config)# boot system flash:/c2960-lanbasek9-mz.150-2.SE/c2960-lanbasek9-mz.150-2.SE.bin
```

**![[Pasted image 20250319231015.png]]**

[[LED Indication]]
