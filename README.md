# 🎮 **Heatmap-Visualization for PUBG Player Deaths**

**Description**

This repository contains two death heatmaps created using **Tableau** to visualize the locations where players commonly die on the **PUBG** game maps. These heatmaps are generated from data collected from in-game matches and help identify hotspots of player deaths, providing valuable insights for game analysis and strategy.

- **Gradient (from high to low death rate)**:  
  **Red → Orange → Yellow → Green → White**
  - **Red**: High death rate (most deaths)
  - **Orange → Yellow → Green**: Medium to low death rate (moderate deaths)
  - **White**: No deaths recorded

---

### **Game Description** _from Kaggle_

**PUBG** (PlayerUnknown’s Battlegrounds) is a **first/third-person shooter** battle royale game. It drops over **90 players** onto a large island where teams and solo players fight to be the last one remaining. The objective is to scavenge weapons, armor, and supplies while avoiding a continually shrinking "bluezone," which damages players outside the safe zone. Players can either choose to fight or hide in the quest to survive and be the last player standing.

---

### **Reasoning Behind the Heatmap**

The **death heatmaps** are created to identify **player tendencies** and potential issues within the game. By analyzing where most player deaths occur, game developers and players can:

- Spot frequent hotspots where deaths occur.
- Understand player behaviors and decisions.
- Enhance gameplay experience and increase retention rate.

---

### **Methodology**

1. **Data Source**:
   - **Link**: [PUBG Match Deaths Dataset on Kaggle](https://www.kaggle.com/datasets/skihikingkevin/pubg-match-deaths)
   - **File**: `kill_match_stats_final_1.csv` (contains detailed player death locations).
   
2. **Data Cleaning**:
   - The raw dataset contained **1,048,575 rows** of data, including:
     - **Victim Position (x and y coordinates)** and the **map** where the death occurred.
     - **Issues**: Some data points had invalid coordinates (e.g., `0's` indicating players who did not have a death position).

3. **Data Processing**:
   - Cleaned the dataset by removing rows with invalid victim positions.
   - Imported the cleaned data into **Tableau** for visualization.

4. **Heatmap Creation**:
   - **Erangel Map**: ~800k data points
   - **Miramar Map**: ~180k data points
   - The **x and y axes** represent death locations on the 800 x 800 grid of the map.
   - Data points were converted into a **density plot** with a **gradient color scale** to show areas with higher or lower death rates.

5. **Customization**:
   - Adjusted **Opacity**, **Intensity**, and **Size** of the data points to highlight key areas with frequent deaths.
   - Overlaid **Erangel** and **Miramar** maps on the dashboard for context.

---

### **How to Use the Heatmaps**

1. **Visualize the Heatmaps**:
   - Open the heatmaps for **Erangel** and **Miramar** to analyze which areas of the map have the highest death rates.
   
2. **Use in Strategy & Analysis**:
   - Players can use these heatmaps to identify **high-risk zones** and modify their strategies accordingly (e.g., avoid frequent death spots).
   - Map shrinkage and spawn points (high density loot areas) are key factors that influence death location. 

---

### **Requirements**

- **Tableau** for creating the heatmaps.
- **Data**: `kill_match_stats_final_1.csv` (available in the Kaggle dataset).

---

### **Forward Looking**

- This project not only demonstrates the power of data visualization to inform game decisions, but it also serves as a foundational example of heatmap creation. Inspired by the game development process during my playtests with _Arkheron_, this project was to aid in the exploration of enhancing game experience through analysis. 

