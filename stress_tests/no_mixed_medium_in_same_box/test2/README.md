# Stress tests


## Case 2 
### Why the expected_output.json is correct for input.csv

Case 2 contains multiple medium types and multiple size groups, and therefore tests a wider range of packing conditions and ambiguous situations. The expected_output.json is correct because every box contents match the client’s explicit per-box capacity rules for that specific medium. Canvas–Gallery pieces are packed four per box, canvas–framed pieces are also packed four per box, acoustic panels are packed four per box, and framed paper prints are packed six per box. These capacities come directly from the client documentation and are correctly followed in the output. Because all items in Case 2 fit within the dimensions of the standard box, it is expected and correct that the output includes only standard boxes and does not use large boxes or crates.
The expected_output.json also assigns containers in a way that matches the physical constraints of pallet sizes. Standard boxes with greater depth require oversized pallets, while shallower boxes can be placed on standard pallets. The distribution of container types shown in the output is consistent with these dimensional constraints. The numerical totals for cost, weight, number of containers, and number of boxes match exactly with the calculations that the solver performs, which confirms the correctness of the expected output. Each artwork in the input is successfully packed, and therefore the output appropriately shows zero unpacked items.

### Mixed-medium strategy assumed by our team

Case 2 relies heavily on the medium-isolation strategy defined by our team. Because the client has not specified how to pack boxes containing artworks of different mediums, allowing mixed-medium boxes would require making assumptions about cross-medium stacking rules, fragility, and per-box limits. To avoid making unsupported assumptions, our team decided to forbid mixing different mediums in the same box entirely. This rule applies even when two mediums share identical dimensions or similar material characteristics. In Case 2, this strategy results in boxes that contain only one medium type at a time: canvas items are boxed separately from acoustic panels, and both are boxed separately from framed prints. This strategy ensures consistent and safe packing behavior and avoids any ambiguity regarding improper medium combinations.
