# Stress tests
Strategy: Depth-based packing

Client does NOT accept crates

## Totals for each material type:
- 94 Paper Print – Framed
- 95 Canvas – Gallery
- 95 Acoustic panel
- 96 Canvas – Float Frame
- 95 Acoustic panel – Framed



## Depth of each material type:
Assumption: these numbers are the same, regardless of whether box is standard or large
- 1/6 box each:
    - Paper Print – Framed
- 1/4 box each:
    - Canvas – Gallery
    - Canvas – Float Frame
    - Acoustic panel
    - Acoustic panel – Framed



## Lines that need custom packing:
Rule: both dimensions > 43.5

| Line # | Dimensions | Qty    |
| ------ | ---------- | ------ |
| **8**  | 44 × 68    | **9**  |
| **9**  | 46 × 72    | **10** |
| **10** | 48 × 76    | **9**  |
| **11** | 50 × 80    | **10** |
| **19** | 44 × 70    | **10** |
| **20** | 46 × 74    | **9**  |
| **21** | 48 × 78    | **10** |
| **30** | 44 × 72    | **9**  |
| **31** | 46 × 76    | **10** |
| **32** | 48 × 80    | **9**  |
| **40** | 44 × 74    | **9**  |
| **41** | 46 × 78    | **10** |
| **50** | 44 × 72    | **9**  |


7 of those lines have 9 pieces; 6 have 10

7x9 + 6x10 = 123 custom packing needed



## Pieces that fit in standard boxes:
Rule: As long as at least ONE dimension of an art piece is 36" or less, it will fit in a standard size box. Boxes can be telescoped to a max height of 88"

- Paper Print – Framed
    - Fits on lines: 1, 26, 36, 46
    - Quantities: 10 + 9 + 9 + 9
    - Total = 37 pieces

- Canvas – Gallery
    - Fits on lines: 2, 12
    - Quantities: 9 + 9
    - Total = 18 pieces

- Acoustic panel
    - Fits on lines: 3, 13, 23, 33, 43
    - Quantities: 10 + 10 + 10 + 10 + 10
    - Total = 50 pieces

- Canvas – Float Frame
    - Fits on lines: 4, 14, 24, 34, 44
    - Quantities: 9 + 9 + 9 + 9 + 9
    - Total = 45 pieces

- Acoustic panel – Framed
    - Fits on lines: 15, 25, 35, 45
    - Quantities: 10 + 10 + 10 + 10
    - Total = 40 pieces


Total 6-per-box that fits in standard box: 37 <br>
Total 4-per-box that fits in standard box: 153



## Pieces that require large boxes:
Rule: pieces that AREN'T custom and DON'T fit in standard box

- Paper Print – Framed
    - Lines: 6, 16  
    - Quantities: 8 + 9  
    - Total = 17 pieces

- Canvas – Gallery
    - Lines: 7, 17, 22, 27, 37, 42, 47  
    - Quantities: 10 + 10 + 9 + 10 + 10 + 9 + 10  
    - Total = 68 pieces

- Acoustic panel
    - Lines: 18, 28, 38, 48  
    - Quantities: 9 + 9 + 9 + 9  
    - Total = 36 pieces

- Canvas – Float Frame
    - Lines: 29, 39, 49  
    - Quantities: 10 + 11 + 10  
    - Total = 31 pieces

- Acoustic panel – Framed
    - Lines: 5  
    - Quantities: 10  
    - Total = 10 pieces

Total 6-per-box that needs large box: 17 <br>
Total 4-per-box that needs large box: 145



## Resummarized box needs:
- 123 custom packing needed
- Total 6-per-box that needs large box: 17
- Total 4-per-box that needs large box: 145
- Total 6-per-box that fits in standard box: 37
- Total 4-per-box that fits in standard box: 153


## Pack art into boxes
Rule: Pack large boxes first, putting standard-size art in to fill gaps as needed, then pack standard size boxes


- large 4-per-box:
    - 145 x 1/4 = 36 full large boxes
    - 1 extra large box that's 25% full
    - use 4 large paper prints to fill up remainder of that box (4/6 + 1/4 = 11/12 < 1)

- large 6-per-box:
    - 17-4 = 13 remaining paper prints also need large boxes
    - 13/6 = 2 full large boxes
    - 1 extra large box that's 1/6 full
    - use 5 standard paper prints to fill the rest of this box

- standard 4-per-box:
    - 153 to pack
    - 153/4 = 38 full standard boxes
    - one remaining 1/4 full box
    - use 4 standard paper prints to fill up remainder of that box (4/6 + 1/4 = 11/12 < 1)

