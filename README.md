# /go/ 中間リンク一式(LINE導線統一+経路計測)

## 仕組み
各SNS → /go/チャネル名 → GA4に経路を記録(0.4秒) → lin.ee/9Ylp1WG へ自動転送
lin.eeを直接貼らないことで、①経路計測 ②転送先の一括変更 が可能になる。

## 設置手順
1. GitHub Pages(またはenlife7.comサーバー)にこの go/ フォルダごとアップロード
2. 全ファイル内の「G-XXXXXXXXXX」をGA4測定IDに一括置換(2箇所×7ファイル)
3. 各SNSのプロフィールリンクを差し替え:
   - Instagram → https://ドメイン/go/ig/
   - TikTok → https://ドメイン/go/tt/
   - YouTube概要欄 → https://ドメイン/go/yt/
   - Facebook(CTAボタンも「登録する」に変更) → https://ドメイン/go/fb/
   - 催事ブースQR(QR再発行) → https://ドメイン/go/booth/
   - 名刺・チラシ → https://ドメイン/go/card/
   - 動画キャプション・固定コメント → https://ドメイン/go/mv/
4. GA4で「line_redirect」イベント+channelパラメータを探索レポートに登録
   → data/LP集計マスター.xlsx「UTM別」シートにPower Automateで週次転記

## 運用ルール
- LINEの入口URLは lin.ee/9Ylp1WG を「正」とし、これ以上発行しない
- 転送先を変えたい時は7ファイルのURL1行を書き換えるだけ(SNS側は触らない)
- 旧URL(JazkvAI/SO0ziwe)も同一アカウントに生きているため貼り替え漏れは機能停止しない
