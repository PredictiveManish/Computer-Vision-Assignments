# 🌇 Day Night Vision – Assignment 1 (Computer Vision)

## 📝 Problem Statement

Analyze the transition of light throughout a video to determine how much of the footage corresponds to different times of the day based on brightness.

### Video Scenarios:
- 🌞 Day to Evening  
- 🌆 Evening to Night  
- 🌃 Night to Morning/Day  

---

### 🎥 Sample Input:
**Input**: Path to a timelapse or transition video  
**Output**:  
- `40%` Day/Evening  
- `60%` Night  
or  
- `20%` Early Morning, `10%` Night, `70%` Day  

---

## ✅ Solution Overview

### 📺 [YouTube Video Link (Video Analysed)](https://youtu.be/Ljh1ycfNeZ0?si=1ZGFEI6q3TIywFkr)

This video is used for the analysis in this project.

### 📁 Main Files:

- `day_night_vision.ipynb`: Main Jupyter notebook with all the processing steps.
- `brightness_values.txt`: Contains brightness data for each extracted video frame.
- `Images/`: Contains all extracted frames from the video.

---

## ⚙️ Technologies and Libraries Used

| Library      | Purpose                                  |
|--------------|-------------------------------------------|
| `cv2`        | Reading video, extracting and saving frames |
| `numpy`      | Calculating brightness using mean intensity |
| `pandas`     | (Optional) For data handling (if extended)  |
| `matplotlib` | Plotting brightness trends and charts       |

---

## 📊 Brightness Trends Analysis

### 🔢 Frame-wise Brightness Trend

This line graph shows how brightness fluctuates across the video timeline.

![Brightness trends over frame](https://res.cloudinary.com/dw6ps7x9q/image/upload/v1732966349/output_ralpwr.png)

---

### 🧮 Frame Classification by Time of Day

Frames are categorized into:
- ☀️ **Morning** (Brightness: 60–100)
- 🌇 **Sunset** (Brightness: 40–60)
- 🌃 **Night** (Brightness: 0–40)

Distribution based on average brightness per frame:

![Brightness Wise Frames](https://res.cloudinary.com/dw6ps7x9q/image/upload/v1732966349/Distribution_eacirz.png)

---

### 🥧 Pie Chart – Frame % Distribution

Shows proportion of frames in each category:

![Pie-Graph](https://res.cloudinary.com/dw6ps7x9q/image/upload/v1732966349/pie_paxnva.png)

---

## 📌 Key Steps in the Notebook

1. **Read the Video**  
   Using `cv2.VideoCapture` to read frames from `Sample.mp4`.

2. **Extract Frames**  
   Frames are saved as `.png` files for analysis.

3. **Calculate Brightness**  
   Each frame is converted to grayscale and average brightness is calculated using `numpy`.

4. **Save Brightness Data**  
   All brightness values are stored in `brightness_values.txt`.

5. **Categorize Frames**  
   Based on brightness, frames are classified into Morning, Sunset, or Night.

6. **Visualize Data**  
   Used `matplotlib` to generate trend lines, bar graphs, and pie charts.

---

## 📈 Final Output Summary

> Example Output:
