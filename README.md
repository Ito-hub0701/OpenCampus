# OpenCampus

Unityで制作した、オープンキャンパス向けのリアルタイム画像処理デモです。

Webカメラ映像に対してリアルタイムで画像処理を行い、
「コンピュータが画像をどのように見ているか」を体験できる展示を目指しています。

--- # Features ## Basic Filters | Mode | Description | |---|---| | Normal | 通常表示 | | Gray | グレースケール変換 | | Threshold | 二値化処理 | | Invert | 色反転 | --- ## Color Detection HSV 色空間を利用して特定色を抽出します。 | Mode | Description | |---|---| | Red | 赤色のみ抽出 | | Blue | 青色のみ抽出 | | Green | 緑色のみ抽出 | 検出対象以外は暗く表示することで、対象色を強調しています。 --- ## Image Effects | Mode | Description | |---|---| | Mosaic | モザイク処理 | | Posterize | ポスタライズ処理 | | Blur | ガウシアン風ぼかし | | Emboss | エンボス加工 | | Edge | エッジ検出 | --- ## Motion / Temporal Effects | Mode | Description | |---|---| | Motion | フレーム差分による動体検出 | | AfterImage | 残像エフェクト | --- ## Glitch / Visual Effects | Mode | Description | |---|---| | RGBSplit | RGB チャンネル分離 | | Glitch | ランダム画面ずらし演出 | --- # Technologies Used - Unity - C# - WebCamTexture - Texture2D - Real-time pixel processing --- # Processing Overview 毎フレーム `WebCamTexture.GetPixels32()` を使用してカメラ画像を取得し、 各ピクセルに対して画像処理を実行しています。 ```csharp Color32[] pixels = webcamTexture.GetPixels32();

# ライセンス

MIT License
(自由に使っていいけど最低限のルールだけ守ってね)

