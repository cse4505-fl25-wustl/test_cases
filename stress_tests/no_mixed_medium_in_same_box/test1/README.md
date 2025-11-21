# Stress tests
Define your input.csv and expected_output.json files in this repository. If you define multiple test cases, place each one into a separate sub-directory.

Use the provided `expected_output.json` template to fill in the details of the expected output that corresponds to your input.csv.

So, my test case contains 450 total art pieces.

This test case assumes that there are 7 paper prints per large box.

1. Paper Print - Framed (43X43), quantity: 315
- Not custom and Not oversized  
- Weight per piece = ceil(43 X 43 X 0.0098) = 19 lbs

2. Canvas - Gallery (43X43), quantity: 84
- Not custom and Not oversized  
- Weight per piece = ceil(43 X 43 X 0.0061) = 12 lbs

3. Paper Print - Framed (44X46), quantity: 51
- Oversized and Custom  
- Weight per piece = ceil(44 X 46 X 0.0098) = 20 lbs  
- Custom pieces are not boxed.

---

### Packing Strategy Used
This scenario uses a simple medium-separated greedy packing strategy which is consistent with our Feature 2 Packing and Box logic:

- Do not mix different mediums inside the same box.
- Box capacities:
  - Paper Print - Framed: 7 per large box
  - Canvas - Gallery: 4 per large box
- Standard boxes never used (all art exceeds standard limits).
- Custom pieces are excluded from boxing.
- All boxes are placed on standard pallets.
- A standard pallet holds 3 large boxes.

---

### Calculations for the Expected Output
```
{
  "total_pieces": 315 + 84 + 51 = 450  total pieces,   
  "custom_piece_count": 51,
  "standard_size_pieces":  315+84=399 statndart size pieces,
  "standard_box_count": 0 since none of the pieces fit the standard box
  "large_box_count":  315/7=45 boxes and  84 /4 = 21 boxes, 45 + 21 ==66 large boxes
  "standard_pallet_count": 22 since each pallet would hold 3 large boxes 66/3=22,
  "oversized_pallet_count": 0,
  "crate_count": 0,
  "total_artwork_weight": 315X19=5985 and 84X12=1008 (51X20=1020 is custom packaging, so not included in total arwork weight), so 5985+1008=6993,
  "total_packaging_weight": considering 60 lbs for standart pallet tare weight, 22X60=1320,
  "final_shipment_weight":  8013 + 1320 = 9333 lbs.
}
```
