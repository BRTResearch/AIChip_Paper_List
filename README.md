# AI Chip Paper List
## Table of Contents

 - [About This Project](#about-this-project)
 - [The Chronological Listing of Papers](#the-chronological-listing-of-papers)
   -    [ISCA](#ISCA)
   -    [ASPLOS](#ASPLOS)
   -    [MICRO](#MICRO)
   -    [HPCA](#HPCA)


## About This Project
  This project is to help engineers, researchers and students easily finding and learning the good ideas and designs in AI-related fields presented in the top-tier architecture conferences (ISCA, MICRO, ASPLOS, HPCA), such as AI/ML/DL accelerators, chips, and systems. We also try to give some hinds to these papers by adding some tags or notes based on our understanding and expand to more sources gradually. Please let us know if you have any comments or want to contribute.

## The Chronological Listing of Papers


<br>
We list all the papers we have collected. If it is linkable; it is linked to the summary/paper/slides of the paper. The links are still updating.<br>

## ISCA 
### 2019

| Tags                                                                     | \- | Title                                                                                                                                                                                                                                                   | Authors                                             | Affiliations                                                          |
|--------------------------------------------------------------------------|----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------|
| Inference;                                                               | 1  | 3D\-based Video Recognition Acceleration by Leveraging Temporal Locality                                                                                                                                                                                | Huixiang Chen; Tao Li                               | University of Florida                                                 |
| Inference;  Quantum                                                      | 2  | A Stochastic\-Computing based Deep Learning Framework using Adiabatic Quantum\-Flux\-Parametron Superconducting Technology                                                                                                                              | Ruizhe Cai; Ao Ren; Nobuyuki Yoshikawa; Yanzhi Wang | Northeastern University                                               |
| Training;  RL; Distributed training                                      | 3  | Accelerating Distributed Reinforcement Learning with In\-Switch Computing <br><a href="Summarys/2019/Accelerating Distributed Reinforcement Learning with In\-Switch Computing\.docx">summary                                                           | Youjie Li; Jian Huang                               | UIUC                                                                  |
| Training;  Sparsity                                                      | 4  | Eager Pruning: Algorithm and Architecture Support for Fast Training of Deep Neural Networks <br><a href="Summarys/2019/Eager Pruning Algorithm and Architecture Support for Fast Training of Deep Neural Networks\.docx">summary                        | Jiaqi Zhang; Tao Li                                 | University of Florida                                                 |
| Inference;  Sparsity; Bit\-serial                                        | 5  | Laconic Deep Learning Inference Acceleration <br><a href="Summarys/2019/Laconic Deep Learning Inference Acceleration\.docx">summary                                                                                                                     | Sayeh Sharify; Andreas Moshovos                     | University of Toronto                                                 |
| Inference; Memory; bandwidth\-saving; large\-scale networks; compression | 6  | MnnFast: A Fast and Scalable System Architecture for Memory\-Augmented Neural Networks <br><a href="Summarys/2019/MnnFast A Fast and Scalable System Architecture for Memory\-Augmented Neural Network\.docx">summary                                   | Hanhwi Jang; Jangwoo Kim                            | POSTECH; Seoul National University                                    |
| Inference;  ReRAM; Sparsity                                              | 7  | Sparse ReRAM Engine: Joint Exploration of Activation and Weight Sparsity in Compressed Neural Networks <br><a href="Summarys/2019/Sparse ReRAM Engine Joint Exploration of Activation and Weight Sparsity in Compressed Neural Networks\.docx">summary  | Tzu\-Hsien Yang                                     | National Taiwan University; Academia Sinica; Macronix International\. |
| Infernce;  Redundant computing                                           | 8  | TIE: Energy\-efficient Tensor Train\-based Inference Engine for Deep Neural Network <br><a href="Summarys/2019/TIE Energy\-efficient Tensor Train\-based Inference Engine for Deep Neural Network\.docx">summary                                        | Chunhua Deng; Bo Yuan                               | Rutgers University                                                    |
| Training;  CNN; floating point                                           | 9  | FloatPIM\_ in\-memory acceleration of deep neural network training with high precision <br><a href="Summarys/2019/FloatPIM in\-memory acceleration of deep neural network training with high precision\.docx">summary                                   | Mohsen Imani; Tajana Rosing                         | UC San Diego                                                          |
| Training;  Programming model                                             | 10 | Cambricon\-F\_ machine learning computers with fractal von neumann architecture <br><a href="Summarys/2019/Cambricon\-F Machine Learning Computers with Fractal von Neumann Architecture\.docx">summary                                                 | Yongwei Zhao; Yunji Chen                            | ICT; Cambricon                                                        |
| Tags                                                                     | 11 | Master of none acceleration\_ a comparison of accelerator architectures for analytical query processing <br><a href="Summarys/2019/Master of None Acceleration A Comparison of Accelerator Architectures for Analytical Query Processing\.docx">summary | Andrea Lottarini; Martha A\. Kim                    | Google; Columbia University                                           |
<br>

### 2018

| Tags                                           | \- | Title                                                                                                                                                                                                                                          | Authors                               | Affiliations                                                         |
|------------------------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|----------------------------------------------------------------------|
| Training;CNN; RNN                              | 1  | A Configurable Cloud\-Scale DNN Processor for Real\-Time AI <br><a href="Summarys/2018/A Configurable Cloud\-Scale DNN Processor for Real\-Time AI\.docx">summary                                                                              | Jeremy Fowers; Doug Burger            | Microsoft                                                            |
| Inference; ReRAM                               | 2  | PROMISE: An End\-to\-End Design of a Programmable Mixed\-Signal Accelerator for Machine\- Learning Algorithms                                                                                                                                  | Prakalp Srivastava; Mingu Kang        | University of Illinois at Urbana\-Champaign; IBM                     |
| Tags                                           | 3  | Computation Reuse in DNNs by Exploiting Input Similarity                                                                                                                                                                                       | Marc Riera; Antonio Gonza ?lez        | Universitat Polite ?cnica de Catalunya                               |
| Tags                                           | 4  | GenAx: A Genome Sequencing Accelerator <br><a href="Summarys/2018/GANAX A Unified MIMD\-SIMD Acceleration for Generative Adversarial Networks\.docx">summary                                                                                   | Daichi Fujiki; Satish Narayanasamy    | University of Michigan                                               |
| Tags                                           | 5  | Flexon: A Flexible Digital Neuron for Efficient Spiking Neural Network Simulations                                                                                                                                                             | Dayeol Lee; Jangwoo Kim               | Seoul National University; University of California                  |
| Tags                                           | 6  | Space\-Time Algebra: A Model for Neocortical Computation                                                                                                                                                                                       | James E\. Smith                       | University of Wisconsin\-Madison                                     |
| Tags                                           | 7  | Architecting a Stochastic Computing Unit with Molecular Optical Devices                                                                                                                                                                        | Xiangyu Zhang; Alvin R\. Lebeck       | Duke University; Parabon Labs                                        |
| Inference;NN\-DRAM                             | 8  | RANA: Towards Efficient Neural Acceleration with Refresh\-Optimized Embedded DRAM <br><a href="Summarys/2018/RANA Towards Efficient Neural Acceleration with Refresh\-Optimized Embedded DRAM \.docx">summary                                  | Fengbin Tu; Shaojun Wei               | Tsinghua University                                                  |
| Inference;Datapath: bit\-serial                | 9  | Neural Cache: Bit\-Serial In\-Cache Acceleration of Deep Neural Networks                                                                                                                                                                       | Charles Eckert; Reetuparna Das        | University of Michigan; Intel Corporation                            |
| Tags                                           | 10 | RoboX: An End\-to\-End Solution to Accelerate Autonomous Control in Robotics                                                                                                                                                                   | Jacob Sacks; Hadi Esmaeilzadeh        | Georgia Institute of Technology; University of California; San Diego |
| Inference;Vision\-NN codesign                  | 11 | EVA2: Exploiting Temporal Redundancy in Live Computer Vision                                                                                                                                                                                   | Mark Buckler; Adrian Sampson          | Cornell University                                                   |
| Inference;CNN; Vision\-NN codesign; low\-power | 12 | Euphrates: Algorithm\-SoC Co\-Design for Low\-Power Mobile Continuous Vision <br><a href="Summarys/2018/Euphrates Algorithm\-SoC Co\-Design for Low\-Power Mobile Continuous Vision\.docx">summary                                             | Yuhao Zhu; Paul Whatmough             | University of Rochetster; ARM Research                               |
| Inference;GAN;zero\-skipping; MIMD; SIMD       | 13 | GANAX: A Unified MIMD\-SIMD Acceleration for Generative Adversarial Networks <br><a href="Summarys/2018/GANAX A Unified MIMD\-SIMD Acceleration for Generative Adversarial Networks\.docx">summary                                             | Amir Yazdanbakhsh; Hadi Esmaeilzadeh  | Georgia Institute of Technology; UC San Diego; Qualcomm Technologies |
| Inference;  CNN; Approximate                   | 14 | SnaPEA: Predictive Early Activation for Reducing Computation in Deep Convolutional Neural Networks <br><a href="Summarys/2018/SnaPEA Predictive Early Activation for Reducing Computation in Deep Convolutional Neural Networks\.docx">summary | Vahideh Akhlaghi; Hadi Esmaeilzadeh   | Georgia Institute of Technology; UC San Diego; Qualcomm \.           |
| Inference;CNN; sparsity;                       | 15 | UCNN: Exploiting Computational Reuse in Deep Neural Networks via Weight Repetition <br><a href="Summarys/2018/UCNN Exploiting Computational Reuse in Deep Neural Networks via Weight Repetition\.docx">summary                                 | Kartik Hegde; Christopher W\. Fletche | University of Illinois at Urbana\-Champaign;  NVIDIA                 |
| Inference; Datapath: Quantization: Irregular   | 16 | Energy\-Efficient Neural Network Accelerator Based on Outlier\-Aware Low\-Precision Computation <br><a href="Summarys/2018/Energy\-efficient Neural Network Accelerator Based on Outlier\-aware Low\-precision Computation\.docx">summary      | Eunhyeok Park; Sungjoo Yoo            | Seoul National University                                            |
| Inference; Dataflow: Dynamic                   | 17 | Prediction Based Execution on Deep Neural Networks                                                                                                                                                                                             | Mingcong Song; Tao Li                 | University of Flirida                                                |
| Inference;  Datapath: bit\-serial              | 18 | Bit Fusion: Bit\-Level Dynamically Composable Architecture for Accelerating Deep Neural Network                                                                                                                                                | Hardik Sharma; Hadi Esmaeilzadeh      | Georgia Institute of Technology; University of California            |
| Training;  memory: bandwith\-saving            | 19 | Gist: Efficient Data Encoding for Deep Neural Network Training                                                                                                                                                                                 | Animesh Jain; Gennady Pekhimenko      | Microsoft Research; University of Toronto; Univerity of Michigan     |
| Inference;  NN\-post\-processing\-codesign     | 20 | The Dark Side of DNN Pruning                                                                                                                                                                                                                   | Reza Yazdani; Antonio Gonza ?lez      | Universitat Polite ?cnica de Catalunya                               |
<br>

### 2017

| Tags                                     | \- | Title                                                                                                                                                                                        | Authors                                  | Affiliations                                                 |
|------------------------------------------|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|--------------------------------------------------------------|
| Inference                                | 1  | In\-Datacenter Performance Analysis of a Tensor Processing Unit                                                                                                                              | Norman P\. Jouppi                        | Google                                                       |
| Inference; Dataflow                      | 2  | Maximizing CNN Accelerator Efficiency Through Resource Partitioning                                                                                                                          | Yongming Shen                            | Stony Brook University                                       |
| Training                                 | 3  | SCALEDEEP: A Scalable Compute Architecture for Learning and Evaluating Deep Networks                                                                                                         | Swagath Venkataramani; Anand Raghunathan | Purdue University; Parallel Computing Lab; Intel Corporation |
| Inference; Algorithm\-hardware\-codesign | 4  | Scalpel: Customizing DNN Pruning to the Underlying Hardware Parallelism                                                                                                                      | Jiecao Yu; Scott Mahlke                  | University of Michigan; ARM                                  |
| Inference; Sparsity                      | 5  | SCNN: An Accelerator for Compressed\-sparse Convolutional Neural Networks <br><a href="Summarys/2017/SCNN An Accelerator for Compressed\-sparse Convolutional Neural Networks\.docx">summary | Angshuman Parashar; William J\. Dally    | NVIDIA; MIT; UC\-Berkeley; Stanford University               |
| Tags                                     | 6  | Stream\-Dataflow Acceleration                                                                                                                                                                | Tony Nowatzki                            | University of California; University of Wisconsin            |
| Training;Datapath: quantization          | 7  | Understanding and Optimizing Asynchronous Low\-Precision Stochastic Gradient Descent                                                                                                         | Christopher De Sa; Kunle Olukotun        | Stanford University                                          |
<br>


### 2016
| Tags                                        | \- | Title                                                                                                                                                                                                                      | Authors                              | Affiliations                                          |
|---------------------------------------------|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|-------------------------------------------------------|
| Inference; Datapath: Sparsity               | 1  | Cnvlutin: Ineffectual\-Neuron\-Free Deep Neural Network Computing <br><a href="Summarys/2016/Cnvlutin Ineffectual\-Neuron\-Free Deep Neural Network Computing \.docx">summary                                              | Jorge Albericio; Tayler Hetheringto  | University of Toronto; University of British Columbia |
| Inference; Analog                           | 2  | ISAAC: A Convolutional Neural Network Accelerator with In\-Situ Analog Arithmetic in Crossbars                                                                                                                             | Ali Shafiee; Vivek Srikumar          | University of Utah，Hewlett Packard Labs               |
| Inference; PIM                              | 3  | PRIME: A Novel Processing\-in\-Memory Architecture for Neural Network Computation in ReRAM\-Based Main Memory                                                                                                              | Ping Chi; Yuan Xie                   | University of California                              |
| Inference; Sparsity                         | 4  | EIE: Efficient Inference Engine on Compressed Deep Neural Network                                                                                                                                                          | Song Han; William J\. Dally          | Stanford University; NVIDIA                           |
| Inference; Analog                           | 5  | RedEye: Analog ConvNet Image Sensor Architecture for Continuous Mobile                                                                                                                                                     | Robert LiKamWa; Lin Zhong            | Rice University                                       |
| Inference; Architecture\-Physical\-Codesign | 6  | Minerva: Enabling Low\-Power; Highly\-Accurate Deep Neural Network Accelerators <br><a href="Summarys/2016/Minerva Enabling Low\-Power; Highly\-Accurate Deep Neural Network Accelerators \.docx">summary                  | Brandon Reagen; David Brooks         | Harvard University                                    |
| Inference; Dataflow                         | 7  | Eyeriss: A Spatial Architecture for Energy\-Efficient Dataflow for Convolutional Neural Networks                                                                                                                           | Yu\-Hsin Chen; Vivienne Sze          | MIT; NVIDIA                                           |
| Inference; 3D integration                   | 8  | Neurocube: A Programmable Digital Neuromorphic Architecture with High\-Density 3D Memory <br><a href="Summarys/2016/Neurocube A Programmable Digital Neuromorphic Architecture with High\-Density 3D Memory\.docx">summary | Duckhwan Kim; Saibal Mukhopadhyay    | Georgia Institute of Technology                       |
| Inference                                   | 9  | Cambricon: An Instruction Set Architecture for Neural Networks <br><a href="Summarys/2016/Cambricon An Instruction Set Architecture for Neural Networks\.docx">summary                                                     | Shaoli Liu; Tianshi Chen             | CAS; Cambricon Ltd\.                                  |
| Tags                                        | 10 | Energy Efficient Architecture for Graph Analytics Accelerators <br><a href="Summarys/2016/Energy Efficient Architecture for Graph Analytics Accelerators\.docx">summary                                                    | Muhammet Mustafa Ozdal; Ozcan Ozturk | Bilkent University                                    |
| Tags                                        | 11 | Accelerating Markov Random Field Inference Using Molecular Optical Gibbs Sampling Units <br><a href="Summarys/2016/Accelerating Markov Random Field Inference Using Molecular Optical Gibbs Sampling Units\.docx">summary  | Siyang Wang; Alvin R\. Lieberk       | Duke University                                       |
<br>

### 2015
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
| Inference; Vision\-NN\-codesign | 1  | ShiDianNao: Shifting Vision Processing Closer to the Sensor <br><a href="Summarys/2015/ShiDianNao Shifting Vision Processing Closer to the Sensor\.docx">summary | Zidong Du | ICT          |
<br>


## ASPLOS
### 2020
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Shredder: Learning Noise Distributions to Protect Inference Privacy.<br><a href="">paper|     |UCSD
|Tags|  |DNNGuard: An Elastic Heterogeneous DNN Accelerator Architecture against Adversarial Attacks.<br><a href="">paper|     |CAS; USC
|Tags|  |Interstellar: Using Halide’s Scheduling Language to Analyze DNN Accelerators.<br><a href="">paper|     |Stanford; THU
|Tags|  |DeepSniffer: A DNN Model Extraction Framework Based on Learning Architectural Hints.<br><a href="">paper|     |UCSB
|Tags|  |Prague: High-Performance Heterogeneity-Aware Asynchronous Decentralized Training.<br><a href="">paper|     |USC
|Tags|  |PatDNN: Achieving Real-Time DNN Execution on Mobile Devices with Pattern-based Weight Pruning.<br><a href="">paper|     |College of William and Mary; Northeastern ; USC
|Tags|  |Capuchin: Tensor-based GPU Memory Management for Deep Learning.<br><a href="">paper|     |HUST; MSRA; USC
|Tags|  |NeuMMU: Architectural Support for Efficient Address Translations in Neural Processing Units.<br><a href="">paper|     |KAIST
|Tags|  |FlexTensor: An Automatic Schedule Exploration and Optimization Framework for Tensor Computation on Heterogeneous System.<br><a href="">paper|     |PKU
|Tags|  |Orbital Edge Computing: Machine Inference in Space<br><a href="https://dl.acm.org/doi/10.1145/3373376.3378473">paper|     |CMU
<br>

### 2019
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |FA3C: FPGA-Accelerated Deep Reinforcement Learning.|     |Hongik University; SNU
|Tags|  |PUMA: A Programmable Ultra-efficient Memristor-based Accelerator for Machine Learning Inference.|     |Purdue; UIUC; HP
|Tags|  |FPSA: A Full System Stack Solution for Reconfigurable ReRAM-based NN Accelerator Architecture.|     |THU; UCSB
|Tags|  |Bit-Tactical: A Software/Hardware Approach to Exploiting Value and Bit Sparsity in Neural Networks.|     |Toronto; NVIDIA
|Tags|  |TANGRAM: Optimized Coarse-Grained Dataflow for Scalable NN Accelerators.|     |Stanford
|Tags|  |Packing Sparse Convolutional Neural Networks for Efficient Systolic Array Implementations: Column Combining Under Joint Optimization.|     |Harvard
|Tags|  |Split-CNN: Splitting Window-based Operations in Convolutional Neural Networks for Memory System Optimization.|     |IBM; Kyungpook National University
|Tags|  |HOP: Heterogeneity-Aware Decentralized Training.|     |USC; THU
|Tags|  |Astra: Exploiting Predictability to Optimize Deep Learning.|     |Microsoft
|Tags|  |ADMM-NN: An Algorithm-Hardware Co-Design Framework of DNNs Using Alternating Direction Methods of Multipliers.|     |Northeastern; Syracuse; SUNY; Buffalo; USC
|Tags|  |DeepSigns: An End-to-End Watermarking Framework for Protecting the Ownership of Deep Neural Networks.|     |UCSD
<br>

### 2018
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Bridging the Gap Between Neural Networks and Neuromorphic Hardware with A Neural Network Compiler.|     |Tsinghua; UCSB
|Tags|  |MAERI: Enabling Flexible Dataflow Mapping over DNN Accelerators via Reconfigurable Interconnects.|     |Georgia Tech
|Tags|  |VIBNN: Hardware Acceleration of Bayesian Neural Networks.|     |Syracuse University; USC
|Tags|  |Exploiting Dynamical Thermal Energy Harvesting for Reusing in Smartphone with Mobile Applications.|     |Guizhou University; University of Florida
|Tags|  |Potluck: Cross-application Approximate Deduplication for Computation-Intensive Mobile Applications.|     |Yale
<br>

### 2017
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Tetris: Scalable and Efficient Neural Network Acceleration with 3D Memory.|     |Stanford University
|Tags|  |SC-DCNN: Highly-Scalable Deep Convolutional Neural Network using Stochastic Computing.|     |Syracuse University; USC; The City College of New York
<br>

### 2015
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |PuDianNao: A Polyvalent Machine Learning Accelerator.|     |CAS; USTC; Inria
<br>

### 2014
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |DianNao: A Small-Footprint High-Throughput Accelerator for Ubiquitous Machine-Learning.|     |CAS; Inria
<br>

## MICRO
### 2019
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Wire-Aware Architecture and Dataflow for CNN Accelerators.|     |Utah
|Tags|  |ShapeShifter: Enabling Fine-Grain Data Width Adaptation in Deep Learning.|     |Toronto
|Tags|  |Simba: Scaling Deep-Learning Inference with Multi-Chip-Module-Based Architecture.|     |NVIDIA
|Tags|  |ZCOMP: Reducing DNN Cross-Layer Memory Footprint Using Vector Extensions.|     |Google; Intel
|Tags|  |Boosting the Performance of CNN Accelerators with Dynamic Fine-Grained Channel Gating.|     |Cornell
|Tags|  |SparTen: A Sparse Tensor Accelerator for Convolutional Neural Networks.|     |Purdue
|Tags|  |EDEN: Enabling Approximate DRAM for DNN Inference using Error-Resilient Neural Networks.|     |ETHZ; CMU
|Tags|  |eCNN: a Block-Based and Highly-Parallel CNN Accelerator for Edge Inference.|     |NTHU
|Tags|  |TensorDIMM: A Practical Near-Memory Processing Architecture for Embeddings and Tensor Operations in Deep Learning.|     |KAIST
|Tags|  |Understanding Reuse; Performance; and Hardware Cost of DNN Dataflows: A Data-Centric Approach.|     |Georgia Tech; NVIDIA
|Tags|  |MaxNVM: Maximizing DNN Storage Density and Inference Efficiency with Sparse Encoding and Error Mitigation.|     |Harvard; Facebook
|Tags|  |Neuron-Level Fuzzy Memoization in RNNs.|     |UPC
|Tags|  |Manna: An Accelerator for Memory-Augmented Neural Networks.|     |Purdue; Intel
|Tags|  |eAP: A Scalable and Efficient In-Memory Accelerator for Automata Processing.|     |Virginia
|Tags|  |ComputeDRAM: In-Memory Compute Using Off-the-Shelf DRAMs.|     |Princeton
|Tags|  |ExTensor: An Accelerator for Sparse Tensor Algebra.|     |UIUC; NVIDIA
|Tags|  |Efficient SpMV Operation for Large and Highly Sparse Matrices Using Scalable Multi-Way Merge Parallelization.|     |CMU
|Tags|  |Sparse Tensor Core: Algorithm and Hardware Co-Design for Vector-wise Sparse Neural Networks on Modern GPUs.|     |UCSB; Alibaba
|Tags|  |DynaSprint: Microarchitectural Sprints with Dynamic Utility and Thermal Management.|     |Waterloo; ARM; Duke
|Tags|  |MEDAL: Scalable DIMM based Near Data Processing Accelerator for DNA Seeding Algorithm.|     |UCSB; ICT
|Tags|  |Tigris: Architecture and Algorithms for 3D Perception in Point Clouds.|     |Rochester
|Tags|  |ASV: Accelerated Stereo Vision System.|     |Rochester
|Tags|  |Alleviating Irregularity in Graph Analytics Acceleration: a Hardware/Software Co-Design Approach.<br><a href="">paper|     |UCSB; ICT
|Tags|  |A Scalable and Efficient in-Memory Interconnect Architecture for Automata Processing.<br><a href="https://dl.acm.org/doi/pdf/10.1145/3352460.3358324">paper|     |Virginia
<br>

### 2018
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Addressing Irregularity in Sparse Neural Networks: A Cooperative Software/Hardware Approach.|     |USTC; CAS
|Tags|  |Diffy: a Deja vu-Free Differential Deep Neural Network Accelerator.|     |University of Toronto
|Tags|  |Beyond the Memory Wall: A Case for Memory-centric HPC System for Deep Learning.|     |KAIST
|Tags|  |Towards Memory Friendly Long-Short Term Memory Networks(LSTMs) on Mobile GPUs.|     |University of Houston; Capital Normal University
|Tags|  |A Network-Centric Hardware/Algorithm Co-Design to Accelerate Distributed Training of Deep Neural Networks.|     |UIUC; THU; SJTU; Intel; UCSD
|Tags|  |PermDNN: Efficient Compressed Deep Neural Network Architecture with Permuted Diagonal Matrices.|     |City University of New York; University of Minnesota; USC
|Tags|  |GeneSys: Enabling Continuous Learning through Neural Network Evolution in Hardware.|     |Georgia Tech
|Tags|  |Processing-in-Memory for Energy-efficient Neural Network Training: A Heterogeneous Approach.|     |UCM; UCSD; UCSC
|Tags|  |LerGAN: A Zero-free; Low Data Movement and PIM-based GAN Architecture.|     |THU; University of Florida
|Tags|  |Multi-dimensional Parallel Training of Winograd Layer through Distributed Near-Data Processing.|     |KAIST
|Tags|  |SCOPE: A Stochastic Computing Engine for DRAM-based In-situ Accelerator.|     |UCSB; Samsung
|Tags|  |Morph: Flexible Acceleration for 3D CNN-based Video Understanding.|     |UIUC
|Tags|  |Inter-thread Communication in Multithreaded; Reconfigurable Coarse-grain Arrays.|     |Technion
|Tags|  |An Architectural Framework for Accelerating Dynamic Parallel Algorithms on Reconfigurable Hardware.|     |Cornell
<br>

### 2017
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Bit-Pragmatic Deep Neural Network Computing.|     |NVIDIA; University of Toronto
|Tags|  |CirCNN: Accelerating and Compressing Deep Neural Networks Using Block-Circulant Weight Matrices.|     |Syracuse University; City University of New York; USC; California State University; Northeastern University
|Tags|  |DRISA: A DRAM-based Reconfigurable In-Situ Accelerator.|     |UCSB; Samsung
|Tags|  |Scale-Out Acceleration for Machine Learning.|     |Georgia Tech; UCSD
|Tags|  |DeftNN: Addressing Bottlenecks for DNN Execution on GPUs via Synapse Vector Elimination and Near-compute Data Fission.|     |Univ. of Michigan; Univ. of Nevada
|Tags|  |Data Movement Aware Computation Partitioning.|     |PSU; TOBB University of Economics and Technology
  |Tags|  |Partition computation on a manycore system for near data processing.|     |PSU; TOBB University of Economics and Technology
<br>

### 2016
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |From High-Level Deep Neural Models to FPGAs.|     |Georgia Institute of Technology; Intel
|Tags|  |vDNN: Virtualized Deep Neural Networks for Scalable; Memory-Efficient Neural Network Design.|     |NVIDIA
|Tags|  |Stripes: Bit-Serial Deep Neural Network Computing.|     |University of Toronto; University of British Columbia
|Tags|  |Cambricon-X: An Accelerator for Sparse Neural Networks.|     |Chinese Academy of Sciences
|Tags|  |NEUTRAMS: Neural Network Transformation and Co-design under Neuromorphic Hardware Constraints.|     |Tsinghua University; UCSB
|Tags|  |Fused-Layer CNN Accelerators.|     |Stony Brook University
|Tags|  |Bridging the I/O Performance Gap for Big Data Workloads: A New NVDIMM-based Approach.|     |The Hong Kong Polytechnic University; NSF/University of Florida
|Tags|  |A Patch Memory System For Image Processing and Computer Vision.|     |NVIDIA
|Tags|  |An Ultra Low-Power Hardware Accelerator for Automatic Speech Recognition.|     |Universitat Politecnica de Catalunya
|Tags|  |Perceptron Learning for Reuse Prediction.|     |TAMU; Intel Labs
|Tags|  |A Cloud-Scale Acceleration Architecture.|     |Microsoft Research
|Tags|  |Reducing Data Movement Energy via Online Data Clustering and Encoding.|     |University of Rochester
|Tags|  |The Microarchitecture of a Real-time Robot Motion Planning Accelerator.|     |Duke University
|Tags|  |Chameleon: Versatile and Practical Near-DRAM Acceleration Architecture for Large Memory Systems.|     |UIUC; Seoul National University
<br>

### 2014
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |DaDianNao: A Machine-Learning Supercomputer.|     |CAS; Inria; Inner Mongolia University
<br>


## HPCA
### 2020
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Accelerator; memristor|  |Deep Learning Acceleration with Neuron-to-Memory Transformation.<br><a href="https://pdfs.semanticscholar.org/3df4/37d399746e41dd63fe8d46734a3a8523654d.pdf?_ga=2.85586201.1813124284.1587000449-973045201.1587000449">Paper  |     |UCSD
|graph network; computation patterns; accelerator|  |HyGCN: A GCN Accelerator with Hybrid Architecture.<br><a href="https://arxiv.org/pdf/2001.02514.pdf">Paper  |     |ICT; UCSB
|training; accelerator; sparse|  |SIGMA: A Sparse and Irregular GEMM Accelerator with Flexible Interconnects for DNN Training.<br><a href="https://synergy.ece.gatech.edu/wp-content/uploads/sites/332/2020/01/sigma_hpca2020.pdf">Paper  <a href="https://synergy.ece.gatech.edu/wp-content/uploads/sites/332/2020/03/HPCA2020-SIGMA-talk.pdf">Slides|     |Georgia Tech
|Multi-task; architecture; DNN|  |PREMA: A Predictive Multi-task Scheduling Algorithm For Preemptible NPUs.<br><a href="https://arxiv.org/pdf/1909.04548.pdf">Paper  |     |KAIST
|acceleartor; configurable; sparse|  |ALRESCHA: A Lightweight Reconfigurable Sparse-Computation Accelerator.<br><a href="https://www.prism.gatech.edu/~basgari3/papers/asgari-hpca20.pdf">Paper  |     |Georgia Tech
|accelerator; sparse; Huffman-Tree; Matrix Multiplication|  |SpArch: Efficient Architecture for Sparse Matrix Multiplication.<br><a href="https://hanlab.mit.edu/projects/sparch/assets/HPCA2020_SpArch.pdf">Paper  <a href="https://hanlab.mit.edu/projects/sparch/">Project|     |MIT; NVIDIA
|accelerator; attention algorithm|  |A3: Accelerating Attention Mechanisms in Neural Networks with Approximation.<br><a href="https://www.cs.princeton.edu/~tae/a3_hpca2020.pdf">Paper  |     |SNU
|Accelarator; training; cost model; design space|  |AccPar: Tensor Partitioning for Heterogeneous Deep Learning Accelerator Arrays.<br><a href="http://alchem.usc.edu/portal/static/download/accpar.pdf">Paper  |     |Duke; USC
|Tags|  |PIXEL: Photonic Neural Network Accelerator.|     |Ohio; George Washington
|recommendation; workloads; performance metrics|  |The Architectural Implications of Facebook’s DNN-based Personalized Recommendation.<br><a href="https://research.fb.com/wp-content/uploads/2020/02/The-Architectural-Implications-of-Facebook%E2%80%99s-DNN-based-Personalized-Recommendation.pdf?">Paper  |     |Facebook
|Capasule; computing Arch.; processing-in- memory|  |Enabling Highly Efficient Capsule Networks Processing Through A PIM-Based Architecture Design.<br><a href="https://arxiv.org/pdf/1911.03451.pdf">Paper  |     |Houston
|Tags|  |Missing the Forest for the Trees: End-to-End AI Application Performance in Edge Data.<br><a href="https://www.sigarch.org/wp-content/uploads/2020/03/AI_Tax_Missing_the_Forest_for_the_Trees_HPCA2020.pdf">Slides|     |UT Austin; Intel
|accelerator; communication; Lower bound|  |Communication Lower Bound in Convolution Accelerators.<br><a href="https://arxiv.org/pdf/1911.05662.pdf">Paper|     |ICT; THU
|Tags|  |Fulcrum: a Simplified Control and Access Mechanism toward Flexible and Practical in-situ Accelerators.|     |Virginia; UCSB; Micron
|Tags|  |EFLOPS: Algorithm and System Co-design for a High Performance Distributed Training Platform.|     |Alibaba
|ML; NoC; Design Space|  |Experiences with ML-Driven Design: A NoC Case Study.<br><a href="http://jiemingyin.github.io/docs/HPCA2020.pdf">Paper|     |AMD
|Accelerator; sparse; Tensor factorization|  |Tensaurus: A Versatile Accelerator for Mixed Sparse-Dense Tensor Computations.<br><a href="https://www.csl.cornell.edu/~zhiruz/pdfs/tensaurus-hpca2020.pdf">Paper |     |Cornell; Intel
|codesign; computing Arch.|  |A Hybrid Systolic-Dataflow Architecture for Inductive Matrix Algorithms.<br><a href="http://web.cs.ucla.edu/~tjn/papers/hpca2020-revel.pdf">Paper |     |UCLA
|ML; NoC; Design Space|  |A Deep Reinforcement Learning Framework for Architectural Exploration: A Routerless NoC Case Study.<br><a href="http://web.engr.oregonstate.edu/~chenliz/publications/2020_HPCA_Deep%20Reinforcement%20Learning%20for%20Routerless%20NoC.pdf">Paper  |     |USC; OSU
|Tags|  |QuickNN: Memory and Performance Optimization of k-d Tree Based Nearest Neighbor Search for 3D Point Clouds.<br>Paper|     |Umich; General Motors
|mobile; energy efficiency|  |Techniques for Reducing the Connected-Standby Energy Consumption of Mobile Devices.<br><a href="https://people.inf.ethz.ch/omutlu/pub/mobile-idle-power-management-intel-skylake_hpca20.pdf">Paper |     |ETHZ; Cyprus; CMU
<br>

### 2019
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |HyPar: Towards Hybrid Parallelism for Deep Learning Accelerator Array.|     |Duke; USC
|Tags|  |E-RNN: Design Optimization for Efficient Recurrent Neural Networks in FPGAs.|     |Syracuse University; Northeastern University; Florida International University; USC; University at Buffalo
|Tags|  |Bit Prudent In-Cache Acceleration of Deep Convolutional Neural Networks.|     |Michigan; Intel
|Tags|  |Shortcut Mining: Exploiting Cross-layer Shortcut Reuse in DCNN Accelerators.|     |OSU
|Tags|  |NAND-Net: Minimizing Computational Complexity of In-Memory Processing for Binary Neural Networks.|     |KAIST
|Tags|  |Kelp: QoS for Accelerators in Machine Learning Platforms.|     |Microsoft; Google; UT Austin
|Tags|  |Machine Learning at Facebook: Understanding Inference at the Edge.|     |Facebook
|Tags|  |The Accelerator Wall: Limits of Chip Specialization.|     |Princeton
<br>

### 2018
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |Making Memristive Neural Network Accelerators Reliable.|     |University of Rochester
|Tags|  |Towards Efficient Microarchitectural Design for Accelerating Unsupervised GAN-based Deep Learning.|     |University of Florida
|Tags|  |Compressing DMA Engine: Leveraging Activation Sparsity for Training Deep Neural Networks.|     |POSTECH; NVIDIA; UT-Austin
|Tags|  |In-situ AI: Towards Autonomous and Incremental Deep Learning for IoT Systems.|     |University of Florida; Chongqing University; Capital Normal University
|Tags|  |RC-NVM: Enabling Symmetric Row and Column Memory Accesses for In-Memory Databases.|     |PKU; NUDT; Duke; UCLA; PSU
|Tags|  |GraphR: Accelerating Graph Processing Using ReRAM.|     |Duke; USC; Binghamton University SUNY
|Tags|  |GraphP: Reducing Communication of PIM-based Graph Processing with Efficient Data Partition.|     |THU; USC; Stanford
|Tags|  |PM3: Power Modeling and Power Management for Processing-in-Memory.|     |PKU
<br>

### 2017
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |FlexFlow: A Flexible Dataflow Accelerator Architecture for Convolutional Neural Networks.|     |Chinese Academy of Sciences
|Tags|  |PipeLayer: A Pipelined ReRAM-Based Accelerator for Deep Learning.|     |University of Pittsburgh; University of Southern California
|Tags|  |Towards Pervasive and User Satisfactory CNN across GPU Microarchitectures.|     |University of Florida
|Tags|  |Supporting Address Translation for Accelerator-Centric Architectures.|     |UCLA
<br>

### 2016
| Tags                            | \- | Title                                                                                                                                                            | Authors   | Affiliations |
|---------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------------|
|Tags|  |A Performance Analysis Framework for Optimizing OpenCL Applications on FPGAs.|     |Nanyang Technological University; HKUST; Cornell University
|Tags|  |TABLA: A Unified Template-based Architecture for Accelerating Statistical Machine Learning.|     |Georgia Institute of Technology
|Tags|  |Memristive Boltzmann Machine: A Hardware Accelerator for Combinatorial Optimization and Deep Learning.|     |University of Rochester
<br>