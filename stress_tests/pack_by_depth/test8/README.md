# Stress tests
Define your input.csv and expected_output.json files in this repository. If you define multiple test cases, place each one into a separate sub-directory.

Use the provided `expected_output.json` template to fill in the details of the expected output that corresponds to your input.csv.


**Based on the assumptions that canvases (or 4PerBox) are 2.5" wide and paper prints (or 6PerBox) are 1.83" wide.**

## Box Packing:
There are 250 standard sized pieces, all of which are paper prints. So 250 6PerBox will take up 41 StandardBoxes, with 4 more pieces left.  
250 / 6 = 41 .... 4  

There are 183 Large pieces that will be able to fit inside large boxes but not standard boxes. (all of which have both dimensions over 36.5" and at least one dimension under 44"). These 183 4PerBox will take up 45 LargeBoxes, with 3 left.   
183 / 4 = 45 ... 3 

Since we have both large pieces and standard pieces left, we first deal with the large pieces. The 3 large pieces can fit in one LargeBox, constituting 3 * 2.5" = 7.5", leaving 13" - 7.5" = 5.5" space in the LargeBox. We can then fit 5.5" / 1.83 " = 3 6PerBox pieces in there.

This leaves us with 1 extra standard sized, 6PerBox piece no where to go into. So we'll need 1 extra StandardBox to put it in.

## Pallet Packing:

A standard pallet can hold 4 standard boxes but only 3 large boxes. Large boxes should go on standard pallets.
- 37 large boxes go on 13 standard pallets (12 are full and 1 has space for 2 standard boxes).
- Of the 42 standrad boxes we have, 2 will go on the pallet with 1 large box, leaving us with 40 standard boxes. 
   - 40 standard boxes will fit on 8 oversized pallets

Pallet total:
- 13 standard (13 * 60 lbs = 780 lbs)
- 8 oversized (8 * 75 lbs = 600 lbs)
**Total pallet weight: 1380 lbs**
