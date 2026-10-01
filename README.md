## Dataset Description

This dataset contains multi-channel acoustic signals collected from wind turbine blades with various surface fault conditions, designed for research on fault diagnosis and federated learning–based collaborative modeling.

The acoustic data were acquired using a microphone array composed of **three YG-201 microphones**, which were spatially distributed at equal distances from the tested blade and arranged with an **angular separation of 135°**. The microphones were positioned around the blade to capture aerodynamic noise radiated during blade operation, forming a **symmetric three-channel sensing configuration**.  
The tested blade has a **length of 750 mm**, and the experimental setup was mounted at a **height of 1.5 m above the ground**.

All microphone signals were synchronously recorded through a **data acquisition card**, and the three-channel acoustic data were transmitted to a PC for storage and post-processing. The **sampling rate was set to 48 kHz** for each channel, and the raw signals were segmented into fixed-length frames with a window length of 5120 samples.
The experiments were conducted in an **open indoor environment of approximately 50 m²**, with a **room temperature of around 20 °C**, so as to reduce environmental disturbances and ensure stable acoustic conditions.

---

## Fault Types and Severity Levels

The dataset includes **normal blades** and blades with **multiple representative fault types**, as illustrated in **Fig. 1**. Specifically, the fault categories include:
<img width="877" height="725" alt="fault_type" src="https://github.com/user-attachments/assets/171b8e98-93f5-4d75-a726-24f5ee7b8be2" />

### Surface roughening (polish / roughened)
- Slightly roughened  
- Severely roughened  

### Structural damage (crack)
- Slightly cracked  
- Severely cracked  

### Material loss (hole)
- Single hole  
- Double hole  

### Icing conditions (ice)
- Slight icing  
- Severe icing  

These fault types were **artificially introduced and carefully controlled** to represent different fault mechanisms and severity levels commonly encountered in real wind turbine blade operation. This design enables systematic analysis of both **inter-class differences** and **intra-class severity variations**.

---

## Federated Learning Dataset Construction

To support federated learning research, the raw multi-channel acoustic recordings were further processed into a **segmented sample-level dataset**.  
The continuous acoustic signals were divided into **fixed-length overlapping segments** using a sliding-window strategy, resulting in **labeled samples of three-channel time-series data**.

Based on these segmented samples, **federated learning datasets were constructed by partitioning the samples into multiple virtual clients**.  
Different client-wise data distributions were generated to simulate realistic cross-client heterogeneity, including **IID** and **Dirichlet-based non-IID** settings.

Ultimate Data will be provided on request and recommedned to be usesd.

