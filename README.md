# PJSoft Scrolling Capture

Portable Windows utility for capturing scrolling content, combining and editing screenshots, building compact overviews from selected areas, and exporting to PNG or PDF.

Available in **English, Czech (Rolovací výstřižek), Spanish and German**. No installation is required.

## Download

[Download the latest release](https://github.com/petrjones/ScrollingCapture/releases/latest)

Open the release's **Assets** section, download the **ScrollingCapture-…-Windows-x64.zip** package, extract it into a folder, and run the included **ScrollingCapture-….exe**. The ZIP also includes user guides and the QRCoder license.

[Release history and update notes](https://github.com/petrjones/ScrollingCapture/releases)

## Three capture modes

- **Scrolling capture:** select a region, scroll its content automatically, and merge overlapping screenshots. Adaptive recovery can use smaller steps to recover missing intermediate content. Progress and Stop/Esc controls let you interrupt capture and review the verified content captured so far.
- **Manual series:** collect screenshots and combine them vertically or horizontally. Reorder them with buttons or drag and drop, remove selected items with Delete, and clear the series. A configurable keyboard shortcut can add screenshots.
- **Read menu:** read text items from supported accessible menus, optionally number them starting at a selected position, and export them to TXT, PNG or PDF. The list can also be added to a manual series or cleared for another menu.

## Preview, editing and seam repair

Review the combined image before saving. Use 100% zoom, fit-to-width, zoom controls and mouse panning to inspect readability and joins.

The editor includes cropping, arrows, highlighting and **opaque black redaction**. Redactions become part of the exported image; OCR works on the edited result. Overlapping screenshots can also be aligned manually by dragging in the seam repair window. Repair seams before applying image edits.

## Build an overview: keep the essential parts

Select several separate rectangular areas from a long capture and assemble them vertically into one compact document. For example, keep a product photograph, its specifications and warranty terms while leaving out advertisements and unrelated sections.

- Choose areas in the preview editor and arrange their order with buttons or drag and drop.
- Add an optional title above each area and a note below it.
- Preview the assembled overview before applying it.
- Return to the image editor for additional edits and PNG/PDF export. Undo restores the previous image.

Selected image pixels retain their original size, with narrow areas aligned to the left. Area selections and captions are not stored as a separate editable project.

## PDF export and A4 page layout

Export a single long-sheet PDF or a multi-page A4 PDF, in portrait or landscape, with optional searchable text from local Windows OCR.

A4 formats include a **page layout preview before export**:

- Add a manual page break by choosing **Start a new page here** and clicking before the content to move.
- Drag an automatic or manual break line to adjust the boundary. Optional snapping helps locate nearby gaps.
- Remove manual breaks, reset to automatic splitting, or undo changes.
- Keep selected overview areas, including titles and notes, together when they fit on one page. Taller areas still need splitting.
- Return to the editor while retaining the manual page plan for an unchanged image. Image edits reset the plan because its coordinates may have changed.

A manual break moves the following **full-width** image content to the next page. It does not reflow text or move an independent rectangular cutout. Blank space at the end of a manually shortened page is intentional. Preview guides are not exported. Always review boundaries where columns, tables or pictures cross them.

## Scrolling settings and changing content

The capture extent is measured in **selected-area heights**, rather than a fixed screenshot count. Overlaps and corrective steps can therefore require additional screenshots without shortening the requested extent. Capture ends earlier when the bottom is detected; image-size and memory safeguards also apply.

Delay, scroll strength, extent, fixed header, return-to-top preference, output format and last selected folder are remembered. A Reset settings button restores the capture defaults. Use a fixed-header value of 0 when the selected area has no fixed header.

Matching stable content helps tolerate changing advertisements or animations, and corrective backtracking is bounded. This does not freeze the website; major layout changes or insufficient stable content can still prevent a complete capture. Always check the result.

## Capturing administrator windows

If the target application, such as PowerShell or Windows Terminal, runs as administrator, also start Scrolling Capture with **right-click → Run as administrator**, then select the capture area again. Windows may otherwise block simulated scrolling. Changing delay or scroll strength does not remove that permission restriction. For ordinary target windows, normal launching is sufficient.

A small line near the top of the **Scrolling capture** tab explains this and confirms when Scrolling Capture is already running as administrator. The application also checks target permissions when available, reports rejected wheel input, and warns when the content never starts moving. It does not elevate itself automatically.

## Requirements and languages

- Windows 10 or Windows 11, **64-bit**.
- **.NET Framework 4.8**.
- Available Windows OCR language support for searchable PDF export.

The interface, editor and guides support **English, Czech, Spanish and German**. Select a language in the application and restart to apply it. A saved selection takes priority over automatic language detection.

Scrolling capture and menu reading depend on the target application. Custom or virtualized controls may not be supported. The executable is not digitally signed.

## Updates

Use **About → Check for updates** to compare the running version with the latest stable GitHub release. Optional automatic checking runs after launch at most once every 24 hours and announces a newer release in the main window.

Nothing is downloaded or installed automatically. Open the release page, download the new ZIP, extract it into a folder, and run the new executable. If moving to another folder, copy `ScrollingCapture.shortcut.txt` from the previous application folder if you want to keep the configured capture shortcut.

## Settings

Capture, language, update and contribution preferences are stored under the current Windows account in:

```text
%LOCALAPPDATA%\PJSoft\ScrollingCapture\settings.json
```

The capture shortcut is stored in `ScrollingCapture.shortcut.txt` beside the executable.

## Free to use

All features are available free of charge. Voluntary contributions support development and do not unlock additional features. Contribution reminders can be disabled. The application does not verify payments.

## Third-party component

Includes **QRCoder** under the **MIT license**. Its license is included in the download and is available through the application's About dialog.

---

Developed by **PJSoft**.
