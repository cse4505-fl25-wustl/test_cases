# Stress Test Case: 500 Piece Mixed Batch (Corrected Format)

## Overview
This test case stresses the system with **500 art pieces** of varying sizes and mediums, formatted to match the application's specific CSV parser requirements. It tests the logic for Standard Boxes, Large Boxes, and Custom Boxes, as well as the palletization logic for each.

## Input Data Breakdown
The input contains 4 distinct groups (lines):

1.  **Line 1 (Standard Prints):** 240 items | 20" x 20" | Framed Paper (Glass)
    * *Fits Standard Box.*
2.  **Line 2 (Standard Canvases):** 160 items | 30" x 30" | Gallery Canvas
    * *Fits Standard Box.*
3.  **Line 3 (Large Prints):** 70 items | 40" x 40" | Framed Paper (Glass)
    * *Too big for Standard Box, fits Large Box.*
4.  **Line 4 (Oversize Prints):** 30 items | 50" x 50" | Framed Paper (Glass)
    * *Too big for Large Box, requires Custom Box.*

## Calculation of Expected Output

### 1. Box Packing
* **Group 1 (20x20 Glass):**
    * Box Type: **Standard Box** (Width Cap: 11.0")
    * Item Width: 1.83" (Glass) -> `11.0 / 1.83` = 6 items/box.
    * Count: `240 / 6` = **40 Standard Boxes**.
    * Weight: 240 * 4.0 lbs = 960 lbs.
* **Group 2 (30x30 Canvas):**
    * Box Type: **Standard Box** (Width Cap: 11.0")
    * Item Width: 2.75" (GalleryCanvas) -> `11.0 / 2.75` = 4 items/box.
    * Count: `160 / 4` = **40 Standard Boxes**.
    * Weight: 160 * 6.0 lbs = 960 lbs.
* **Group 3 (40x40 Glass):**
    * Box Type: **Large Box** (Width Cap: 13.0")
    * Item Width: 1.83" (Glass) -> `13.0 / 1.83` = 7.1 -> 7 items/box.
    * Count: `70 / 7` = **10 Large Boxes**.
    * Weight: 70 * 16.0 lbs = 1120 lbs.
* **Group 4 (50x50 Glass):**
    * Box Type: **Custom Box** (Max dims > 43.5")
    * Capacity: 10 items (defined in `CustomBox.java`).
    * Count: `30 / 10` = **3 Custom Boxes**.
    * Weight: 30 * 25.0 lbs = 750 lbs.

**Total Boxes:** 80 Standard + 10 Large + 3 Custom.

### 2. Palletization
* **Large Boxes:**
    * Capacity: 3 boxes/standard pallet (reduced capacity rule for Large Boxes).
    * `10 boxes / 3` = 3 full + 1 partial (with room for 2 standard boxes) = **4 Standard Pallets**.

* **Standard Boxes:**
    * 78 boxes remain
    * 14 oversized pallets (5 boxes per pallet) for a total of 70 boxes
    * 2 standard pallets (4 per pallet) for a total of 8 boxes 

### 3. Final Totals
* **Standard Box Count:** 80
* **Large Box Count:** 10
* **Standard Pallet Count:** 6 (4 + 2)
* **Oversize Pallet Count:** 14
* **Custom Pieces:** 30
* **Standard Size Pieces:** 470 (240 + 160 + 70)

### 4. Weights
* **Artwork:** 960 + 960 + 1120 = **3040.0 lbs**
* **Packaging:**
    * 6 Standard Pallets * 60 lbs = 360 lbs
    * 14 Oversize Pallet * 75 lbs = 1050 lbs
    * Total = **1410.0 lbs**
* **Final Shipment:** 3040 + 1410 = **4450.0 lbs**
