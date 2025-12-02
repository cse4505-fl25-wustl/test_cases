# Stress tests

### Author: Bean Royal
### Packing Strategy: pack by depth
This test case tries to fit as many items into a box as the box depth would allow. We estimate the depth of each type of art, and calculate the total depth of the art. If it fits into one box, we put it in one box, otherwise, we split them up.  
Expects items to be packed largest to smallest
### Client Details: does not accept crates

## Results explanation
* there are 600 pieces of art total
* line items are 1 & 2 are custom pieces and require custom boxes because they have a dimension over 88 inches, which makes 200 custom pieces
* line items 3, 5, 7, & 9 are oversized pieces (one dimension over 44) and fit into standard boxes (one dimension less than or equal to 36.5)
* line items 4, 6, 8, & 10 are standard pieces (no dimension over 44) and require large boxes (both dimensions over 36.5)
* this makes a total of 100 standard pieces and 100 oversized pieces, which need to be packed
* line items 3, 5, 7, & 9 get packed into 25 standard boxes
  * 2.75 depth per piece --> 4 pieces per standard box
* line items 4, 6, 8, & 10 get packed into 25 large boxes
  * 2.75 depth per piece --> 4 pieces per large box
* 24 large boxes fit onto 8 standard pallets
* the last large box goes onto a standard pallets with 2 standard boxes
* 15 standard boxes fit onto 3 oversized pallets
* the last 8 standard boxes fit onto 2 standard pallets
* that makes 1 standards pallets (60 lbs each) and 3 oversized pallets (75 lbs each), with a total packaging weight of 885 lbs
* the total artwork weight is 1,800 lbs
  * line items 1 & 2 = 3,600 & 3,400 (respectively, BUT NOT INCLUDED)
  * line items 3 & 4 = 350 each
  * line items 5 & 6 = 250 each
  * line items 7 & 8 = 175 each
  * line items 9 & 10 = 150 each
* the final shipment weight is the sum of the last 2 weights, which is 2,735 lbs
