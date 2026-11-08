---
title: "Overview"
weight: 10
---

# go-streamkit {#go-streamkit}

Site-agnostic transport for streaming media: a retrying, rate-limited HTTP client, an HLS playlist parser and writer, and an MPEG-DASH manifest reader and writer.

The writers (v0.1.0) produce VOD playlists and static MPDs for CMAF/fMP4 and
WebVTT segments, such as the ones go-avkit's `container.Segment` cuts: HLS media
and master playlists (AUDIO and SUBTITLES renditions) through
[Eyevinn/hls-m3u8](https://github.com/Eyevinn/hls-m3u8), and an `isoff-live`
MPD with `SegmentTemplate` and `SegmentTimeline` through
[Eyevinn/dash-mpd](https://github.com/Eyevinn/dash-mpd). URIs and names are
validated (no traversal, no injected tags). No live playlists, no encoding
ladders, no encryption.

Part of the **Graphics, images & media** family of the
[pure-Go ecosystem](https://go-desktop.github.io/) — 1 module,
all `CGO_ENABLED=0`.

## What is here {#what-is-here}

This site is the organisation's reference index: what each module is, and where its
API documentation lives. The API itself is generated from the source and served by
[pkg.go.dev](https://pkg.go.dev/), which is always current with the released tags —
duplicating it here would only create a second copy to go stale.

- **[Modules]({{< relref "modules.md" >}})** — every module in go-streamkit, with its source and its reference.

## What every module here is held to {#what-every-module-here-is-held-to}

- `CGO_ENABLED=0`: no cgo, and no shelling out to a command-line tool in place of a
  library.
- Built and tested on amd64, arm64, riscv64, loong64, ppc64le and s390x — the last
  being big-endian, which keeps every on-disk and on-wire encoding honest.
- 100% statement coverage as a CI gate, error branches included.
- BSD-3-Clause.

The standard is described in full on the
[ecosystem map](https://go-desktop.github.io/docs/latest/standards/).
