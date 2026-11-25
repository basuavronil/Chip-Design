<img width="1266" height="1022" alt="image" src="https://github.com/user-attachments/assets/74653813-5a02-453c-a030-7444228961d2" />

Crystal oscillator: An off-chip component that vibrates at a fixed frequency and gives the chip a stable reference clock. Without it, the PLL has nothing to lock to, so no clock is generated and the chip stays frozen.

Power supply: The off-chip source (battery or board regulator) that provides the voltage the chip runs on. Without it, nothing on the chip works, because transistors can't switch without power.

Clock, reset and power management (PLL, PMU): The support block that multiplies the crystal clock into high-speed clocks, controls reset at startup and manages each block's voltage and power state. Without it, blocks would have no usable clock, would start in random states and would waste power. The chip would be unreliable, hot and power-hungry, even if parts of it worked.

CPU cores: The general-purpose processors, with L1/L2 cache, that run the operating system and program instructions and control the rest of the chip. Without them, nothing decides what the other blocks do and no software runs, so the chip is a collection of idle hardware.

GPU / NPU: Accelerators built to do many simple calculations in parallel, such as graphics (GPU) and AI inference (NPU). Without them, the CPU would do this work. The chip would still function but be much slower and use more power on graphics and AI tasks.

DSP / ISP: Specialised processors for signal work, with the DSP handling audio and radio and the ISP handling camera images. Without them, the CPU would process this data, which costs speed and battery life, and camera and audio quality would suffer.

System interconnect (AMBA bus / NoC): The communication network that lets all the blocks send data and requests to each other. Without it, blocks can't talk, so the CPU couldn't reach memory or peripherals. Wiring every block directly to every other would be impractical as the chip grows.

Memory controller: The block that talks to the external DRAM, handling its timing, addresses and refresh. Without it, the chip can't use DRAM and is limited to the small on-chip SRAM, so it couldn't run an operating system or large applications.

On-chip SRAM (cache, ROM): Small, very fast memory on the die, holding cache and boot code in ROM. Without it, every access would go to slow DRAM, which cripples performance, and the chip would have no boot code, so it couldn't even start.

Peripherals (UART, SPI, I2C): Interfaces for simple, slow devices such as sensors, debug consoles and small chips. Without them, the chip couldn't talk to these devices or be debugged easily.

I/O interface (PCIe, USB): High-speed links to the outside world, such as storage, a host computer and expansion devices. Without it, the chip would have no fast path to storage, the host or other chips.

External DRAM: Large, cheap memory off the chip that holds the OS, applications and working data. Without it, the chip would have only the tiny SRAM, which is enough for simple firmware but not for a modern OS or apps.

Off-chip devices (sensors, display, host): The real-world devices the chip senses and controls. Without them, the chip would run internally but have nothing to read from or show output on, so it would be of no practical use.
