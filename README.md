# vs2010-nuget
nuget packageを使用したバージョン管理についてのメモ

## NuGetとは
Visual Studioプロジェクトの (パッケージとして配置される) ライブラリの追加、更新、および削除を容易にするVisual Studioの拡張機能
dll参照と違いバージョン管理しやすい

## 導入方法
### NuGetのインストール
Visual Studio ギャラリー
https://marketplace.visualstudio.com/

・「NuGet Package Manager」と検索しダウンロードして、実行

・Visual Studio 2010を再起動すれば、NuGetがインストールされている

### プロキシの設定
参照：https://kaji-3.hatenablog.com/entry/2012/08/08/063450

・C:\\Program Files (x86)\Microsoft Visual Studio 10.0\Common7\IDE\devenv.exe.configを開き、最後の方にあるsystem.net項目を下記のように編集

```
<system.net>
    <settings>
        <ipv6 enabled="true"/>
    </settings>
    <defaultProxy useDefaultCredentials="true" enabled="true">
      <proxy usesystemdefault="true"/>
    </defaultProxy>
</system.net>
```
### 確認
適当なプロジェクトを開き、参照設定を右クリックすると、「NuGetパッケージの管理」が追加されているはず


https://qiita.com/nia_tn1012/items/0815e1f493ac49d20d41
