**Paper title:**

Techniques for Reducing the Connected-Standby Energy Consumption of Mobile
Devices.

**Publication:**

HPCA’20

**Problem to solve:**

To increase battery life in the connected-standby mode, a mobile device enters
the deepest-runtime-idle-power state (DRIPS), which minimizes power consumption
and retains fast wake-up capability. However, there exists energy inefficiency
in modern DRIPS designs.

**Major contribution:**

1.  Monitoring of wake-up events: Offloading the monitoring of wake-up events to
    low-power off-chip circuitry enables turning off all of the processor’s
    clock sources.

2.  I/O functions: offloads all of the processor’s input/output functionality
    off-chip and power gates the corresponding on-chip input/output functions.

3.  Reducing leakage power: transfers the processor’s context to a secure memory
    region inside DRAM, which eliminates the need to store the context using
    high-leakage on-chip SRAMs, thereby reducing leakage power.

**Lessons learnt:**

They implement ODRIPS in Intel’s Skylake client processor and its associated
Sunrise-Point chipset. Their analysis of ODRIPS on a real system reveals that it
reduces the platform average power consumption in connected-standby mode by 22%.

Referred to the first two contributions, the key idea of addressing the energy
inefficiency in handling the timer wake-up events in DRIPS is to 1) dynamically
migrate the timer event handling to the chipset and 2) toggle the timer with a
drastically slower clock. Compared to baseline DRIPS, this technique results in
lower power but longer entry and exit latencies.

Referred to the last contributions, the context SRAMs are powered with retention
voltage, which is the lowest possible power supply voltage at which the data can
be retained inside SRAM. Thus, it is not feasible to further reduce SRAM voltage
to save power in DRIPS. Storing the context in DRAM theoretically consumes
“zero” additional power, because in DRIPS the whole DRAM is anyway
self-refreshed to retain all data, and DRAM capacity is huge compared to the
size of the processor context (GBs vs KBs). Therefore, reserving a small area of
the DRAM for the context is feasible and inexpensive. However, processor context
includes sensitive information and configuration state. This raises a security
concern as several attacks, can be carried out on DRAM to reveal or change its
contents.
