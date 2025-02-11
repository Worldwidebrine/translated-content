---
title: AudioScheduledSourceNode
slug: Web/API/AudioScheduledSourceNode
l10n:
  sourceCommit: 6b8b53f565c67eb22fd78f8dec036c4694ad18d4
---

{{APIRef("Web Audio API")}}

`AudioScheduledSourceNode` インターフェイス（ウェブ音声 API の一部）は、オーディオソースノード各種の親インターフェイスであり、必要に応じ、指定された時間で開始や停止を行う機能を持ちます。具体的には、このインターフェイスでは、{{domxref("AudioScheduledSourceNode.start", "start()")}} や、{{domxref("AudioScheduledSourceNode.stop", "stop()")}} メソッドの他、{{domxref("AudioScheduledSourceNode.ended_event", "ended")}} イベントを定義しています。

> **メモ:** `AudioScheduledSourceNode` オブジェクトは、直接作成することはできません。
> かわりに、{{domxref("AudioBufferSourceNode")}} や、{{domxref("OscillatorNode")}}、または {{domxref("ConstantSourceNode")}} を使用してください。

特に明記しない限り、 `AudioScheduledSourceNode` をベースにしたノードは、再生されていない時（つまり、 `start()` の前や、 `stop()` の後）は、無音を出力します。無音は、値がゼロ (0) であるサンプルストリームを、常に流し続けることで表現されています。

{{InheritanceDiagram}}

## インスタンスプロパティ

_親インターフェイスである {{domxref("AudioNode")}} からプロパティを継承しています。_

## インスタンスメソッド

_親インターフェイスである {{domxref("AudioNode")}} からメソッドを継承しており、さらに以下のメソッドがあります。_

- {{domxref("AudioScheduledSourceNode.start", "start()")}}
  - : 指定した時刻に、ノードが特定の音を再生するようスケジュールします。時刻を指定しない場合、ノードはすぐに再生を開始します。
- {{domxref("AudioScheduledSourceNode.stop", "stop()")}}
  - : 指定した時刻に、ノードの再生を停止するよう、スケジュールします。時刻を指定しない場合、ノードはすぐに停止します。

## イベント

これらのイベントは [`addEventListener()`](/ja/docs/Web/API/EventTarget/addEventListener) を使用するか、このインターフェイス `onイベント名` プロパティにイベントリスナーを代入することで待ち受けすることができます。

- [`ended`](/ja/docs/Web/API/AudioScheduledSourceNode/ended_event)
  - : ソースノードが、所定の停止時間に達した、音声の全時間が演奏された、あるいはバッファの全体が演奏されたなどの理由で、再生を停止したときに発行されます。

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- [ウェブ音声 API の使用](/ja/docs/Web/API/Web_Audio_API/Using_Web_Audio_API)
- {{domxref("AudioNode")}}
