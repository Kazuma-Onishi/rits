# 各launch ファイルの動作
基本的にhogehoge.launchはhogehogeというノードがhogehoge.yamlをロードして起動するようになっています。

その他のlaunchファイルは実験やデモの際にまとめてlaunchするためのファイルになっています。

まとめてlaunchするものは実験の際に必要なものを適当に作っていたのと、今使ってないファイルが参照されていたりするので一回全部消してリセットしてしまってもいいかもしれません
## 単体でノードを立ち上げるためのlaunchファイル
- connect_carrier
- control_gear
- control_roll (不要?)
- control_signal
- control_signal2
- control_steer
- control_steer2
- control_tray
- gnss
- imu
- information
- manage_mode
- path
## 複数のノードを同時に立ち上げるlaunchファイル(自分が実際に使ったもの)
- demo_docking
- essential.launch
- fordocking.launch

# 備考
control_signalは制御に用いるPLCやマイコン、操舵装置との通信用のノードでcontrol_signal2は今年追加された自動選別・収納機能のマイコンと通信するノード。収納機能は自動走行には関係ないので同時進行で行うために別ファイルで作成。マイコンがPLCに置き換わったりしなければ独立したノードとして運用したい。

control_steer2はcontrol_steerが機能の拡張を繰り返してめちゃくちゃ汚くなってしまったので新たに書きなおしたノード。モードの切り替えなど軽く確認したが、

