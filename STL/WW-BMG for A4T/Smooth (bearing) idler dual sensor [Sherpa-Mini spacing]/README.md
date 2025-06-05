# A dual filament sensor, smooth (bearing) idler WWBMG

This version of the WWBMG uses a bearing instead of the toothed secondary drive gear. It is primarily aimed at **reducing potential extrusion consistency artefacts** caused by slight system misalignments. Together with a Bondtech IDGA gear assembly, it helps mitigate extrusion deviations that can appear as inconsistent layer stacking on outer walls.

![IMG_6269](https://github.com/user-attachments/assets/c03596f7-6137-4dd8-81d7-a0ae45402238)

---

## Printed Parts

### Print Settings

Use the same settings as the **A4T toolhead**.

- **Avoid seams** in filament sensor paths – seams may cause slight bulging, making the bearings bind. If necessary use seam painting and blockers in your slicer to do so.
- A **well-calibrated printer** is essential for proper sensor actuation.
- If the sensor bearing holes are too tight:
  - Adjust filament flow rate (EM)
  - Reduce print speed
  - Tweak shrinkage compensation

---

## Bill of Materials (BOM)

- `1x M3x16 SHCS screw`
- `1x 693ZZ bearing`  
  Make sure the bearing dimensions are:
  - **8 mm OD**
  - **3 mm ID**
  - **4 mm width**

---

## Assembly & Setup

### Removing the Built-in Tensioner Arm Supports

The built-in supports are anchored in **three places**:
- Two one-perimeter-wide anchors on the tensioner arm
- One post stabilising the support

**Recommended removal process:**
1. Break the two anchors on the tensioner arm first. Use an X-Acto knife to wedge between the support and the part on both sides of the bottom screw hole. **Be careful not to cut into the built-in bearing standoff!**
2. Turn the stabilising post left and right until it loosens.
3. Break the stabilising post away from the part.
4. Use your X-Acto knife and/or your flush cutter to cut the support in half and remove it.

⚠️ **Warning:** Be careful not to break off the *printed* bearing standoffs!

![IMG_6267](https://github.com/user-attachments/assets/30d1a09b-187c-461d-9364-0b56dbf5f044)

---

### Assembly

1. Insert the `693` bearing into the smooth idler.
2. Insert the `M3x16` screw from the top until it's flush with the part.
3. **Do not overtighten** — the screw threads into plastic.
4. There should be slight play in the bearing (up/down and side-to-side) — this is **intentional** to allow the idler to self-center on the filament path.

The rest of the extruder assembly remains unchanged from the baseline WWBMG design.

![IMG_6268](https://github.com/user-attachments/assets/87bba57e-211b-48a9-8bc9-223df750efe3)


---

### Setting the Tension

The smooth idler tensioner requires slightly **higher tension** than the standard WWBMG:

- Tighten the spring tensioner **until the idler arm no longer moves**.
- Then tighten **3–4 turns further** to set the proper tension. Run some filament through and observe how squished it is against both the teeth and the bearing. You should get a good imprint of the teeth on the filament without the filament flattening much on the bearing side.

---

### Calibration & Use

After installing the smooth idler re-calibrate your:
  - **Rotation distance**
  - **Pressure advance**

Expect both to need adjustment due to the changed filament path and tensioning method.
