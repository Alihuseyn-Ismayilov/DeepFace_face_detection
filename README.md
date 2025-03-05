---

# How to Use and Customize Face Detection

## Overview
This project captures a live video feed and compares detected faces against predefined reference images. The reference images are loaded at the beginning of the script, and the face comparison is based on the `known_faces` dictionary.

If you want to test a different image or fine-tune the recognition for a specific case, you need to **replace** `resume_photo.jpg` with a different image.

---

## Running the Project
### 1. Install Dependencies
Before running the project, install the required dependencies:
```bash
pip install opencv-python tkinter
```

### 2. Run the Script
Execute the Python script (if it's not in a Jupyter Notebook):
```bash
python face_detection.py
```

---

## Changing the Reference Image (`resume_photo.jpg`)

### 1. Locate This Line in the Code:
```python
alihuseyn = cv2.imread('resume_photo.jpg')
```
This line loads the reference image (`resume_photo.jpg`) into memory.

### 2. Replace It with Your Desired Image:
For example, if you want to use `new_face.jpg` instead, change the line to:
```python
alihuseyn = cv2.imread('new_face.jpg')
```
Make sure:
- The new image is placed in the same directory as the script.
- The filename and extension are correctly written.

### 3. (Optional) Add More Known Faces:
The `known_faces` dictionary stores all the reference images for face comparison. You can add new faces by modifying the dictionary:
```python
new_person = cv2.imread('new_person.jpg')

known_faces = {
    'Alihuseyn' : alihuseyn,
    'Bill Gates': bill,
    'Elon Musk' : elon,
    'New Person': new_person
}
```

### 4. Save and Re-run the Script
Once you’ve made the changes, save the file and restart the script to apply the new reference image.

---

## Fine-Tuning for Better Detection
If recognition accuracy is low, consider these improvements:
- **Use a high-quality, well-lit image** for the reference photo.
- **Crop the face tightly** in the image before using it.
- **Ensure consistent image formats**, such as `.jpg` or `.png`.

---