- standard 6-per-box:
    - 37-5-4 = 28 remaining
    - 28/6 = 4 full standard boxes
    - 1 remaining 2/3 full box
    
TOTAL LARGE BOXES: 37+3 = 40 <br>
TOTAL STANDARD BOXES: 39+5 = 44



## Pack boxes onto pallets

### Pallet capacity rules:
- Standard pallet can hold:
    - 4 standard boxes
    - 3 large boxes

- Large pallet can hold:
    - 5 standard boxes
    - 3 large boxes

### Packing:
- All large boxes should go on standard pallet:
    - 40/3 = 13 full standard pallets
    - 1 standard pallet with 1 large box
        - has room for 2 standard boxes (possibly 3 but I'll go with 2 to be conservative)

- Remaining standard boxes:
    - 44-2 = 42
    - 42/4 (standard pallets) = 10.5 -> 11 
        - (tare weight 60 lbs each)
        - would weigh 11x60 = 660 lbs
    - 42/5 (large pallets)    = 8.4  -> 9  
        - (tare weight 75 lbs each)
        - would weigh 9x75 = 675 lbs
    - or 8 standard, 2 large (8x4 + 2x5 = 42)
        - would weigh 8x60 + 2x75 = 630 lbs
    
    - 630 lbs is the lowest weight, so should do the last option


PALLET SUMMARY:
- standard: 14 + 8 = 22
- large ("oversize"): 2
- total tare weight: 22x60 + 2x75 = 1470


## Weight calculations
- Total tare weight: 22x60 + 2x75 = 1470
    - 22 standard pallets (60 lbs each)
    - 2 oversize pallets (75 lbs each)

- Non-custom art weight:
    - Paper Print – Framed (Glass Glazing)
        - Density: 0.0098
        - TOTAL: 120 lbs

    - Paper Print – Framed (Acrylic Glazing)
        - Density: 0.0094
        - TOTAL: 184 + 189 + 171 + 180 + 171 = 895 lbs

    - Canvas – Gallery
        - Density: 0.0061
        - TOTAL: 81 + 170 + 72 + 160 + 117 + 140 + 150 + 108 + 140 = 1138 lbs

    - Canvas – Float Frame
        - Density: 0.0085
        - TOTAL: 144 + 135 + 126 + 250 + 126 + 275 + 126 + 250 = 1432 lbs

    - Acoustic panel
        - Density: 0.0038
        - TOTAL: 70 + 60 + 99 + 60 + 90 + 60 + 99 + 60 + 90 = 688 lbs
        
    - Acoustic panel – Framed
        - Density: 0.0037
        - TOTAL: 80 + 80 + 70 + 70 + 70 = 370 lbs

    - GRAND TOTAL ART WEIGHT: 120 + 895 + 1138 + 1432 + 688 + 370 = 4643
        

## Detailed Art Weight Calculations

### *Paper Print – Framed*
- *Line numbers:* 1, 6, 16, 26, 36, 46
- *Items:*
  - Glass (Density: 0.0098)
    - 30*40 * 0.0098 = 11.8 = 12
        - Quantity: 10
        - Total weight = 10 * 12 = 120

  - Acrylic (Density: 0.0094)
    - 40*60 * 0.0094 = 22.6 = 23
        - Quantity: 8
        - Total weight = 8 * 23 = 184

    - 38*58 * 0.0094 = 20.7 = 21
        - Quantity: 9
        - Total weight = 9 * 21 = 189

    - 36*56 * 0.0094 = 18.95 = 19
        - Quantity: 9
        - Total weight = 9 * 19 = 171

    - 36*58 * 0.0094 = 19.6 = 20
        - Quantity: 9
        - Total weight = 9 * 20 = 180

    - 36*56 * 0.0094 = 18.95 = 19
        - Quantity: 9
        - Total weight = 9 * 19 = 171

TOTAL: 120 + 184 + 189 + 171 + 180 + 171
      = 1015 lbs

---

### **Canvas – Gallery**
- Line numbers: 2, 7, 12, 17, 22, 27, 37, 42, 47
- Density: 0.0061
- Items:
  - 32*44 * 0.0061 = 8.59 = 9
    - Quantity: 9
    - Total weight = 9 * 9 = 81

  - 42*64 * 0.0061 = 16.40 = 17
    - Quantity: 10
    - Total weight = 10 * 17 = 170

  - 30*42 * 0.0061 = 7.69 = 8
    - Quantity: 9
    - Total weight = 9 * 8 = 72

  - 40*62 * 0.0061 = 15.13 = 16
    - Quantity: 10
    - Total weight = 10 * 16 = 160

  - 50*40 * 0.0061 = 12.2 = 13
    - Quantity: 9
    - Total weight = 9 * 13 = 117

  - 38*60 * 0.0061 = 13.91 = 14
    - Quantity: 10
    - Total weight = 10 * 14 = 140

  - 38*62 * 0.0061 = 14.37 = 15
    - Quantity: 10
    - Total weight = 10 * 15 = 150

  - 48*40 * 0.0061 = 11.71 = 12
    - Quantity: 9
    - Total weight = 9 * 12 = 108

  - 38*60 * 0.0061 = 13.908 = 14
    - Quantity: 10
    - Total weight = 10 * 14 = 140

TOTAL: 81 + 170 + 72 + 160 + 117 + 140 + 150 + 108 + 140
      = 1138 lbs

---

### **Canvas – Float Frame**
- Line numbers: 4, 14, 24, 29, 34, 39, 44, 49
- Density: 0.0085
- Items:
  - 36*52 * 0.0085 = 15.912 = 16
    - Quantity: 9
    - Total weight = 9 * 16 = 144

  - 34*50 * 0.0085 = 14.45 = 15
    - Quantity: 9
    - Total weight = 9 * 15 = 135

  - 32*48 * 0.0085 = 13.056 = 14
    - Quantity: 9
    - Total weight = 9 * 14 = 126

  - 42*68 * 0.0085 = 24.276 = 25
    - Quantity: 10
    - Total weight = 10 * 25 = 250

  - 32*50 * 0.0085 = 13.6 = 14
    - Quantity: 9
    - Total weight = 9 * 14 = 126

  - 42*70 * 0.0085 = 24.99 = 25
    - Quantity: 11
    - Total weight = 11 * 25 = 275

  - 32*48 * 0.0085 = 13.056 = 14
    - Quantity: 9
    - Total weight = 9 * 14 = 126

  - 42*68 * 0.0085 = 24.276 = 25
    - Quantity: 10
    - Total weight = 10 * 25 = 250


TOTAL: 144 + 135 + 126 + 250 + 126 + 275 + 126 + 250
      = 1432 lbs

---

### **Acoustic panel**
- Line numbers: 3, 13, 18, 23, 28, 33, 38, 43, 48
- Density: 0.0038
- Items:
  - 34*48 * 0.0038 = 6.2 = 7
    - Quantity: 10
    - Total weight = 10 * 7 = 70

  - 32*46 * 0.0038 = 5.6 = 6
    - Quantity: 10
    - Total weight = 10 * 6 = 60

  - 42*66 * 0.0038 = 10.5 = 11
    - Quantity: 9
    - Total weight = 9 * 11 = 99

  - 30*44 * 0.0038 = 5.02 = 6
    - Quantity: 10
    - Total weight = 10 * 6 = 60

  - 40*64 * 0.0038 = 9.7 = 10
    - Quantity: 9
    - Total weight = 9 * 10 = 90

  - 30*46 * 0.0038 = 5.2 = 6
    - Quantity: 10
    - Total weight = 10 * 6 = 60

  - 40*66 * 0.0038 = 10.03 = 11
    - Quantity: 9
    - Total weight = 9 * 11 = 99

  - 30*44 * 0.0038 = 5.02 = 6
    - Quantity: 10
    - Total weight = 10 * 6 = 60

  - 40*64 * 0.0038 = 9.7 = 10
    - Quantity: 9
    - Total weight = 9 * 10 = 90

TOTAL: 70 + 60 + 99 + 60 + 90 + 60 + 99 + 60 + 90
      = 688 lbs

---

### **Acoustic panel – Framed**
- Line numbers: 5, 15, 25, 35, 45
- Density: 0.0037
- Items:
  - 38*56 * 0.0037 = 7.9 = 8
    - Quantity: 10
    - Total weight = 10 * 8 = 80

  - 36*54 * 0.0037 = 7.2 = 8
    - Quantity: 10
    - Total weight = 10 * 8 = 80

  - 34*52 * 0.0037 = 6.5 = 7
    - Quantity: 10
    - Total weight = 10 * 7 = 70

  - 34*54 * 0.0037 = 6.8 = 7
    - Quantity: 10
    - Total weight = 10 * 7 = 70

  - 34*52 * 0.0037 = 6.5 = 7
    - Quantity: 10
    - Total weight = 10 * 7 = 70

TOTAL: 80 + 80 + 70 + 70 + 70
      = 370 lbs