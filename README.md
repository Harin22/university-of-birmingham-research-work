# Taylor Bubble Detection and Tracking System

This project implements a **Taylor bubble detection and tracking system** for mechanical engineering fluid dynamics research. The system combines **Mask R-CNN** for precise bubble segmentation with **OC-SORT** tracking algorithm to analyze bubble in continuous flow reactors and to measure slug length using a edge based method, the final output will be Gradio web app for quick analysis.

### Core Capabilities
-  **Custom Mask R-CNN** trained on annotated bubble images  
-  **Real-time OC-SORT tracking** with unique bubble ID assigned
-  **Precise radius measurement** using instance segmentation masks and contour analysis
-  Edge-based slug length measurement** using left/right bubble boundaries
-  **Automated CSV export** with bubble metrics in tablueaur
-  **Google Colab** for easy deployment

### Research Context
This work was a part of **University of Birmingham** research collaboration on Taylor bubble dynamics in microfluidic systems.

## System Architecture

```
Input Videos → Mask R-CNN Detection → OC-SORT Tracking → Radius Calculation → slug length measurement → CSV format
     ↓              ↓                      ↓                    ↓              ↓                           ↓
Taylor Flow    Bubble Segmentation   Multi-Object         Contour Analysis   Research Data                           
   Videos         (187 trained         Tracking           & Measurements      for Analysis                           
                   annotations)     (Unique Track IDs)                                                               
```

<div align="center">
  <img src="https://github.com/user-attachments/assets/07703e9e-f51e-4351-a451-9550f5ee371e" width="600">
  <p><em>Taylor bubble flow analysis setup with backlight and precision flow channel for real-time imaging.</em></p>
</div>


## Getting Started

### Prerequisites

- Python 3.8+
- T4 GPU 
- Google Colab account (optional)

## Results

<div align="center" style="display: flex; justify-content: center; gap: 10px;">

  <img src="https://github.com/user-attachments/assets/e5075a65-9e22-4544-8729-e66c15338655" 
       alt="Slug length measurement between Taylor bubbles" 
       width="47%" />

  <img src="https://github.com/user-attachments/assets/296677a5-cc93-492a-b92c-a534a3de5954" 
       alt="Taylor bubble radius and width estimation" 
       width="47%" />

  <br>
  <p><b>Left:</b> Edge-based slug length measurement between Taylor bubbles. <br>
     <b>Right:</b> Radius and width estimation of individual Taylor bubbles for geometric analysis.</p>

</div>


### Model Performance
- **Mask R-CNN mAP@0.5**: 88.3% on bubble segmentation
- **Processing Speed**: ~15 FPS on GPU (RTX 3080)
- **Tracking Accuracy**: 95%+ bubble ID consistency

### Research Findings
| Avg Bubble Radius | Std Deviation  | Bubble Count  |
|-------------------|----------------|---------------|
| 24.5 pixels       |  3.2 pixels    |  1,247        |
| 22.8 pixels       |  4.1 pixels    |  1,856        |
| 19.3 pixels       |  2.8 pixels    |  2,334        |


## Progress update

- [x] Custom Mask R-CNN training on bubble dataset
- [x] OC-SORT integration for multi-object tracking  
- [x] Real-time radius measurement
- [x] Edge-based slug length and radius measurement implemented
- [ ] **Phase 2**: Gradio web app deployed for interactive analysis
- [ ] **Phase 3**: Integration with lab flow controllers for live quality monitoring


## License

Distributed Under the 'MIT License'. See `LICENSE` for more information.


***
*Developed for leveraging AI in advancing fluid dynamics research*
