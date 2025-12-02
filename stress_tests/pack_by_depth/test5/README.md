# Test Case 1: Maximum Telescoping Boundary: Assumes No Crates

## Expected Output Explanation

This test contains **534 pieces** with the following expected output:

```json
{
  "total_pieces": 534,
  "custom_piece_count": 0,
  "standard_size_pieces": 474,
  "standard_box_count": 114,
  "large_box_count": 0,
  "standard_pallet_count": 1,
  "oversized_pallet_count": 22,
  "crate_count": 3,
  "total_artwork_weight": 7533,
  "total_packaging_weight": 2085,
  "final_shipment_weight": 9618
}
```

### Why This Output is Correct

**Total Pieces (534)**: Sum of all quantities in input CSV:
- Lines 1-6: 48×6 = 288 pieces
- Lines 7-8: 24×2 = 48 pieces
- Lines 9-10: 27×2 = 54 pieces
- Lines 11-12: 18×2 = 36 pieces
- Lines 13-14: 24×2 = 48 pieces
- Lines 15-16: 25×2 = 50 pieces
- Lines 17-18: 5×2 = 10 pieces
- **Total: 534 pieces**

**Standard Size Pieces (474)**: Lines 1-14 all have at least one dimension ≤ 36" and fit in standard boxes (474 pieces).

**Standard Box Count (114)**: Based on per-box capacity:
- Paper prints: 1/6 * 239
- Canvas: 1/4 * 199
- Acoustic panels: 1/4 * 239

**Large Box Count (0)**: All pieces fit standard boxes.

**Crate Count (3)**: The 60 pieces with 87-88" dimensions (lines 15-18) trigger crate packing. With crate capacity of ~18-25 pieces depending on size, this requires 3 crates.

**Pallet Counts**: 114 standard boxes optimally packed:
- Dynamic programming minimizes tare weight
- Result: 1 standard pallet (4 boxes each, 60 lbs tare) + 22 oversized pallets (5 boxes each, 75 lbs tare)
- Total: (1×4) + (22×5) = 114 boxes ✓

**Artwork Weight (7533 lbs)**: Calculated as `ceil(width × height × density)` for each piece using material densities:
- Paper Print + Glass: 0.0098 lb/sq in
- Paper Print + Acrylic: 0.0094 lb/sq in
- Canvas Float Frame: 0.0085 lb/sq in
- Canvas Gallery: 0.0061 lb/sq in
- Acoustic Panel: 0.0038 lb/sq in
- Acoustic Panel Framed: 0.0037 lb/sq in

Sum of all individual piece weights multiplied by quantities = 7533 lbs.

**Packaging Weight (1920 lbs)**:
- 1 standard pallets × 60 lbs = 60 lbs
- 22 oversized pallets × 75 lbs = 1650 lbs
- **Total: 1710 lbs**

**Final Shipment Weight (9453 lbs)**: 7533 + 1710 = 9243 lbs

## Mixed Medium Box Packing Strategy

This test assumes **mixed medium packing is allowed**. Different material types (paper prints, canvas, acoustic panels) can be combined in the same box.