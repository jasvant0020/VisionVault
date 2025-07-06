# 🔍 VisionVault

Your room’s memory bank — logs what was seen and when.

ObjectLogger AI is an intelligent Python-based computer vision system that monitors a room using a camera, detects and tracks objects in real-time, and logs their last seen details — making it incredibly easy to find misplaced items like keys, wallets, phones, etc.

Instead of manually scrubbing through long hours of CCTV footage, users can quickly retrieve the **last known location**, **timestamp**, and **snapshot** of any detected object — instantly.

---

## 🎯 Key Features

✅ **Real-Time Object Detection**  
Detect common objects like keys, phones, bags, bottles, and more using YOLOv8.

✅ **Smart Object Tracking**  
Assign unique IDs to each detected object and track them continuously across frames.

✅ **Last Seen Snapshot Logging**  
Capture and save the latest snapshot and metadata of every object seen in the room.

✅ **Person-Object Interaction Logging** *(optional)*  
If someone picks up or drops an object, the system logs the interaction with a person ID.

✅ **Organized Object Logs**  
Each object has a dedicated folder containing its latest image and `meta.json` file with time, ID, and other data.

✅ **No More Scrubbing CCTV Footage!**  
Users can search and view where and when an object was last seen with a single command or simple GUI.

---

## 📂 Folder Structure

    ObjectLogger-AI/
    │
    ├── main.py # Main controller script
    ├── detection/
    │ └── detector.py # Object detection logic (YOLOv8)
    ├── tracking/
    │ └── tracker.py # Object tracking logic (Deep SORT)
    ├── logs/
    │ ├── key/
    │ │ ├── last_seen.jpg
    │ │ └── meta.json
    │ └── phone/
    │ ├── last_seen.jpg
    │ └── meta.json
    └── gui/
    └── search_interface.py # Optional GUI for searching objects

---

## 🚀 How It Works

1. **Live video stream** from a camera monitors the room.
2. Detected objects are tracked using YOLO and Deep SORT.
3. For every unique object:
   - A folder is created inside `/logs/`
   - A snapshot and metadata are saved every time the object is seen
4. When an object disappears or needs to be found, users can:
   - Check the `/logs/<object_name>/last_seen.jpg`
   - View the associated `meta.json` for timestamp and details

---

## 🧠 Real-Life Use Case

> A person leaves their keys in the room and forgets.  
> Instead of watching the whole CCTV footage, they check the **logs/keys/** folder.  
> It shows the **last seen image**, **exact time**, and even **who picked it up** if a person was in frame.

---

## 🛠️ Built With

- **Python 3.10+**
- **YOLOv8 (Ultralytics)** for object detection
- **Deep SORT / ByteTrack** for object tracking
- **OpenCV** for video processing
- **JSON & OS modules** for file and metadata management

---

## 🔮 Future Upgradations

- 🔎 **Search Interface (GUI/CLI)**  
  Search for objects using keywords and instantly load their last seen snapshots and details.

- 👁️ **3D Object Location Tracking**  
  If using a depth camera, show where in the room the object was placed.

- 🧑‍💼 **Facial Recognition of Person Handling Objects**  
  Link object movements with recognized faces for audit trails.

- 🛑 **Missing Object Alert System**  
  Get notified if a frequently used object hasn't been seen for a long time.

- 🧠 **Offline Timeline of Object Appearances**  
  Timeline view of each object’s visibility throughout the day.

---

## 📌 Project Status

🚧 **In Development** — Stay tuned for upcoming versions!  
📢 **Star this repo** to stay updated and contribute ideas or suggestions.

---

## 🤝 Contributing

Pull requests are welcome! If you have ideas for improvement or want to extend functionality, feel free to fork and contribute.

---

## 📃 License

[MIT License](LICENSE)

---

## 🙋‍♂️ Author

**Jasvant**  
🚀 Passionate about AI | CV Projects | Making the unseen, seen  
🔗 [GitHub](https://github.com/jasvant0020)

---



















