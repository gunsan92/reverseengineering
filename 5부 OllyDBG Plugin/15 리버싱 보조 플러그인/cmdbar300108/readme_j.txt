CommandBar ; Plugin for OllyDbg

OllyDbg に付属の command line プラグインを改造して、最下部に貼りついたバータイプにしました。

幾つかのコマンドと、コマンド候補表示機能を追加しています。

コマンドについては、command line プラグインのヘルプを参照ください。

v3.00.108
 ・マクロ機能を実装しました。
    pluginと同じフォルダに "macro.def"を置いてください。
    マクロの書き方は、macro.def の中身を参照してください。

 ・設定ファイルを ollydbg.ini から CmdBar.ini に変更しました。
    プラグインの初期化時に、GetPrivateProfileSectionNames で、マクロ名を一括取得しています。
    このマクロ名格納用バッファも初期化時に確保しており、そのサイズは CmdBar.ini に書いてあります。
    マクロが増えて、バッファサイズが足りなくなったら、CmdBar.iniを直接編集して、サイズを調整してください。
      例：Macro Name Buffer Size=256


  マクロ定義ファイルにサンプルとして DebugPluginと同じ機能のマクロを用意しました。
  参考にしてください。



















































































































































































戯言
あー、ソースが汚い。
思いつきで足していってるから、無駄な変数とかｲﾊﾟｰｲあるし、
元がそうだったから分割コンパイルとかしてるけど、グローバル変数バリバリ足しちゃって、もうメチャクチャ。
添削してやろうっていう奇特な方は、掲示板とかに書かずに、こっそり送ってくらはい。
