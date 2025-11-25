# Stress tests
Define your input.csv and expected_output.json files in this repository. If you define multiple test cases, place each one into a separate sub-directory.

Use the provided `expected_output.json` template to fill in the details of the expected output that corresponds to your input.csv.

# Justification

- Crates not allowed
- Uses depth packing for mixed mediums

## Canvas - Framed
- 1 * 43.5 * 0.0086 = 0.3741 lbs
- 398 * 1 = 398 lbs
- 99.5 standard boxes
- Because 1 < 84 height threshold, we can still fit these into standard boxes

## Acoustic Panel - Framed
- 43.5 * 1 * 0.0037 = 0.16095 lbs
- 102 * 1 = 102 lbs
- 25.5 standard boxes

## Pallets
- 99.5+25.5=125 standard boxes
- 4 per pallet, 32 standard pallets = 1920 lbs
- If 5 per pallet, 25 oversized pallets = 1875 lbs
- We choose oversized pallets as these weigh less.

## Totals
- 125 standard boxes
- 500 total artwork
- Packing weight = 1875 lbs
- Artwork weight = 500 lbs
- Total = 2375 lbs
