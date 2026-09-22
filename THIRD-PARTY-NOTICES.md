# Third-party notices

What Cave Aurora Edge and its companion bridge include from other people, and under
what terms.

## Lucide icons

The outline icons in `CaveAuroraEdge/scripts/views/icons.js` are adapted from
[Lucide](https://lucide.dev).

ISC License

Copyright (c) for portions of Lucide are held by Cole Bemis 2013-2022 as part of
Feather (MIT). All other copyright (c) for Lucide are held by Lucide Contributors 2022.

Permission to use, copy, modify, and/or distribute this software for any purpose with
or without fee is hereby granted, provided that the above copyright notice and this
permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD
TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO
EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL
DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN
AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN
CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

## iCUE widget wrappers

`CaveAuroraEdge/common/plugins/*.js` are Corsair's official iCUE widget API wrappers,
included as the iCUE widget framework requires. Each is copied byte for byte from
`C:\Program Files\Corsair\Corsair iCUE5 Software\widgets\common\plugins\` and is
© Corsair Memory, Inc. — `IcueWidgetApiWrapper.js`, `SimpleMediaApiWrapper.js` and
`SimpleSensorApiWrapper.js`, all three from the iCUE 5 build that ships
`WidgetbuilderSensorsdataproviderQmlPlugin.dll` for Corsair_iCUE_RJ_v5.49 (file date
15 Aug 2026). They are not modified here; only the line endings are normalised to LF
to match `.gitattributes`.

## NAudio

The companion bridge uses [NAudio](https://github.com/naudio/NAudio) (MIT).
