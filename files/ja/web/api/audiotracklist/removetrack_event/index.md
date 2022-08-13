---
title: 'AudioTrackList: removetrack イベント'
slug: Web/API/AudioTrackList/removetrack_event
tags:
  - AudioTrackList
  - Event
  - events
  - removeTrack
translation_of: Web/API/AudioTrackList/removetrack_event
---
{{APIRef}}

`removeTrack` イベントは、トラックが {{domxref("AudioTrackList")}} から取り除かれたときに発生します。

| バブリング                 | なし                                                             |
| -------------------------- | ---------------------------------------------------------------- |
| キャンセル                 | 不可                                                             |
| インターフェイス           | {{domxref("TrackEvent")}}                                 |
| イベントハンドラプロパティ | [`onremovetrack`](/ja/docs/Web/API/AudioTrackList/onremovetrack) |

## 例

`AddEventListener()` を使用する場合

```js
const videoElement = document.querySelector('video');

videoElement.audioTracks.addEventListener('removetrack', (event) => {
  console.log(`Audio track: ${event.track.label} removed`);
});
```

`onremovetrack` イベントハンドラプロパティを使用する場合

```js
const videoElement = document.querySelector('video');

videoElement.audioTracks.onremovetrack = (event) => {
  console.log(`Audio track: ${event.track.label} removed`);
};
```

## 仕様

| 仕様                                                                                                         | 状態                             |
| ------------------------------------------------------------------------------------------------------------ | -------------------------------- |
| {{SpecName('HTML WHATWG', 'media.html#event-media-removetrack', 'removetrack')}} | {{Spec2('HTML WHATWG')}} |

## ブラウザーの互換性

{{Compat("api.AudioTrackList.removetrack_event")}}

## See also

- 関連情報: [`addtrack`](/ja/docs/Web/API/AudioTrackList/addtrack_event), [`change`](/ja/docs/Web/API/AudioTrackList/change_event)
- [`VideoTrackList`](/ja/docs/Web/API/VideoTrackList) 対象でのこのイベント: [`removetrack`](/ja/docs/Web/API/VideoTrackList/removetrack_event)
- [`MediaStream`](/ja/docs/Web/API/MediaStream) 対象でのこのイベント: [`removetrack`](/ja/docs/Web/API/MediaStream/removetrack_event)
- [Media Streams API](/ja/docs/Web/API/Media_Streams_API)
- [WebRTC API](/ja/docs/Web/API/WebRTC_API)