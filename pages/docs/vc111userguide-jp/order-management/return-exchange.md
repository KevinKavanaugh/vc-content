---
title: 返品 / 交
description: 返品 / 交換
layout: docs
date: 2016-06-03T10:21:23.333Z
priority: 3
---
## はじめに

お客様に商品を発送することは大変重要な意味があります。お客様が再度購入してくれるかどうかを決定します。オンラインシュップは、商品購入後の経験に焦点をあて、ユーザーエクスペリエンスが満足できるレベルでサービス・品質を保つことが最も重要な部分です。コマースマネージャーは、**Order** モジュールから返品を実行することができ、返品が **Fulfillment**　モジュールで処理されます。

ユーザーは、返品・交換を行う為に適切な権限を持っている必要があります。システムは、自動的に取引の為の返品承認(RMA)コードと呼ばれる固有のコードを作成します。一般的に、RMA番号がお客様口座への支払の受信をマッチさせるフルフィルメントセンター従業員を支援するための物理的な返品を記録します。

## 返品の作成

返品を作成するには、適切な権限を持っていなけらばなりません。そして注文のステータスは、**Completed** になっていなければなりません。次の手順で処理を行います。

1. **Orders** モジュールを開き、注文リストから注文を選択します。
2. **Summary** タブの Create return ボタンをクリックします。
3. ウィザードのステップ２が表示されます。注文リストのアイテムは、数量を持つアイテムを含んでいます。返品リストのアイテムは、返品商品を含んでいます。
  <img src="../../../assets/images/docs/image2013-6-3 17_38_41.png" />
4. リストからアイテムを選択し、
  <img src="../../../assets/images/docs/image2013-6-3 17_45_54.png" />
  ボタンをクリックします。Tip: 別の方法として、アイテムのダブルクリックでもできます。
5. "Specify return data" ダイアログが表示されます。
  <img src="../../../assets/images/docs/image2013-6-3 17_53_56.png" />
6. **Return quantity and Reason** を入力し、**OK** ボタンをクリックします。
7. 新しいレコードが、**Items to return** リストに追加されます。(更新が必要な数１). 数量とアイテム名・返品理由が表示されます。また、リストの下の "Return summary" が更新されます。
  <img src="../../../assets/images/docs/image2013-6-3 18_5_23.png" />
8. 必要があれば、Customer comment を入力します。
9. Next をクリックします。 Adjust Return processing details が表示されます。
  <img src="../../../assets/images/docs/image2013-6-3 18_11_51.png" />
10. 総払い戻し金額は、前のステップから引き継がれます。返品が払い戻し前に必要かどうか指定することができます。このオプションは、デフォルトではオフになっています。
11. Finish ボタンをクリックします。新しく作成されたRMAが自動的にDBに保存され、返品/払い戻しタブがアクティブになります。

## 返品のキャンセル

返品が完了した状態になっていない場合、返品をキャンセルすることができます。キャンセルは、以下の手順になります。

1. Return / Exchange タブのキャンセルするRMA リクエストを選択します。
2. 選択したRMAリクエストからキャンセルボタンをクリックします。ステータスがキャンセルに設定されます。

## 返品の完了

スタータスが、AwaitingCompletion の場合は、RMAリクエスト処理を完了することができます。完了の手順は、以下の通りです。

1. Return / Exchange タブからRMA リクエスト完了を選択します。
2. MAリクエスト選択後、 Complete ボタンをクリックします。払い戻しが必要な場合は、Create Refund for RMA Requestウィザードが表示されます。これは、支払数量項目に RMA リクエスト合計欄に払い戻し金額が設定されている場合、ウィザードが起動されます。
  <img src="../../../assets/images/docs/image2013-6-4 13_51_23.png" />
3. 返金を完了するために払い戻しの指示に従ってください。
4. 払い戻し成功後、
  - RMAリクエストステータスが完了に設定されている。
  - 変更内容が保存されている。
  - 注文支払リストが更新されている。

## 注文の交換作成

交換注文を作成するには、適切な権限を持っている必要があります。注文のステータスが、AwaitingStockReturn 又はAwaitingCompletionの状態である必要があります。交換注文を作成する手順は、以下の通りです。

1. Return / Exchange タブの交換を作成するRMAリクエストを選択します。
2. 選択したRMAリクエストでCreate Exchange Orderボタンをクリックします。
3. ２ステップのCreate an exchange Order ウィザードが表示します。ウィザードの最初のステップは、購入した商品を選択、カタログ選択、検索キーワードを入力、カートに追加します。利用可能な商品は、購入された商品が含まれています。カートのリスト内の項目は、ショッピングカートの項目が含まれています。
  <img src="../../../assets/images/docs/image2013-6-4 18_30_57.png" />