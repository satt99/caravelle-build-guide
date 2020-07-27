# Caravelle-BLE ビルドガイド
自作キーボードキット[Caravelle-BLE](https://satt.booth.pm/items/1644450)のビルドガイドです。  
組み立ての際は、本ビルドガイドの最後まで目を通した上で作業をはじめることを推奨します。

## 準備
最初に必要な部品および工具があることを確認します。
### 同梱品の確認
| ![parts](./img/parts/case.jpg) |  ![parts](./img/parts/plate.jpg) | ![parts](./img/parts/foam.jpg) | ![parts](./img/parts/foamcuthelper.jpg) |
| ---- | ---- | ---- | ---- |
| トップケース＋ボトムケース：左右1個ずつ | プレート：左右1枚ずつ |  消音フォーム：カット前 or カット済み 2枚 | フォームカットヘルパー：1枚 （フォームがカット済み場合は不要）|
| ![parts](./img/parts/mainpcb.jpg) | ![parts](./img/parts/screw.jpg) | ![parts](./img/parts/allenkey.jpg) | ![parts](./img/parts/insert.jpg) |
| 本体基板：左右1枚ずつ | M2×4mmねじ：18個 | 1.5mm六角レンチ：1個 | M2インサート：19個 |
| ![parts](./img/parts/insertpracticecube.jpg) |  ![parts](./img/parts/bumpon.jpg) | ![parts](./img/parts/tactileswitch.jpg) | ![parts](./img/parts/slideswitch.jpg) |
|インサート練習用ブロック：1個 | 滑り止め：8個 | タクトスイッチ：2個 （本体基板に取付済の場合もあり）| スライドスイッチ：2個 or 4個|
| ![parts](./img/parts/phconnector.jpg) |  ![parts](./img/parts/batterypcb.jpg) | ![parts](./img/parts/coincellholder.jpg) | ![parts](./img/parts/diode.jpg) |
| PHコネクタ：2個 | 電池用基板：2枚 | ボタン電池ホルダー：4個 | ショットキーバリアダイオード：4個 |
| ![parts](./img/parts/capacitor.jpg) | ![parts](./img/parts/phcable.jpg) |  |  |
| コンデンサ：2個 | PHコネクタ付きケーブル：2個 |  |  | 

### 追加で用意する部品
|部品|個数|
|---|---|
|ボタン電池(CR2032)|4個|
|MX互換スイッチ|48個|
|MX用キーキャップ|1u 42個、1.25u 4個、1.5u 2個|

### 工具
組み立てには電子工作に使用する工具が一通り必要です。下記のページなどを参考に工具を用意しましょう。
* [Helix キーボードキットの製作に必要な工具メモ | gist.github.com](https://gist.github.com/mtei/6957107a676ddfa85bde0ae41f8fa849)
* [第8回「自作キーボードのつくりかた #2」組み立てる道具とはんだ付け編 | Youtube](https://youtu.be/LOC53FeU-QM)
* [自作キーボードを作るために必要なもの | 自作キーボード温泉街の歩き方](https://salicylic-acid3.hatenablog.com/entry/2018/11/24/%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%E3%82%92%E4%BD%9C%E3%82%8B%E3%81%9F%E3%82%81%E3%81%AB%E5%BF%85%E8%A6%81%E3%81%AA%E3%82%82%E3%81%AE#%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%E3%81%A7%E5%BF%85%E8%A6%81%E3%81%AA%E3%82%82%E3%81%AE)
* [自作キーボードの組み立てに使っている工具 | yfuku blog](https://blog.yfuku.com/entry/keybord_build_tool)

なおインサートをケースに熱圧入する都合上、はんだごては温度調整機能がついているもの（HAKKO FX600等）が必須です。

## 組み立て
### 概要
次の順番でキットを組み立てていきます。
* 電池用基板を組み立てる
* 本体基板を組み立てる
* 本体基板の動作確認
* 本体基板にスイッチを取り付ける
* ケースを組み立てる

### 電池用基板に部品を組み立てる
はじめに電池用基板を組み立てます。注：基板のバージョン（基板左上に記載）によって部品の配置がやや異なります。

1. ボタン電池ホルダー×2 (BT1, BT2) を取り付ける

    | ![batterypcb](./img/batterypcb/coincellholder1.jpg) |  ![batterypcb](./img/batterypcb/coincellholder2.jpg) |
    | ---- | ---- |
    | ホルダーの片脚をペンチでまっすぐ伸ばします | 電池を入れる側（小さいでっぱりと反対側）が基板の角を向くようにホルダーの両脚を基板に挿します |
    | ![batterypcb](./img/batterypcb/coincellholder3.jpg) | ![batterypcb](./img/batterypcb/coincellholder4.jpg) |
    | まっすぐにした脚を再び折り曲げ、基板と平行にし、ホルダーの両脚を基板にはんだ付けします | もう片方のホルダーも同様の手順で取り付けます |

1. ダイオード×2 (D1, D2) を取り付ける

    | ![batterypcb](./img/batterypcb/diode1.jpg) | ![batterypcb](./img/batterypcb/diode2.jpg) | ![batterypcb](./img/batterypcb/diode3.jpg) | 
    | ---- | ---- | ---- |
    | 片側のパッドに予備はんだを盛ります | ダイオードの向きに注意しつつ、予備はんだをつけたパッドにダイオードをはんだ付けします（基板の逆`コ`の字型のシルクの縦線とダイオードの印字の縦線の向きを揃えます、シルクがかすれている場合は下の段の写真で向きを確認します） | もう片側のパッドもはんだ付けします |
    | ![batterypcb](./img/batterypcb/diodedirectionv11.jpg) | ![batterypcb](./img/batterypcb/diodedirectionv20.jpg) || 
    | V1.1基板 | V2.0基板以降 ||

1. コンデンサ (C1) を取り付ける
    * ダイオードと同様の手順でコンデンサを基板にはんだ付けします

1. (V2.0基板のみ)スライドスイッチ (SW1) を基板裏面に取り付ける
    * スライドスイッチの上下に注意します。スイッチの脚が付いている側が基板の下向きになるようにします
    * ずれやすいのでマスキングテープ等で固定した上ではんだづけします
    * 電源ON・OFFの方向については基板表面のシルクを参照

    | ![batterypcb](./img/batterypcb/slideswitch.jpg) |
    | ---- |
    | 写真のように基板裏面に実装します |

1. PHコネクタ付きケーブルを基板の左側のスルーホール (J1) に取り付ける

    | ![batterypcb](./img/batterypcb/cable1.jpg) |  ![batterypcb](./img/batterypcb/cable2.jpg) |
    | ---- | ---- |
    | 赤いケーブルの被覆が剥けた先端をVCC、黒いケーブルの被覆が剥けた先端をGNDと書かれた穴に通します。ケーブル先端を両方とも穴に通したら、穴からケーブルが抜けないように軽く曲げ、それぞれをはんだ付けします。注：ケーブルを通す穴が小さめなため、ケーブル先端には予備はんだを行わず、穴に通してからはんだ付けするようにしてください | ケーブルがショートしないように必要に応じて余分な配線を切ります |

1. ボタン電池を入れ、テスターで電圧を確認する

    | ![batterypcb](./img/batterypcb/tester.jpg) |
    | ---- |
    | 正しく組み立てられていれば、VCCとGNDの間で3Vほどが測定されます。（V2.0基板のみ）なお、V2.0基板ではスライドスイッチを電源ONの方向にスライドしておく必要があります。また、コンデンサに電荷が溜まっている間は電池基板の電源をOFFにしたとしてもVCCとGNDの間の電圧が3Vほどで保たれます。 |

1. 2個目の電池用基板も1個目と同様の手順で部品を取り付ける

    | ![batterypcb](./img/batterypcb/batterypcb.jpg) |
    | ---- |
    | 2個めの電池基板ではケーブルを1個目と逆の位置 (J2) に取り付けます |

### 本体基板を組み立てる
次に本体基板を組み立てます。

1. タクトスイッチ (SW3/SW4) を取り付ける
    * 電池基板のダイオードと同様の手順でタクトスイッチを基板にはんだ付けします
    * 一部個体では取付済の状態で出荷されています。その場合、この手順は不要です。

1. スライドスイッチ (SW1/SW2) を取り付ける
    * スライドスイッチの上下に注意します。スイッチの脚が付いている側が基板の下向きになるようにします
    * ずれやすいのでマスキングテープ等で固定した上ではんだづけします

    | ![mainpcb](./img/mainpcb/slideswitch.jpg) |
    | :----: |
    | スライドスイッチのはんだ付け |

1. PHコネクタ (J2/J4) を取り付ける
    * こちらもマスキングテープ等で固定した上ではんだづけします

1. もう片側の本体基板も同様に組み立てます

    | ![mainpcb](./img/mainpcb/mainpcb.jpg) |
    | :----: |
    | 本体基板組み立て完了後 |

### 本体基板の動作確認
スイッチを取り付ける前に本体基板が正しく動作することを確認し、マスタとスレーブ、マスタと端末をそれぞれペアリングします。なおキットでは、事前にデフォルトのファームウェアが書き込まれています。

| ![mainpcb](./img/mainpcb/pairing.png) |
| :----: |
| ペアリング模式図 |

1. スレーブ側（右手側）を起動する
    * 電池基板のケーブルをスレーブ側の本体基板のコネクタにはめます
    * スライドスイッチの端子をON側（右側）にスライドします
    * パソコン等の端末からBluetoothデバイスのスキャンを実行します
    * デバイス一覧に`Nordic UART`と表示されることを確認します
    * **`Nordic UART`の表示が確認できない場合**
        - 端末のBTアダプタによっては接続上の相性問題があるようです。その場合は別の端末でスキャンを実行してみてください。
        - マスタ-スレーブのペアリングが確立されていると、スレーブ側が`Nordic UART`としてアドバタイズされなくなります。[トラブルシュート](#ペアリングが出来ない・出来なくなった)を参考に一度スレーブ側のペアリング情報を削除し、再度Bluetoothデバイスのスキャンを実行してください
        - スレーブ側が正しく起動しているものの、端末によってはスキャン時に`Nordic UART`が表示されない場合があるようです。このような場合は`Nordic UART`の確認を飛ばし、マスタとスレーブのペアリングを行えばスレーブ側からの入力ができるか確認してみるといいです。
        - 電源が正しく供給されていることを確認します。電源ONの状態で基板裏面のプログラミングポートにテスターを当て、VCC-GND間が3V前後となっていれば正常に電源が供給されています。正常に電源が供給されていない場合は電池基板と本体基板のはんだづけが正しく行われていることを再度確認します。

    | ![mainpcb](./img/mainpcb/nordicuart.png) |
    | :----: |
    | スレーブ側動作確認 |

1. マスタ側（左手側）を起動する
    * スレーブ側と同様の手順でマスタ側を起動します
    * マスタとスレーブのペアリングが自動的に実行されます
    * 端末からBluetoothデバイスのスキャンを再度実行します
    * デバイス一覧から`Nordic UART`という表示が消え、代わりに`Caravelle-BLE`が表示されることを確認後、ペアリングを実行します（これ以降、スレーブ側のみを起動したとしても`Nordic UART`はデバイス一覧に表示されません）
    * マスタ側が起動しない場合は、電源が正しく供給されていることを確認します。電源ONの状態で基板裏面のプログラミングポートにテスターを当て、VCC-GND間が3V前後となっていれば正常に電源が供給されています。正常に電源が供給されていない場合は電池基板と本体基板のはんだづけが正しく行われていることを再度確認します。
    * 接続時にドライバエラーが発生する、接続済み・ペアリング済みが交互に発生し入力ができない場合は、[トラブルシュート](#ドライバエラーが発生する、接続済み・ペアリング済みが交互に発生し入力ができない)を参考に一度ペアリング情報を削除してください

    | ![mainpcb](./img/mainpcb/caravelleble.png) |
    | :----: |
    | マスタ側動作確認 |

1. 入力テストを行う
    * ピンセット等で各キーのスルーホールをショートさせ、文字が入力されることを確認します
    * [EK Switch Hitter](https://www.majorgeeks.com/files/details/switch_hitter.html)や[KeyboardTester.com](https://www.keyboardtester.com/)を使用するとどのキーが押されたか簡単に確認できます
    * デフォルトのキーマップについては[こちら](#キーマップ)を確認してください。US配列のキーマップである点や、`LOWER`・`ADJUST`のレイヤー変更キー等の単独では入力がされないキーがある点、スマートフォンなどでは正しく入力されないキーコードもある点に注意

1. DFUボタンの動作確認を行う
    * 一度マスタ、スレーブの両方の電源を切ります
    * タクトスイッチを押しながらスライドスイッチを操作してマスタ側を起動します
    * 端末からBluetoothデバイスのスキャンを実行し、`DFU Targ`（DFUモードで起動したキーボード）が表示されることを確認します
    * タクトスイッチを押しながら起動してもDFUモードに突入しない場合は、タクトスイッチのはんだづけが正しく行われていることを再度確認します
    * スレーブ側も同様にDFUボタンの動作確認をします

### 本体基板にスイッチを取り付ける

動作確認が完了したら本体基板にスイッチを取り付けます。

1. スイッチをプレートにはめる

1. スイッチをはめたプレートを本体基板にはめる
    * 本体基板にスイッチをはめる際にピンが折れないように注意します
    * スライドスイッチのスライド部分がプレートの切り込みに合っていることを確認します。スライド部分が干渉してプレートが上手くはまらない場合は、スライドスイッチのはんだ付けを修正します

1. スイッチをはんだ付けする

    | ![mainpcb](./img/mainpcb/keyswitch.jpg) |
    | :----: |
    | スイッチ取り付け後 |

### ケースを組み立てる

最後にケースを組み立てます。

1. ケースにインサートを熱圧入する
    * ケースの素材は60度ほどで軟化、200度ほどで融解するため、温度調整が可能なはんだごてを使用して作業する必要があります
    * 最初に練習用ブロックを使用してインサートの熱圧入の練習をします
    * はんだごての温度を230度ほどに設定します。こて先にはんだが付いている場合はクリーナーで軽く除去します
    * ピンセットでインサートを穴の上にのせ、軽い力ではんだごてを当て、インサートの温度上昇に合わせてゆっくりとインサートを穴に押し込みます（注：無理に力を入れて押し込むと、穴が崩れたり、インサートが傾いて挿入されることがあります）
    * 一回で最後まで押し込むのではなくインサートの位置を確認しつつ何度かに分けて押し込んでいくと失敗しにくいです（押し込み量が足りない場合は修正が簡単ですが、押し込みすぎた場合は修正が比較的大変なため）
    * インサートのフランジと穴周辺との段差がなくなるまで押し込んだら熱圧入完了です
    * トップケース（片側8箇所）、ボトムケース（片側1箇所）にインサートを熱圧入します。ケースに熱圧入する際ははんだごてが周囲の部分に誤ってぶつかり溶かさないように注意します

    | ![case](./img/case/heatinsert1.jpg) |  ![case](./img/case/heatinsert2.jpg) |
    | :----: | :----: |
    | インサート熱圧入 | インサート押し込み量の目安 |
    | ![case](./img/case/topcase.jpg) | ![case](./img/case/bottomcase.jpg) |
    | インサートを熱圧入したトップケース | インサートを熱圧入したボトムケース |

1. 消音フォームを切り出す
    * 出荷時に消音フォームがカット済みの個体ではこの手順は不要です。
    * フォームカットヘルパーの外周にそって消音フォームを2枚切り出します
    * 柔らかい素材のため、カッターで罫書き線を入れ、ハサミで切り出すという方式が簡単です

    | ![case](./img/case/foam.jpg) |
    | :----: |
    | 切り出した消音フォーム |

1. トップケースにプレートを取り付ける
    * 電池基板のケーブルが本体基板に取り付けられていることを確認します
    * プレートをトップケースに載せ、六角レンチを使用してねじでとめます（片側4箇所）（注：無理に力を入れてねじを回すとインサートが外れてしまうことがあるため、軽い抵抗を感じる時点でねじを回すのを止めましょう）

1. ボトムケースに電池基板を取り付ける
    * 電池基板をボトムケースに載せ、六角レンチを使用してねじでとめます（片側1箇所）

    | ![case](./img/case/screwplate.jpg) |
    | :----: |
    | プレート＋電池基板ねじ止め後 |

1. トップケースにボトムケースを取り付ける
    * 溝に沿ってケーブルをはわせた上で、ボトムケースに消音フォームをのせる（注：消音フォームはスイッチピンとボタン電池の絶縁材を兼ねているので、忘れずにいれてください）
    * ケーブルと消音フォームの位置がずれないように注意しつつ、ボトムケースにトップケースをはめ、六角レンチを使用してねじでとめます（片側4箇所）

    | ![case](./img/case/casewithfoam.jpg) |
    | :----: |
    | 消音フォームを忘れずに挟む |

1. ボトムケース底面の円形の切り欠きに合わせて滑り止めを貼る

1. キーキャップを取り付ける
    
    | ![case](./img/case/complete.jpg) |
    | :----: |
    | 組み立て完了です！ | 

1. 必要に応じてファームウェアを更新し、キーマップの変更や、[通信間隔の調整](#入力遅延が気になる)を行う
    * 通信環境や入力速度は人によって大きく異なるため、自分に合わせて通信間隔の調整を行うことをおすすめします

## ファームウェア書き込み
BLEに対応するため、ファームウェアにはSekigon氏の[nrf52対応のqmk_firmware](https://github.com/sekigon-gonnoc/qmk_firmware/tree/nrf52)を使用します。

1. リポジトリを取得する  
  nrf52対応のqmk_firmwareは[こちら](https://github.com/sekigon-gonnoc/qmk_firmware/tree/nrf52)

	* 既にqmk_firmwareを使っていて別のブランチとして用意したい場合
	```
        git remote add sekigon https://github.com/sekigon-gonnoc/qmk_firmware.git
        git fetch sekigon
        git checkout -b nrf52 sekigon/nrf52
	```
	
	* 既にqmk_firmwareを使っていて別のフォルダに置きたい場合
	  
	 ```
		git clone  -b nrf52 https://github.com/sekigon-gonnoc/qmk_firmware.git ble_micro_pro
	 ```
	  
	* 初めて使う場合
	
	```
        git clone --depth 1 -b nrf52 https://github.com/sekigon-gonnoc/qmk_firmware.git
	```

1. 必要なサブモジュールを用意

		make git-submodule

1. [NRFSDK v12.3.0](https://www.nordicsemi.com/Software-and-Tools/Software/nRF5-SDK/Download)を取得し、適当なディレクトリに展開する

	* 技適の関係上、バージョン番号は厳守してください。

1. 展開したディレクトリをmsys2などビルド環境の環境変数に設定する

    ```
    export NRFSDK12_ROOT=<path to sdk> #例 /c/dev/nRF5_SDK_12.3.0_d7731ad
    ```    
    
### nrfutilのセットアップ(Windows(MSYS2))
[nrfutil.exe](https://github.com/NordicSemiconductor/pc-nrfutil/releases)をダウンロードし、~/qmk_utilに保存します。

### nrfutilのセットアップ(Mac, Linux)
pipでnrfutilを入れます。(python2.7)

```
pip install nrfutil
```

### 本体へのファームウェア書き込み
#### ブートローダを使用した書き込み（推奨）
Caravelle BLEにはブートローダが事前に書き込んであるため、無線通信によるファームウェアアップデートが可能です。

1. スマートフォン・タブレットに[nRF Toolbox](https://apps.apple.com/jp/app/nrf-toolbox/id820906058)をインストール

1. マスタ(左手側）、スレーブ(右手側)それぞれのファームウェアをビルドする

    ```
    make caravelle_ble/master:default:dfu_ble
    make caravelle_ble/slave:default:dfu_ble
    ```
    * `qmk_firmware`直下に、`caravelle_ble_master_default.zip`と`caravelle_ble_slave_default.zip`という2つのzipファイルが生成されます

    | ![case](./img/firmware/buildfirmware.png) |
    | :----: |
    | デバッグモードでビルドするため、上記画像のような警告が出ますが問題ありません。（ファームウェア更新時のバージョン番号チェックを避けるためデバッグモードが必要となります。） | 

1. 生成された2つのzipファイルを共有フォルダやメールを使用してスマートフォンに移動し、nRF Toolboxにコピーする
    * iphoneを使用する自分は、「生成されたzipファイルをdropboxにコピー」→「iphoneのdropboxアプリからzipファイルを選択」→「`エクスポート`を選択」→「`nRF Toolboxにコピー`を選択」という手順で行っています
    * 共有フォルダの代わりに、「自分宛てにzipファイルを添付したメールを送信」→「スマートフォンで受信したメールのzipファイルを選択」という風にメールを使用することもできます

1. nRF Toolboxを起動し、DFUを選択

1. `SELECT FILE`から先ほど用意したzipファイルを選択

1. 書き込みたい基板の電源をタクトスイッチを押しながら入れ、DFUモードに突入する

1. `SELECT DEVICE`で`DFU Targ`を選択

1. `UPLOAD`を押し、ファームウェアを書き込み
    * 注：書き込みが完了するまでスマートフォンと基盤の電源はOFFにしないこと
    * 書き込み完了後、一旦電源をOFFにし、再度ONにすると、`Caravelle-BLE`あるいは`Nordic UART`として自動的にアドバタイズがはじまります。（注：
    接続済みの端末がある場合はアドバタイズは開始されません。）
    * まれに書き込み完了も`DFU Targ`と表示されつづけ、キーボードとしてのアプリケーションが起動しない場合があります。その場合、手順6から順に再びファームウェアの書き込みを行ってください。
    * 電池残量が少ないと`DEVICE FIRMWARE UPDATE`開始直後にエラーが発生することがあります。その場合、電池を交換し再度ファームウェアの書き込みを行ってください

| ![firmware](./img/firmware/copyzip.jpg) |  ![firmware](./img/firmware/selectdevice.jpg) | ![firmware](./img/firmware/nrftoolbox.jpg) |
| ---- | ---- | ---- |
| nRF Toolboxにコピー | SELECT DEVICEで`DFU Targ`を選択 | UPLOADを押し、書き込みを開始 |

#### SWDを使用した書き込み（初期化・ブートローダ再書き込み）
OpenOCD(0.10.0)とST-Link V2を使用して書き込みます。  (CMSIS-DAPでも可能なようですが、作者は未確認です。)
* ST-Link V2は、aliexpressやamazonで安価なクローン品を購入することができます
* MSYS2でのOpenOCD(0.10.0)のインストールは[こちらのサイト](https://kunsen.net/2018/09/30/post-1749/)が参考になります
* WindowsでST-Link V2を使用するためには、ST-Link V2のファームウェアのアップデートが必要となる場合があります。[こちらのサイト](https://kunsen.net/2018/09/30/post-1773/)が参考になります。

1. 本体基板のスライドスイッチを電源OFF側にし、電池基板と本体基板の接続を解除する

1. ST-Linkの`3.3V GND SWDIO SWDCLK`を基板の`VCC GND SWDIO SWDCLK`に接続する（基板裏面のシルクを参照）

1. MCUを初期化し、ソフトデバイスを書き込む
    ```
    openocd -s /mingw64/share/openocd/scripts -f interface/stlink.cfg -f target/nrf52.cfg -c init -c "reset init" -c halt -c "nrf5 mass_erase" -c "program s132_nrf52_3.0.0_softdevice.hex verify" -c reset -c exit
    ```
    * ソフトデバイスは[ファームウェア書き込み](#ファームウェア書き込み)においてダウンロードした、`NRFSDK v12.3.0`の中の`nRF5_SDK_12.3.0_d7731ad/components/softdevice/s132/hex`に保存されています
    * CMSIS-DAPを使用する場合は、`interface/stlink.cfg`を`interface/cmsis-dap.cfg`に変更します（次の手順でも同様）

1. 本リポジトリの[リリース](https://github.com/satt99/caravelle-build-guide/releases)からブートローダ（`caravelle_ble-bootloader.hex`）をダウンロードし書き込む
    ```
    openocd -f interface/stlink.cfg -f target/nrf52.cfg -c "program caravelle_ble-bootloader.hex verify" -c "reset" -c exit
    ```

1. 正しくブートローダが書き込めていれば、キーボードを起動し、端末からBluetoothデバイスのスキャンを実行すると`DFU Targ`と表示されます。この状態ではキーボードとしてのファームウェアが書き込まれていないので、[前項](#ブートローダを使用した書き込み（推奨）)を参考に無線通信でファームウェアを書き込みます。

| ![firmware](./img/firmware/openocd1.png) |  ![firmware](./img/firmware/openocd2.png) | ![firmware](./img/firmware/openocd3.png) |
| ---- | ---- | ---- |
| ソフトデバイスを書き込み | ブートローダ書き込み | ST-Linkを正しく接続できていないとこのようなエラーが発生します |

# キーマップ

Caravelleのデフォルトのキーマップはリンク先の[keymap.c](https://github.com/sekigon-gonnoc/qmk_firmware/blob/nrf52/keyboards/caravelle_ble/keymaps/default/keymap.c)にて定義されています。以下はそれを画像にしたものです。

| ![firmware](./img/keymap/caravelle-default2.png) |  
| ---- |
| デフォルトキーマップ。黒文字：Baseレイヤー、青文字：Lowerレイヤー、赤文字：Raiseレイヤー、緑文字：Adjustレイヤー（次画像参照）。Home、End、PageUp、PageDown、Escは2020/07/27に追加しました。それ以前に出荷したものでは定義されていないので注意。| 

| ![firmware](./img/keymap/caravelle-default-adjust.png) |  
| ---- |
| Adjustレイヤー。設定関連のマクロが定義されています。 |

|マクロ|定義|
|---|---|
|AD_WO_L| マスタと新たな端末とのペアリングを開始（他の端末の無線を一旦OFFにし接続を解除してから新たなペアリングを開始してください）|
|ADV_IDX| マスタをX番目にペアリングした端末と接続（AD_WO_Lでペアリングしたものから順にID1、ID2…となります）|
|DELBNDS| マスタに保存されたペアリング情報をすべて削除|
|DEL_IDX| マスタに保存されたX番目のペアリング情報を削除|
|BATT_LV| マスタ側の電池の電圧を表示（例：`2998mV`）|
|ENT_SLP| スリープモードに突入|
|ENT_DFU| DFUモードに突入|
|RESET| マスタを再起動|

## トラブルシューティング
### ペアリングが出来ない・出来なくなった
端末、マスタ、スレーブのペアリング情報を削除してから再ペアリングを実行してみてください。
 - マスタに記録されたペアリング情報を削除する
    - 最上段の中心3つのキー（デフォルトの配列では`WER`に相当）を押しながら電源をONにすることで端末、スレーブとのすべてのペアリング情報を削除できます
    - `DELBNDS`キーコードでも全てのペアリング情報を削除できます
    - 特定の端末とのペアリング情報を削除するには、`DEL_IDx`(`x`はその端末のペアリング番号)をキーマップに割り当てて実行してください
 - スレーブに記録されたペアリング情報を削除する
    - 最上段の中心3つのキー（デフォルトの配列では`UIO`に相当）を押しながら電源をONにする
 - 端末に記録されたペアリング情報を削除する
    - Bluetoothの設定画面からCaravelle-BLEのペアリングを解除してください（例: Windows10なら「Bluetoothとその他デバイス」から「Caravelle-BLE」を選択し「デバイスの削除」）

それでも症状が改善しない場合は、[無線通信でのファームウェア更新](#ブートローダを使用した書き込み（推奨）)、[MCUの初期化](#SWDを使用した書き込み（初期化・ブートローダ再書き込み）)を順に試してみてください。

### [Windows] ドライバエラーが発生する、接続済み・ペアリング済みが交互に発生し入力ができない
端末-マスタの片側のペアリング情報のみを削除し、もう片側に古いペアリング情報が残ったまま、端末-マスタを新しくペアリングすると表題の問題が発生するようです。[ペアリングが出来ない・出来なくなった](#ブートローダを使用した書き込み（推奨）)を参考にペアリング情報をすべて削除した上で再度ペアリングを行うと解決されます。

| ![troubleshoot](./img/troubleshoot/drivererror.png) |
| :----: |
| ドライバエラー | 

### 入力遅延が気になる
- 入力遅延が気になる場合は、`caravelle_ble/config.h`内の下記のパラメタを編集します。
- 接続先の省電力設定も確認してください

|パラメータ|定義|
|---|---|
|BLE_NUS_MIN_INTERVAL| 左右間の通信間隔の最小値(ms)　下げるとマスタとスレーブ間の遅延が減るものの、消費電力が増える。デフォルトは20 (2020/07/27以前は30)|
|BLE_NUS_MAX_INTERVAL| 左右間の通信間隔の最大値(ms)　下げるとマスタとスレーブ間の遅延が減るものの、消費電力が増える。デフォルトは50 (2020/07/27以前は30)|
|BLE_HID_MAX_INTERVAL| 端末との通信間隔の最大値(ms)　下げると端末とマスタ間の遅延が減るものの、消費電力が増える。デフォルトは60 (2020/07/27以前は90)|
|BLE_HID_SLAVE_LATENCY| 端末との通信パラメータ　下げると通信頻度が増えるが、消費電力が増える。HID_INTERVALに反比例させると良い？　デフォルトは3 (2020/07/27以前は4)|

### チャタリングが気になる
`config.h`の`DEBOUNCE`の値を調整してください

## 使用上の注意
- 電源を常時付けたままでも3ヶ月以上は電池が持つ試算ですが（使用環境や条件によって変化します）、長時間使用しない場合は電池の消耗を防ぐため、電源を切ってください。また、持ち運び時にキーが押下状態のままになると電波を発信しつづけて電池が消耗するため、持ち運びの場合も電源を切った状態にしてください。
- 正常な動作中に電池が発熱することはありません。発熱を感じた場合はただちに使用を中止してください

## 参考文献
本ビルドガイドは下記を参考に執筆しました。
- nrtkbb氏 [uzu42ビルドガイド](https://github.com/nrtkbb/Keyboards/blob/master/uzu42/build_guide_jp.md)
- Sekigon氏 [SISO59ビルドガイド](https://github.com/sekigon-gonnoc/SISO59-doc/blob/master/README.md)、[BLE-Micro-Proドキュメント](https://github.com/sekigon-gonnoc/BLE-Micro-Pro/blob/master/README.md)  
- yfuku氏 [Claw44ビルドガイド](https://blog.yfuku.com/entry/craw44_buildguide)
