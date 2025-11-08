# Taylor Bubble Detection and Tracking System

This project implements a **Taylor bubble detection and tracking system** for mechanical engineering fluid dynamics research. The system combines **Mask R-CNN** for precise bubble segmentation with **OC-SORT** tracking algorithm to analyze bubble characteristics across different flow velocities in continuous flow reactors and to measure slug length using a edge based method, the final output will be Gradio web app for quick analysis.

### Core Capabilities
-  **Custom Mask R-CNN** trained on annotated bubble images  
-  **Real-time OC-SORT tracking** with unique bubble ID assigned
-  **Precise radius measurement** using instance segmentation masks and contour analysis
-  Edge-based slug length measurement** using left/right bubble boundaries
-  **Automated CSV export** with bubble metrics in tablueaur
-  **Google Colab** for easy deployment

### Research Context
This work was a continouation part of my dissertation project at **University of Birmingham MSc Robotics** research collaboration on Taylor bubble dynamics in microfluidic systems for advanced manufacturing quality control system.

## System Architecture

```
Input Videos → Mask R-CNN Detection → OC-SORT Tracking → Radius Calculation → slug length measurement → CSV format
     ↓              ↓                      ↓                    ↓              ↓                           ↓
Taylor Flow    Bubble Segmentation   Multi-Object         Contour Analysis   Research Data                           
   Videos         (187 trained         Tracking           & Measurements      for Analysis                           
                   annotations)     (Unique Track IDs)                                                               
```

![WhatsApp Image 2025-11-08 at 14 13 27_704902f1](https://github.com/user-attachments/assets/07703e9e-f51e-4351-a451-9550f5ee371e)
Taylor bubble flow analysis setup with backlight and precision flow channel for real time imaging





## Getting Started

### Prerequisites

- Python 3.8+
- T4 GPU 
- Google Colab account (optional)

## Results

### Model Performance
- **Mask R-CNN mAP@0.5**: 88.3% on bubble segmentation
- **Processing Speed**: ~15 FPS on GPU (RTX 3080)
- **Tracking Accuracy**: 95%+ bubble ID consistency

### Research Findings
| Flow Velocity | Avg Bubble Radius | Std Deviation | Bubble Count |
|---------------|-------------------|---------------|--------------|
| 0.5 ml/min    | 24.5 pixels      | 3.2 pixels    | 1,247        |
| 1.0 ml/min    | 22.8 pixels      | 4.1 pixels    | 1,856        |
| 2.0 ml/min    | 19.3 pixels      | 2.8 pixels    | 2,334        |


## Progress update

- [x] Custom Mask R-CNN training on bubble dataset
- [x] OC-SORT integration for multi-object tracking  
- [x] Real-time radius measurement
- [x] Edge-based slug length and radius measurement implemented
- [ ] **Phase 2**: Gradio web app deployed for interactive analysis
- [ ] **Phase 3**: Integration with industrial flow controllers for live quality monitoring


## License

Distributed Under the 'MIT License'. See `LICENSE` for more information.

## Acknowledgments

- **University of Birmingham** - MSc Robotics Program + Dissertation project
- **Research Collaborators**: Faysal Ahmad, Fahad Rahman (PhD Mechanical Engineering)
- **Supervisor**: Dr. Jason Stafford
- **Infrastructure**: Google Colab Pro for GPU training resources


***
*Developed with ❤️ for leveraging AI in advancing fluid dynamics research*
