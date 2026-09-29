# US Construction Estimating Constants

A table of the constants that the [TakeoffMetric](https://takeoffmetric.com/) calculators use to turn dimensions into
order quantities: bag yields, aggregate and soil densities, swell and compaction ratios, rebar weights, dressed lumber
sizes, block counts, mortar rules of thumb, paver base depths, shingle coverage, asphalt unit weights and air properties
for duct sizing. Each row gives one value, its unit, an SI conversion, the condition it applies to, and a link to the
primary source it was read from.

Compiled 2026-09-29 by TakeoffMetric Editorial (TakeOffMetrics Research). 148 rows.

## Files

| File | Content |
|---|---|
| `constants.csv` | The data, UTF-8, comma-separated, one value per row |

## Columns

`id` · `category` · `material_or_item` · `quantity` · `value` · `unit` · `value_si` · `unit_si` · `condition` ·
`source_publisher` · `source_title` · `source_url` · `source_type` · `date_opened` · `used_by_tool_url` · `engine_file` ·
`engine_symbol` · `notes`

- `value` is written as the source prints it, in US customary units.
- `value_si` is a conversion of `value` with the exact NIST factors (1 lb = 0.45359237 kg, 1 ft = 0.3048 m), rounded to
  4 significant digits. Where the source prints its own metric figure and it differs by rounding, `notes` gives it.
- `source_type` is one of `federal_public_domain`, `manufacturer_datasheet`, `trade_association`, `supplier`, `other`
  (university extension services, state DOT specifications, a peer-reviewed paper, a national laboratory resource).
- `used_by_tool_url`, `engine_file` and `engine_symbol` may hold several entries separated by `; ` when more than one
  calculator uses the same value. The two engine columns point to the site's source code, which is not part of this
  package.

## Method

- Every value was read in the source document itself on the date in `date_opened`, and recorded in the site's source
  ledger with the passage it came from. A URL that answers is not treated as a source; the value has to be on the page.
- Only values the ledger marks verified are included. Values a calculator treats as its own editable assumption (for
  example the 150 lb/ft³ default for concrete) are not included.
- Ratios such as loose-to-compacted volume are arithmetic on two values of the same source row; `notes` shows the
  division.
- Building-code provisions and published tables (IRC, AWC, the Brick Industry Association's quantity tables, the CMHA
  grout table) are not reproduced here; the calculator pages link to them.
- No passage from any source is copied here: value, unit and link only.
- Each `value` was checked on 2026-09-29 against the number the calculator code holds at `engine_symbol`: 148 of 148
  match.

How the calculators use these values is described on the [methodology page](https://takeoffmetric.com/methodology/).

## Summary by category

| Category | Rows | Sources |
|---|---:|---|
| concrete | 11 | QUIKRETE data sheets, FHWA, NRMCA |
| rebar | 15 | Texas DOT specification, Nucor |
| aggregates | 25 | Caterpillar reference table, two suppliers, FHWA |
| earthwork | 18 | FHWA Federal Lands Highway |
| landscaping | 8 | university extension services |
| asphalt | 4 | Asphalt Institute, Minnesota Asphalt Pavement Association, Texas DOT |
| masonry | 17 | CMHA / NCMA |
| pavers | 8 | CMHA, Oregon State University Extension |
| roofing | 6 | GAF data sheets |
| lumber | 16 | NIST PS 20-20, University of Missouri Extension |
| framing | 8 | APA |
| decking | 4 | Trex installation guide |
| hvac | 8 | McGill AirFlow, PNNL, NASA Glenn Research Center, Purdue University |

By source type: manufacturer data sheet 44 · federal (public domain) 39 · trade association 37 · other 25 · supplier 3.

Two of the calculators that use these values, as examples: the
[concrete calculator](https://takeoffmetric.com/concrete/concrete-calculator/) (bag yields, unit weight) and the
[gravel calculator](https://takeoffmetric.com/earthwork/gravel-calculator/) (loose and bank densities). The
`used_by_tool_url` column lists the page for every row.

## Limits

- These are estimating values. Densities change with moisture, gradation and compaction; bag yields and coverage are for
  the named product line only. Confirm with your plans, your supplier and your local code before ordering or building.
- The `condition` column matters: a loose density, a bank density and a compacted density of the same material are
  different numbers, and using one for another changes the order quantity.
- FHWA Exhibit 5.1 A values describe highway embankment work. The calculators apply them as described in `notes`.

## License

CC BY 4.0 for the compilation; each value remains attributed to its source. Cite as: TakeoffMetric Editorial,
*US Construction Estimating Constants*, 2026, takeoffmetric.com. Values from federal publications are US
government works; values from other publishers stay attributed to them through `source_publisher` and `source_url`.
