# 高度な使い方

## 高解像度での描画

デフォルトでは4K解像度までの描画に対応しています。  
より高解像度での描画のためには、下記の通りに2つのRender Targetの解像度を所望の解像度以上に増やしてください。

1. メニューの「File > New Level...」から新しいレベルを開きます
2. コンテンツブラウザで下記のアセットを開きます

	- Plugins > VistaSplatPro Content > VistaSplatPro > RenderTarget > Canvas_RGBD
	- Plugins > VistaSplatPro Content > VistaSplatPro > RenderTarget > Canvas_Alpha

3. 詳細パネルで「Size X」「Size Y」を16の倍数で所望の解像度に変更します
4. アセットの変更を保存します

また、同様の操作で4Kより小さい解像度を指定することで、GPUメモリの消費を節約することもできます。

<!-- ## ソートバッファのサイズ変更

3D Gaussian Splattingの描画時、画面上のガウシアン（点）を奥行き方向にソートする処理があります。  
この際のソート対象を一時的に保持するメモリ領域のサイズを変更できます。  
デフォルトでは4096 x 4096です。この値を増やすことで、画面上に同時により多くのガウシアン（点）を描画できるようになります。  
データ量の多いモデルで、モデルの一部が欠けて表示されてしまう場合はこの値を増やしてください。

1. 「(プロジェクトフォルダ)\Plugins\VistaSplatPro\Source\VistaSplatProRenderer\VistaSplatProRenderer.build.cs」を開きます
2.  14行目の「PublicDefinitions.Add("SORTED_TEXTURE_WIDHT=4096");」の「4096」を任意の値（例えば「4096」）に変更します
3. 「(プロジェクトフォルダ)\Plugins\VistaSplatPro\Shaders\Private\VistaSplatProCommon.usf」を開きます
4.  7行目の「#define SORTED_TEXTURE_WIDHT 4096」の「4096」を上記と同じ値（例えば「4096」）に変更します
5. ファイルを保存し、プロジェクトを開きなおします。

また、同様の操作でより小さい値を指定することで、GPUメモリの消費を節約することもできます。 -->
