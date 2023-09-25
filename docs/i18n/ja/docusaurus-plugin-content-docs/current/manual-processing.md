---
sidebar_position: 7
---

# 手動処理

VRChat向けにアバターを作る場合は、通常Modular Avatarに自動でアバターを処理させてもよいはずです。
プレイモードに入るか、アバターをビルドすると、Modular Avatarが自動的に処理を行います。
しかし、VRChat以外のプラットフォーム向けにアバターを作る場合や、アバターの問題をデバッグする場合など、手動でModular Avatarの処理を適用する必要が生じることもあります。

アバターを右クリックし、`Modular Avatar -> Manual bake avatar`を選択することで、手動で処理することができます。
Modular Avatarは、すべての変換を適用したアバターのコピーを作成します。

![Manual Bake Avatar option](manual-bake-avatar.png)

:::caution

手動処理の場合、Modular Avatarによって生成されるメッシュ等が自動的に削除されず、実行した分だけ溜まります。
自動生成されるアセットは`ModularAvatarOutput`というフォルダーにまとめられますので、生成されたアバターは使い終わったら削除してもかまいません。

:::

## 生成されたアセット

Modular Avatarは、アバターに付いているコンポーネントに基づいて、一時的にいくつかのアセットを生成します。
アバターを手動で処理すると、この一時アセットがプロジェクトのAssetsフォルダー内にある`ModularAvatarOutput`フォルダーに保存されます。
初めはすべてのアセットが1つのファイルに格納されています。これは、Unityのバグを回避し、処理時間を短縮するために必要です。
ただし、プロジェクトビューでこのファイルを選択し、インスペクターで`Unpack`をクリックすると展開することができます。

![Unpack button](manual-bake-unpack.png)

`Unpack`を押すと、生成されたアセットが別々のファイルに展開されます。

Unpackするかどうかにかかわらず、手動処理で生成されたアバターを削除した後は`ModularAvatarOutput`フォルダーを削除しても大丈夫です。