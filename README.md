# US Construction Estimating Constants

A table of the constants that the [TakeoffMetric](https://takeoffmetric.com/) calculators use to turn dimensions into
order quantities: bag yields, aggregate and soil densities, swell and compaction ratios, rebar weights, dressed lumber
sizes, block counts, mortar rules of thumb, paver base depths, shingle coverage, asphalt unit weights and air properties
for duct sizing. Each row gives one value, its unit, an SI conversion, the condition it applies to, and a link to the
primary source it was read from.

Compiled 2026-09-29 by TakeoffMetric Editorial (TakeOffMetrics Research). 148 rows.

**Version 1.1.0 (2026-10-04).** 55 of the 148 rows keep their source, link and dates but carry no value: their publishers'
terms of use do not allow republication, or could not be read (`values_withheld`, `withheld_hosts`). The 93 other values
are unchanged from 1.0.0. Row HVC-003 is now credited to its three authors (Liu, Long & Chen, 2012), and its quantity
states that the figure is the roughness of the galvanized duct fittings in that study.

**Version 1.1.1 (2026-10-09).** Three source links that redirected now point to their final address, same document:
the QUIKRETE No. 1101 data sheet (rows CON-001 to CON-005), NIST PS 20-20 Revision 1 (LUM-002 to LUM-016) and the archived
GAF RESHR112 sell sheet (ROF-003). No value, unit or condition changed.

## Files

| File | Content |
|---|---|
| `constants.csv` | The data, UTF-8, comma-separated, one value per row |

## Columns

`id` · `category` · `material_or_item` · `quantity` · `value` · `unit` · `value_si` · `unit_si` · `condition` ·
`source_publisher` · `source_title` · `source_url` · `source_type` · `date_opened` · `used_by_tool_url` · `engine_file` ·
`engine_symbol` · `notes` · `values_withheld` · `withheld_hosts`

- `value` is written as the source prints it, in US customary units.
- `value_si` is a conversion of `value` with the exact NIST factors (1 lb = 0.45359237 kg, 1 ft = 0.3048 m), rounded to
  4 significant digits. Where the source prints its own metric figure and it differs by rounding, `notes` gives it.
- `source_type` is one of `federal_public_domain`, `manufacturer_datasheet`, `trade_association`, `supplier`, `other`
  (university extension services, state DOT specifications, a peer-reviewed paper, a national laboratory resource).
- `values_withheld` is `true` when `value` and `value_si` are left empty because the publisher's terms of use forbid
  republication or could not be read; `withheld_hosts` names the domain(s) concerned. Read the value at `source_url`.
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
  matched in 1.0.0; the 93 values kept in 1.1.0 are those same values.
- On 2026-10-04 the terms of use of every publisher were looked up. A value is kept when it comes from a US federal
  publication (public domain), from a publisher whose terms allow reuse, or from a publisher that has no terms page;
  where the terms forbid republication or could not be read, the value is withheld.

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
| hvac | 8 | McGill AirFlow, PNNL, NASA Glenn Research Center, Liu, Long & Chen (ASHRAE RP-1493) |

By source type: manufacturer data sheet 44 · federal (public domain) 39 · trade association 37 · other 25 · supplier 3.

## Calculators that read these values

Counted from the `used_by_tool_url` column: 19 calculator pages on takeoffmetric.com read at least one row of this
table. A row that several calculators use is counted once for each of them.

| Calculator page | Rows |
|---|---:|
| [takeoffmetric.com/earthwork/gravel-calculator/](https://takeoffmetric.com/earthwork/gravel-calculator/) | 24 |
| [takeoffmetric.com/earthwork/fill-dirt-calculator/](https://takeoffmetric.com/earthwork/fill-dirt-calculator/) | 18 |
| [takeoffmetric.com/masonry/concrete-block-calculator/](https://takeoffmetric.com/masonry/concrete-block-calculator/) | 17 |
| [takeoffmetric.com/framing/board-foot-calculator/](https://takeoffmetric.com/framing/board-foot-calculator/) | 16 |
| [takeoffmetric.com/concrete/rebar-calculator/](https://takeoffmetric.com/concrete/rebar-calculator/) | 15 |
| [takeoffmetric.com/measure/cubic-yard-calculator/](https://takeoffmetric.com/measure/cubic-yard-calculator/) | 12 |
| [takeoffmetric.com/concrete/concrete-calculator/](https://takeoffmetric.com/concrete/concrete-calculator/) | 10 |
| [takeoffmetric.com/earthwork/topsoil-calculator/](https://takeoffmetric.com/earthwork/topsoil-calculator/) | 10 |
| [takeoffmetric.com/masonry/paver-base-calculator/](https://takeoffmetric.com/masonry/paver-base-calculator/) | 10 |
| [takeoffmetric.com/decks-fences/deck-calculator/](https://takeoffmetric.com/decks-fences/deck-calculator/) | 9 |
| [takeoffmetric.com/earthwork/sand-calculator/](https://takeoffmetric.com/earthwork/sand-calculator/) | 8 |
| [takeoffmetric.com/framing/wall-framing-calculator/](https://takeoffmetric.com/framing/wall-framing-calculator/) | 8 |
| [takeoffmetric.com/hvac/duct-calculator/](https://takeoffmetric.com/hvac/duct-calculator/) | 8 |
| [takeoffmetric.com/roofing/roofing-calculator/](https://takeoffmetric.com/roofing/roofing-calculator/) | 6 |
| [takeoffmetric.com/concrete/concrete-cost-calculator/](https://takeoffmetric.com/concrete/concrete-cost-calculator/) | 5 |
| [takeoffmetric.com/concrete/footing-calculator/](https://takeoffmetric.com/concrete/footing-calculator/) | 5 |
| [takeoffmetric.com/decks-fences/fence-calculator/](https://takeoffmetric.com/decks-fences/fence-calculator/) | 5 |
| [takeoffmetric.com/paving/asphalt-calculator/](https://takeoffmetric.com/paving/asphalt-calculator/) | 4 |
| [takeoffmetric.com/stairs/stair-stringer-calculator/](https://takeoffmetric.com/stairs/stair-stringer-calculator/) | 1 |

## Limits

- These are estimating values. Densities change with moisture, gradation and compaction; bag yields and coverage are for
  the named product line only. Confirm with your plans, your supplier and your local code before ordering or building.
- The `condition` column matters: a loose density, a bank density and a compacted density of the same material are
  different numbers, and using one for another changes the order quantity.
- FHWA Exhibit 5.1 A values describe highway embankment work. The calculators apply them as described in `notes`.

## License

CC BY 4.0 covers the compilation: the selection and arrangement of the rows, the SI conversions, the conditions and the
notes. It does not cover third-party values: values from US federal publications are government works in the public
domain, and every other value stays under its publisher's terms, cited row by row through `source_publisher` and
`source_url`. Cite as: TakeoffMetric Editorial, *US Construction Estimating Constants*, version 1.1.1, 2026,
takeoffmetric.com.
