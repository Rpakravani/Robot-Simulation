# 🤖 Multi‑Robot Floor Painting Simulation (C)

A C‑based simulation where multiple autonomous robots move across a 2D floor grid, paint tiles, and change direction based on tile color rules.  
The program supports different floor initialization modes, random robot placement, and configurable simulation parameters loaded from a file.

This project demonstrates **dynamic memory allocation**, **pointer‑based 2D arrays**, **simulation loops**, **randomized behavior**, and **file‑driven configuration**.

---

## 🚀 Features

- **Dynamic 2D floor allocation** using `malloc`  
- **Three initialization modes**:
  - All Magenta  
  - Checkerboard  
  - Random Vertical Stripes  
- **Multiple robots** with:
  - Random starting positions  
  - Random directions  
  - Random paint colors  
- **Tile‑based direction rules** (turning based on tile color)  
- **Toroidal movement** (wrapping around edges)  
- **Simulation output at configurable intervals**  
- **Parameter loading from input file**  

---

## 🧠 Technical Highlights

### **Dynamic Memory Management**
- Allocates a `numRows × numCols` floor grid using a pointer‑to‑pointer structure  
- Proper cleanup of all allocated memory  

### **Robot Behavior**

Each robot has:
struct Robot {
int x;
int y;
int direction;
int paintColour;
};


Robots:
- Move 4 steps per iteration  
- Paint the tile they land on  
- Change direction based on tile color  
- Wrap around edges using modulo arithmetic  

### **Floor Initialization Modes**
- **ALL_MAGENTA** → every tile = 5  
- **CHECKERBOARD** → alternating 6/5 blocks  
- **RANDOM_STRIPES** → random colors in first row, copied downward  

### **File‑Driven Configuration**
The program reads:

---

## 📂 File Structure

/robot-simulation

│── robots.c

│── robots_input.txt

│── README.md


---

## 🖥️ How to Compile & Run

### **Compile**

### **Run**

Make sure your `robots_input.txt` is in the same directory.

---

## 📄 Example Input File

20 20 5 1 12345 200 20 output.txt

Meaning:
- 20×20 grid  
- 5 robots  
- initType = RANDOM_STRIPES  
- seed = 12345  
- 200 iterations  
- print every 20 iterations  
- output file name = output.txt  

---

## 🔧 Future Improvements

- Add visualization (ASCII or GUI)  
- Add robot collision rules  
- Add energy or battery mechanics  
- Add more tile‑based behaviors  
- Export simulation frames to file  
- Add multi‑threaded robot movement  

---

## 🏁 Summary

This project showcases:
- Systems programming in C  
- Memory‑safe dynamic allocation  
- Simulation logic  
- Randomized behavior  
- File parsing  
- Clean modular design  




