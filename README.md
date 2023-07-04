# Human IKRigGenerator
## 概要
本ツールは人型の **"IK Rig"**, **"IK Retargeter"** を生成できるEditor Utility Widget（以下、EUW）です。<br>
IK Rigについては[公式ドキュメント](https://docs.unrealengine.com/5.0/ja/unreal-engine-ik-rig/)をご参照下さい。

<img src="https://github.com/LeonGameworks/Screenshot/blob/c1899419d8818065fd21bb6220dc4b86a4542d6d/Human_IKRigGenerator/EUW.png" width="600">


[おかずさんのツイート](https://twitter.com/pafuhana1213/status/1672935116119871488)を参考に本ツールを作成させて頂きました！
<br>
<br>
## 使い方
1. 本プロジェクトをダウンロードし、プロジェクトを起動します。
2. コンテンツブラウザ上で **"/Content/IKRigGenerator/EUW_Human_IKRigGenerator"** を右クリックし、**"Run Editor Utility Widget"** を実行します。<br><img src="https://github.com/LeonGameworks/Screenshot/blob/965bec76829d81763c4e95a0df865fc902e64805/Human_IKRigGenerator/Run.png" width="500">
3. 各種設定を行い、"Generate"ボタンからアセットを生成します。<br><img src="https://github.com/LeonGameworks/Screenshot/blob/9da36b2b5a1594f14d3a09f3affc6db6966a01fa/Human_IKRigGenerator/EUWSettings.png" width="800">
4. "Save Config"、"Load Config" から構成の保存、読み込みができます。
<br>
<br>

## 他プロジェクトへの移行手順
1. 移行先のプロジェクトで **"Json Blueprint Utilities"** と **"Blueprint File Utilities"** プラグインを有効にし、エディターを再起動します。<br><img src="https://github.com/LeonGameworks/Screenshot/blob/2b179ee744028933960940d554c23aa33a08e85f/Human_IKRigGenerator/Plugin1.png" width="800"><br><img src="https://github.com/LeonGameworks/Screenshot/blob/2b179ee744028933960940d554c23aa33a08e85f/Human_IKRigGenerator/Plugin2.png" width="800">
2. EUW_Human_IKRigGenerator を右クリックから **Migrate** を実行します。<br><img src="https://github.com/LeonGameworks/Screenshot/blob/eba28e5189242287c414148a38220ee6bd8d9b72/Human_IKRigGenerator/Migrate.png" width="500">
3. 移行先の Content フォルダを指定すれば完了です。
<br>
<br>

## 技術的な補足
### アニメーションのリターゲット
Anim Sequence等のリターゲットについては手動の方がしやすいかと思われましたのでツールのUIからは除外しておりますが、機能は用意しておりますので必要な場合は "GenerateAnimSequence" という関数をご活用下さい。

### Configファイルについて
設定ファイルは **"[Project Dir]/Saved/IKRigGenerator/Config.json"** として保存されております。
ツールの簡略化のため、保存ファイルは１つのみとしております。また、Jsonファイルを共有すれば他の環境でも読み込み可能です。

### 人型限定？
人型以外でも活用可能です。
ただ、FullBodyIKの適用など基本人型を前提に検証、作成しております。
<br>
<br>
## プロジェクトバージョン
UE5.2

## 履歴
- 2023/07/03　プロジェクト公開