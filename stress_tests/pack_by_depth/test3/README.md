# Stress tests
Define your input.csv and expected_output.json files in this repository. If you define multiple test cases, place each one into a separate sub-directory.

Use the provided `expected_output.json` template to fill in the details of the expected output that corresponds to your input.csv.

## EXPECTED OUTPUT JUSTIFICATION

### TOTAL PIECES:
- adding up all the quantities gives 500

### OVERSIZED PIECES:
- if one side is > 44
- 40 + 20 = 60 pieces

### STANDARD SIZED PIECES:
- all the other remaining pieces that aren't oversized
- 100 + 80 + 60 + 40 + 20 + 50 + 30 + 30 + 20 + 10 = 440 pieces

### CUSTOM PIECES (needs custom packaging):
- 0, none of them have both dimensions > 43.5"

### BOX PACKING (Depth-based)
40×40 Acrylic Paper Print (60 pieces): 60/7 = 8.57 --> Boxes 1-8 (8 LARGE) are all full
- Box 9 (LARGE): 4 pieces x 1.833 = 7.332" so we have a remaining width of 13" - 7.332" = 5.668"

43×43 Glass Paper Print (40 pieces): 40/7 = 5.714 --> Boxes 10-14 (5 LARGE) are all full
- Box 15 (1 LARGE): 5 pieces × 1.833" = 9.165" so we have a remaining width of 13" - 9.165" = 3.835"

24×30 Glass Paper Print (100 pieces)
- 1.833" per piece 
- 1.833" x 3 = 5.499" so we can fit 3 of these into box 9 to make it full.
- 1.833" x 1 = 1.833" so we can fit 1 of these into box 15, leaving it with remaining capacity of 2.002
- 96/6 = 16 so box 16-31 (16 STANDARD) are all full

36×36 Glass Paper Print (80 pieces)
- 78/6 = 13 so box 32-44 (13 STANDARD) are full
- Box 45 (1 STANDARD): 2 pieces x 1.833" = 3.666" so we have a remaining width of 11" - 3.666" = 7.334"

20×24 Acrylic Paper Print (20 pieces)
- 1.833" x 2 = 3.666" so we can fit 2 of these into box 44 to make it fuller, with remaining capacity of 7.334 - 2.666 = 3.668.
- 18/6 = 3 so box 46-48 (3 STANDARD) are full

30×40 Canvas Framed (50 pieces)
- 48/4 = 12 so box 49-60 (12 STANDARD) are full
- Box 61 (1 STANDARD): 2 pieces x 2.75" = 5.5" so we have a remaining width of 11" - 5.5" = 5.5"

20×20 Canvas Framed (30 pieces)
- 2.75" x 2 pieces = 5.5" so put them into box 61 to make it full (reached quantity capacity)
- 28/4 = 7 so box 62-68 (7 STANDARD) are full

24×36 Canvas Gallery (30 pieces):
- 28/4 = 7 so box 69-75 (7 STANDARD) are full
- Box 76 (1 STANDARD): 2.75" x 2 pieces = 5.5" so we have a remaining width of 11" - 5.5" = 5.5"

24×24 Acoustic Panel (20 pieces):
- 2.75" x 2 pieces = 5.5" so put them into box 76 to make it full
- 16/4 = 4 so box 77-80 (4 STANDARD) are full
- Box 81 (1 STANDARD): 2.75" x 2 pieces = 5.5" so we have a remaining width of 11" - 5.5" = 5.5"

30×30 Acoustic Panel Framed (10 pieces):
- 2.75" x 2 pieces = 5.5" so put them into box 81 to make it full
- 8/4 = 2 so box 82-83 (2 STANDARD) are full

37×48 Canvas Framed (40 pieces):
- 40/4 = 10 so box 84-93 (10 LARGE) are full

40×50 Canvas Gallery (20 pieces):
- 20/4 = 5 so box 94-98 (5 LARGE) are full

#### TOTAL BOXES:
- 30 LARGE
- 68 STANDARD

### TOTAL ARTWORK WEIGHT:
- Line 1: 24×30×0.0098 = 7.056 = 8×100 = 800 lbs
- Line 2: 36×36×0.0098 = 12.7008 = 13×80 = 1,040 lbs
- Line 3: 40×40×0.0098 = 15.68 = 16×60 = 960 lbs
- Line 4: 43×43×0.0098 = 18.12 = 19×40 = 760 lbs
- Line 5: 20×24×0.0098 = 4.704 = 5×20 = 100 lbs
- Line 6: 30×40×0.0085 = 10.2 = 11×50 = 550 lbs
- Line 7: 37×48×0.0085 = 15.096 = 16×40 = 640 lbs
- Line 8: 20×20×0.0085 = 3.4 = 4×30 = 120 lbs
- Line 9: 24×36×0.0061 = 5.2704 = 6×30 = 180 lbs
- Line 10: 40×50×0.0061 = 12.2 = 13×20 = 260 lbs
- Line 11: 24×24×0.0038 = 2.1888 = 3×20 = 60 lbs
- Line 12: 30×30×0.0037 = 3.33 = 4×10 = 40 lbs
- TOTAL = 5,510 lbs

### PALLETS
- 30 large boxes go on 10 standard pallets
- 60 standard boxes go on 12 oversized pallets
- 8 standard boxes go on 2 standard pallets
- TOTAL: 12 oversized pallets, 12 standard pallets

### CRATES
- assume no crates

### TOTAL PACKAGING WEIGHT
- 75 lbs x 12 = 900 lbs
- 60 lbs x 12 = 720 lbs
- TOTAL = 1620 lbs

### FINAL SHIPMENT WEIGHT
- 5,510 lbs + 1,620 lbs = 7,130 lbs



