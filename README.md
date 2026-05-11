## **EEG-Controlled Exoskeleton for Walking and Standing – A Longitudinal Motor Imagery Study in Healthy Adults**
### **Dataset Overview**
This dataset comprises multimodal recordings from a brain–machine interface (BMI) training study involving seven healthy adult participants (ages 20–30 years; mean = 24.3, SD = 3.8). The study investigated both open-loop and closed-loop control of a lower-limb exoskeleton (Rex Bionics). The dataset includes 60-channel EEG, 4-channel EOG, motion data from two IMU sensors (mounted on the participant’s forehead and the exoskeleton), and exoskeleton control and feedback signals. Each participant completed nine sessions over several weeks, with each session structured into a training phase followed by a closed-loop trial phase.
### **Experimental Design**

- **Participants:** 7 healthy adults (4 male, 3 female)
- **Sessions:** 9 per participant
- **Training Phase:** Motor imagery calibration
- **Trial Phase:** Closed-loop BMI control (walk/stop)
- **Conditions:** Walk / Stop (motor imagery)

### **Task Structure**
**Training:**
Participants perform motor imagery tasks without feedback to calibrate the BMI decoder.

**TrialXX:**
Each session includes 12 closed-loop BMI trials (trial01–trial12), during which participants use motor imagery to control the exoskeleton in real time.

- **Block 1:** Trials 1–4
- **Block 2:** Trials 5–8
- **Block 3:** Trials 9–12

**walk6min / stop6min:**
After the 12 trials, participants complete two extended motor imagery tasks:

- **walk6min:** Imagining continuous walking for 6 minutes
- **stop6min:** Imagining standing still for 6 minutes

### **Data Modalities**

- **EEG:** 60 scalp channels + 4 EOG channels
- **IMU:** 3-axis accelerometer, gyroscope, magnetometer, and quaternion
- **Sensor Placement:** IMUs mounted on the participant’s forehead and the exosuit back brace
- **Decoder Signals / Feedback:** Logged control signals and BMI predictions

### **Additional Materials**

- **MIQ‑RS:** Motor Imagery Questionnaire – Revised Second Version (PDFs in `derivatives/MIQ-RS/`)
- **Validation Tables:** Data availability, synchronization, and electrode placement (`derivatives/validation/`)
- **Raw Data:** Provided without filtering or artifact removal

### **Folder Structure**

---

```
dataset-root/
│
├── sub-/
│   └── ses-/
│       ├── eeg/
│       │   ├── sub-_ses-_coordsystem.json
│       │   ├── sub-_ses-_electrodes.tsv
│       │   ├── sub-_ses-_electrodes.json
│       │   │
│       │   ├── sub-_ses-_task-_eeg.edf
│       │   ├── sub-_ses-_task-_eeg.json
│       │   │
│       │   ├── sub-_ses-_task-_acq-_events.tsv
│       │   ├── sub-_ses-_task-_acq-_events.json
│       │   │
│       │   ├── sub-_ses-_task-_recording-_stim.tsv.gz
│       │   └── sub-_ses-_task-_recording-_stim.json
│       │
│       └── motion/
│           ├── sub-_ses-_task-_tracksys-_motion.tsv
│           └── sub-_ses-_task-_tracksys-_motion.json
│
└── derivatives/
    ├── MIQ-RS/
    │   └── sub-_MIQ-RS.pdf
    │
    └── validation/
        ├── BeepValidation.xls
        ├── ExoIMU_Stats.xls
        ├── ExoIMU_W_vs_S.xls
        ├── HeadIMU_Stats.xls
        ├── HeadIMU_W_vs_S.xls
        ├── IMU_Orientation.xls
        ├── Training-OpenLoop-Stats.xls
        ├── Trial-CloseLoop-Stats.xls
        ├── failCounterValidation.xls
        ├── infoClosedLoopValidation.xls
        ├── rexCommandValidation.xls
        └── rexStateValidation.xls
```

### **Naming Convention**

- **SubNo (Participant ID):** 1–7
- **SesNo (Session Number):** 1–9
- **Task:** `training`, `trial01–trial12`, `stop6min`, `walk6min`
- **Acq‑Label:** `infoclosedloop`, `rexcommand`, `rexstate`
- **Stim‑Label:** `beep`, `failcounter`
- **IMU‑Pos:** `head`, `exo`

### **Citation**
If you use this dataset, please cite the associated study and acknowledge the contributors.