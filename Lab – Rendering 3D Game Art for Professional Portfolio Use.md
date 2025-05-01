
# Lab – Rendering 3D Game Art for Professional Portfolio Use

*In this lab, we will render high-quality wireframe-on-clay images of our 3D game assets using Blender’s bevel + material index workflow. This method gives a clean, stylized look suitable for portfolio presentation, and it visually communicates topology and edge flow.*

![alt text](<ClayWireframeLab-Cover.png>)

---

### Introduction

A professional portfolio should show both artistic skill and technical competency. Rendering a clay model with an overlay wireframe gives employers a clear look at your modeling precision without distracting textures.

In this lab, you will:

- Apply bevel modifiers to accentuate geometry edges
- Use material indices to isolate wireframe highlights
- Configure materials for a clay base and glowing edge overlay
- Render final images in Blender’s Cycles engine

---

### Core Concepts

#### **1. Why Use a Clay + Wireframe Render?**
This style is widely used in 3D portfolios to show edge flow, silhouette quality, and mesh cleanliness in a visually appealing way.

#### **2. Non-Destructive Bevels**
By using a **Bevel Modifier** set to affect **nothing**, we can still leverage material indexing to control what gets rendered — no changes to geometry required.

#### **3. Material Index-Based Rendering**
Blender allows us to assign different materials to geometry based on material index, which we’ll use to highlight edges independently from the clay base.

---

### Section 1 – Setting Up Your Asset

#### **Step 1: Open Your Clean Mesh**
- Load your final retopologized and UV’d model into **Blender**.
- Ensure that **modifiers are unapplied** — you’ll be working non-destructively.

#### **Step 2: Smooth Shading**
- In Object Mode, right-click your model.
- Choose **Shade Smooth** for a clean clay look.

---

### Section 2 – Apply the Bevel Modifier for Edge Highlighting

#### **Step 1: Add Bevel Modifier**
- With your object selected, go to the **Modifiers** tab.
- Add **Bevel Modifier**.
- Set **Limit Method** to **None**.
- Change **Segments** to **1**.
- Set **Width** to a small value like `0.005`.

#### **Step 2: Assign a Material Index to Bevel**
- Under the Bevel settings, find **Material** and set it to **1**.
> This will assign material slot 2 (index 1) to the beveled edges.

---

### Section 3 – Create Clay and Wire Materials

#### **Step 1: Add Two Material Slots**
- In the **Material Properties**, click **+** twice to add two slots.
- Assign:
  - **Slot 1 (Index 0): Clay Base**
  - **Slot 2 (Index 1): Wireframe Edges**

#### **Step 2: Configure Clay Material**
- Set the **Base Color** to a neutral matte (e.g. mid-gray or tan).
- Use a **Principled BSDF** with roughness around **0.8**.

#### **Step 3: Configure Wireframe Material**
- Use **Emission Shader**.
- Set Emission Color to bright (white, orange, or cyan work well).
- Increase **Strength** to 3–5.

> *This lets the beveled edges glow softly in the final render.*

---

### Section 4 – Render Setup and Lighting

#### **Step 1: Set Up Lighting**
- Add a **3-point light setup** or an **HDRI** for subtle ambient shadows.
- Ensure lights aren’t too strong — keep attention on the mesh.

#### **Step 2: Set Camera Angle**
- Position your camera to show your mesh’s silhouette clearly.
- Use **Shift + ` (accent key)** and **G**/**R** to fly and rotate your view easily.

#### **Step 3: Set Render Engine to Cycles**
- Go to **Render Properties**.
- Set **Render Engine** to **Cycles**.
- Enable **GPU Acceleration** if available.

---

### Section 5 – Render Final Image

#### **Step 1: Set Render Resolution**
- Output Properties > Resolution: **1920x1080** or higher.

#### **Step 2: Set Render Samples**
- For quality output, set **Samples** to at least **128**.

#### **Step 3: Hit Render**
- Press **F12** to render your scene.
- Save image via Image > Save As.

> *Export a few angles to show different aspects of your topology.*

---

### Final Checklist

✅ Applied bevel modifier with material index targeting  
✅ Created a clay base and glowing wireframe overlay material  
✅ Rendered in Cycles with clean lighting setup  
✅ Saved high-quality renders for portfolio use  
