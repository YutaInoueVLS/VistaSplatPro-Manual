# Vista Splat Proって何？

[Vista Splat Pro](https://vls.co.jp/vistasplatpro.html)は、[3D Gaussian Splatting](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/)のデータをUnreal Engineでリアルタイム描画するためのプラグインです。

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/xxxxxxxxxxxxx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->

- このプラグインは、Unreal Engineのレンダリングパイプラインに独自の描画パスをエンジン改造無しで追加することで、3D Gaussian Splatting本来の描画手法に基づいた正確な描画を行います。
- 3D Gaussian Splattingのモデルに、Unreal Engine内の他のオブジェクトから動的な影を落とすことができます。
- 複数のモデルを配置可能です。