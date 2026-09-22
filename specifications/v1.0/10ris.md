# 10-Inch Rack Interface Specification (10RIS), Version 1.0

| Field | Value |
| --- | --- |
| Identifier | 10RIS |
| Version | v1.0 |
| Published | 2026-09-22 |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Status | Published open specification proposal |

## Status of This Document

This is a published open specification proposal authored by Nodeqore. It is not an EIA standard, is not endorsed by EIA, and creates no certification programme. Implementers may make a self-declaration of compatibility only as described in this document.

The English text is authoritative. Any translation is explanatory and must defer to this version where a conflict exists.

## 1. Scope

10RIS defines a compact front mounting interface for rack-mounted equipment intended for home, lab, and small-office environments. Its purpose is to give enclosures, rails, panels, shelves, and accessories a common geometry without implying compatibility with 19-inch equipment.

The core requirements cover the front-panel width, rail mounting-hole centrelines, vertical mounting-hole spacing, and two mounting-hole types. Depth, rail construction, enclosure geometry, load rating, thermal performance, grounding, cable management, and accessory design are implementation guidance. They are not conditions of core interface compatibility.

## 2. Conventions and Terms

The key words **MUST**, **MUST NOT**, **REQUIRED**, **SHOULD**, **SHOULD NOT**, and **MAY** in this document are to be interpreted as described by [RFC 8174](https://www.rfc-editor.org/rfc/rfc8174.html) when, and only when, they appear in all capitals.

**Front-panel width** is the maximum width across the equipment face, including its mounting flanges or rack ears. **Rail mounting-hole centreline** is the vertical line through the centres of a rail's mounting-hole series and is the rail datum for horizontal interface dimensions. **Rail mounting-hole centre-to-centre spacing** is the distance between the centres of corresponding holes in the left and right front rails. **Clear opening** is the smallest unobstructed distance between the inner faces of the two front rails. **U** is a rack unit with a nominal height of 44.45 mm.

## 3. Core Interface Requirements

An implementation claiming 10RIS Core Interface Compatible MUST meet the following requirements at the front mounting plane:

| Interface property | Requirement | Interpretation |
| --- | ---: | --- |
| Maximum front-panel width | 254.00 mm maximum | Equipment may be narrower; it MUST NOT rely on more width. |
| Rail mounting-hole centre-to-centre spacing | 236.525 mm nominal | Corresponding left/right hole centres use this common nominal spacing. |
| Clear opening | 222.25 mm minimum | The result is measured between rail inner faces at the mounting plane. |
| Unit height | 44.45 mm nominal | One U repeats throughout a rail's usable height. |
| Vertical mounting-hole spacings within 1U | 15.875 / 15.875 / 12.70 mm | The three-hole spacing sequence repeats from U to U. |

Figure 1 is normative for the relationship between the horizontal dimensions. The rail mounting-hole centrelines and clear-opening limit remain independent; a rail's holes are not assumed to sit at its geometric centre.

10RIS intentionally specifies functional limits rather than unvalidated bilateral manufacturing tolerances. A manufacturer remains responsible for selecting tolerances, material, process controls, and inspection suitable to consistently meet these limits.

## 4. Mounting-Hole Types

An implementation MUST support at least one of these core mounting-hole types and MUST state which type it supports.

1. **9.5 mm square mounting holes.** Each mounting hole is a nominal 9.5 mm square suitable for a cage-nut system selected by the implementation.
2. **M6 threaded mounting holes.** Each mounting hole has an M6 thread.

The mounting-hole type applies to the same vertical mounting-hole spacing in both cases. A 3 mm semicircular relief, a particular rail cross-section, a chosen cage-nut thread, and any screw-head style are optional implementation choices; none changes core compatibility.

## 5. Reference Figures

The linked SVG source files are part of this document and are normative where identified. Their labels are designed for screen, print, and machine-independent download.

- [Figure 1 — Horizontal mounting interface](figures/figure-1-horizontal-interface.svg) (normative)
- [Figure 2 — Vertical mounting-hole spacing](figures/figure-2-vertical-rhythm.svg) (normative)
- [Figure 3 — 9.5 mm square mounting holes](figures/figure-3-square-profile.svg) (normative)
- [Figure 4 — M6 threaded mounting holes](figures/figure-4-m6-profile.svg) (normative)

### Build a Rack Reference

Create a basic front-elevation reference for a selected mounting-hole type and U height with the [10RIS Rack Reference Generator](https://www.nodeqore.com/tools/10ris-rack-reference-generator). The tool is non-normative and does not assess construction, depth, loading, or conformance.

## 6. Conformance and Self-Declaration

No Nodeqore review, badge, approval, or endorsement is implied by this specification. A product maker MAY state **“10RIS Core Interface Compatible, self-declared”** only after measuring a representative production configuration.

The declaration MUST identify the product and tested configuration, the supported mounting-hole type or types, the measured maximum front-panel width, the measured minimum clear opening, the measured rail mounting-hole centre-to-centre spacing used, the number of usable rack units (U), and the measurement date. It MUST name this document as **10-Inch Rack Interface Specification (10RIS), Version 1.0 — Authored by Nodeqore**.

## 7. Non-Normative Implementation Guidance

Depth is intentionally not a core compatibility requirement. EIA-310 mounting practice does not create a universal cabinet depth, and real equipment manuals specify their own rail and cabinet ranges. Manufacturers SHOULD declare usable installation depth, rail-adjustment range, rear cable-clearance envelope, and any front-door or rear-door clearance before a buyer selects an enclosure.

For context, IBM and Cisco installation materials describe cabinet/rail requirements for their own equipment, not a universal 10-inch depth: [IBM rack specifications](https://www.ibm.com/docs/en/power5?topic=sheets-specifications-non-rack-installation) and [Cisco cabinet and rack requirements](https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus9000/hw/n9348y12c-se1/cisco-n9348y12c-se1-switch-installation-guide/prepare-to-install/rack-and-cabinet-requirements.html).

Load, wall anchoring, cooling, electrical safety, and grounding require product-specific engineering. An enclosure MUST NOT use a 10RIS compatibility claim to imply a load rating, wall-installation approval, thermal capacity, or electrical compliance.

## 8. Changes and Feedback

Version 1.0 is the initial published version. Later versions will keep their own stable URLs and change records; a compatible implementation MUST cite the version it used.

Submit errata or change proposals through the [10RIS public GitHub Issues](https://github.com/nodeqore/10ris/issues). Reports should identify the version, relevant figure or section, hardware configuration, measured values, and a reproducible interoperability concern.

## 9. Licence, Attribution, and Trademarks

The text and reference SVG figures in this 10RIS v1.0 document are licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). Reuse must preserve appropriate attribution, link the licence, and indicate modifications. A suggested attribution is: “10-Inch Rack Interface Specification (10RIS), Version 1.0 — Authored by Nodeqore, CC BY 4.0.”

Nodeqore names, logos, and trademarks are not licensed by CC BY 4.0. This document is a technical proposal, not legal, safety, certification, or compliance advice.
