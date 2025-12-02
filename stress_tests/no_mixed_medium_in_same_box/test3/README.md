# Stress test case (540 pieces, mixed media / mixed sizes)

## Input mix (400–600 requirement satisfied)
- 200 × Paper Print - Framed, 30"×24", glazing: Regular Glass  
- 120 × Paper Print - Framed, 38"×30", glazing: Acrylic  
- 80 × Canvas - Gallery, 30"×24"  
- 40 × Canvas - Float Frame, 42"×30"  
- 30 × Acoustic panel, 43"×43" (oversize box path)  
- 70 × Acoustic panel - framed, 32"×28"  
- Total pieces: 540; all media labels are on the allowed list. Mixed-media policy: **do not mix different media in the same carton**.

## Expected output (per project rules)
- Box capacities: Paper (glass/acrylic) 6/box; Canvas (Gallery/Float) 4/box; Acoustic 4/box; oversize pieces still respect per-product limit.  
  - Paper: 200/6 = 34 boxes, 120/6 = 20 boxes → 54 standard boxes  
  - Canvas: 80/4 = 20, 40/4 = 10 → 30 standard boxes  
  - Acoustic framed: 70/4 = 18 standard boxes  
  - Acoustic 43×43: 30/4 = 8 large boxes  
  - **Standard boxes: 102; Large boxes: 8**
- Pallets: standard pallets hold 4 standard boxes → 102/4 = 26 (ceil); oversize pallets hold 5 large boxes → 8/5 = 2 (ceil). Crates: 0.
- Piece counts: standard_size_pieces = 510 (everything except the 30 oversize acoustic panels); custom_piece_count = 0; total_pieces = 540.
- Artwork weight (each piece rounded up, then multiplied):
  - Paper (glass 0.0098): 30×24=720 → 720×0.0098=7.056 → 8 lb ×200 = 1600
  - Paper (acrylic 0.0094): 30×38=1140 → 1140×0.0094=10.716 → 11 lb ×120 = 1320
  - Canvas Gallery (0.0061): 720×0.0061=4.392 → 5 lb ×80 = 400
  - Canvas Float (0.0085): 42×30=1260 ×0.0085=10.71 → 11 lb ×40 = 440
  - Acoustic (0.0038): 43×43=1849 ×0.0038=7.026 → 8 lb ×30 = 240
  - Acoustic framed (0.0037): 32×28=896 ×0.0037=3.315 → 4 lb ×70 = 280  
  - **Total artwork weight: 4280 lb**
- Packaging weight:
  - Boxes: 102 standard; 8 large
  - Pallets: 
 	- Large boxes go on standard pallets (3 per pallet): 2 full pallets 1 partial pallet
	- 1 standard box can go on the 1 partial pallet, leaving 101 standard boxes to package
 	- We can use 17 oversized pallets (5 per pallet) and 4 standard pallets (4 per pallet) to fit 101 standard boxes
	- Totals: 17 oversized pallets (75 lbs each) and 7 standard pallets (60 lbs each), for a total of 1695 lbs 
  - **Total packaging weight: 1695 lb**
- Final shipment weight: 4280 + 1695 = **5975 lb**

## Files
- `input.csv` — six rows covering mixed media and size classes
- `expected_output.json` — fills in all required fields with the above calculations
