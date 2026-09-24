# Counter project — instructions

Paste this into the project's **Instructions** box. It tells every new chat in the project
what exists, how it is built, and the rules to work by.

---

## What this project is

A school snack counter run by a special-education class, and the tools that go with it.
Everything is built from one product list and is used on an iPad at the counter or by students.

**The counter:** snacks and drinks, mostly $1.00. 71 products; 68 have a verified barcode.
Prices: 59 at $1.00, 7 at $1.50, 5 at $2.00 (the two Dunkin' coffees are $2.00).

**Still missing a barcode:** 7UP, MM BLACK RASPBERRY, RICE KRISPIES TREATS.
**Known problems:** the HONEY BUN and HONEY BUN FROSTED photos show the wrong packages
(Little Debbie and Hostess instead of Duchess). GATORADE COOL BLUE uses 052000102871,
which is listed elsewhere as Frost Glacier Freeze — worth checking against the bottle.

## The tools

| Tool | What it does | Who uses it |
|---|---|---|
| **Scan Log** | The real till. Scans barcodes, rings up a customer, takes cash, works out change, keeps the day's totals. | Staff and students at the counter |
| **Scan Log Practice** | A pretend till. Ring up a customer, make change. 9 levels, accuracy scores, PDF and spreadsheet of results. | Students, with a teacher |
| **Shelf Check** | Yes/no inventory list with photos, read-aloud, counts, PDF at the end. | Students |
| **Stock the Shelf** | Stocking game: match the tag, sort by aisle, check the UPC, restock. Levels, accuracy tracking, PDF per sitting. | Students |
| **Shelf tags** | Printed price tags with photo, price and a real UPC-A barcode. | The shelves themselves |
| **Tag Book / Product Lookup / Missing UPC Worksheet** | Supporting pages: browse and reprint tags, look a barcode up, fill in missing codes. | Staff |

All of them are single self-contained HTML files with the photos embedded, and they also
run as a website with no Claude account (see **Hosting** below).

## Rules to work by

1. **One change reaches everything.** The product list is the source of truth. A price, name,
   photo or barcode change must flow to: the CSV, the tag PDF, the catalogue PDF, Scan Log,
   Product Lookup, Tag Book, the Missing UPC Worksheet, Shelf Check, Scan Log Practice and
   Stock the Shelf. Never update one and leave the others.
2. **No barcode is filed without checking it.** UPC-A check digit must be correct
   ((10 − ((3×odd + even) mod 10)) mod 10), the code must not already belong to another product,
   and the GS1 prefix should match the brand. If a scan looks wrong, hold it and ask.
3. **Don't reprint every tag.** When something changes, produce a small PDF of only the
   affected tags.
4. **Built for special education.** Big targets that do not move, plain words, pictures before
   text, read-aloud where it helps, gentle wording on mistakes. Say "that one is not on the list",
   never "wrong". Respect Reduce Motion.
5. **Student data stays on the device** it was used on, and is only ever handed over as a PDF,
   a spreadsheet, an email or text the teacher copies. Nothing is uploaded anywhere.
6. **Test before handing anything over.** Run the actual page, do the thing a student would do,
   and check the numbers on screen match the PDF and the spreadsheet.

## Hosting

The tools are published as Claude artifacts (handy, but **file downloads only work for signed-in
members of the organization**) and as a plain website with no Claude involved, where downloads
work for everyone. The website version is the one students use.

Website files, all in one folder: `index.html` (home page linking the others), `practice.html`,
`stock-the-shelf.html`, `shelf-check.html`, `scan-log.html`.

## Artifact links

- Scan Log — https://claude.ai/artifact/Ut4gJJ71kpZEiZJg2FQXdL
- Scan Log Practice — https://claude.ai/artifact/NANH4M4PCTCoZwKTLMgzkV
- Shelf Check — https://claude.ai/artifact/TtHPNkvXEBzrP47P8cBaAd
- Stock the Shelf (teacher copy) — https://claude.ai/artifact/BxMFDqQyFYUDXNsJZbB4XL
- Stock the Shelf (student copy) — https://claude.ai/artifact/CEYLUbRgRjLqZ5PBowVcRG
- Tag Book — https://claude.ai/artifact/75dtUArCQiUN5iJquTahuk
- Product Lookup — https://claude.ai/artifact/Qe4zzueR6aBxyKFtXFzzxD
- Missing UPC Worksheet — https://claude.ai/artifact/6PDh579JAiQhi7RtX3DH2S

## What to do first in a new chat

Read `product_catalog.csv` (attached to this project) before changing anything about products.
If the work is about one of the tools, ask for the current file or the artifact link, because the
version in the project may be older than the one in use.
