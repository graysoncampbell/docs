---

copyright:
  years: 2016
lastupdated: "2016-10-26"

---


{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}


# サービスの動作
{{site.data.keyword.iotinsurance_full}} は、接続されている保険契約者からデータを収集、管理、分析するためのフローを作成します。
{:shortdesc}

保険会社は、{{site.data.keyword.Bluemix_notm}} 組織内に {{site.data.keyword.iotinsurance_short}} のインスタンスを作成します。保険会社の顧客の住宅には、センサー提供会社のクラウドに接続されたセンサーが配置されています。顧客はモバイル・デバイスから、{{site.data.keyword.iotinsurance_short}} サービスに対し、センサー・データの受信を許可します。{{site.data.keyword.iotinsurance_short}} 変換プログラムは、センサー提供会社のクラウドに接続し、各ユーザーのデータをプルし、{{site.data.keyword.iot_short_notm}} サーバーに送信します。顧客の住宅のセンサーで、保険会社のシールドに指定された条件を満たしたことが示されると、保険会社のダッシュボードと顧客のデバイスに通知が送信されます。

接続されているセンサーが、水漏れなどのイベントを検出し、その情報を Wink などのスマート・ホーム・ベンダーに送信します。{{site.data.keyword.iotinsurance_short}} は、スマート・ホーム・ベンダーのクラウドとの接続を使用してシグナルを検出し、アラート・ペイロードを作成します。そのペイロードは、MQTT により {{site.data.keyword.iotinsurance_short}} シールド・エンジンに送信されて、処理されることになります。シールド・エンジンは、そのペイロードが、シールド・ルールによって定義されている基準に一致するかどうかを分析します。一致している場合、シールド・エンジンは MQTT によりハザード・ペイロードを {{site.data.keyword.iotinsurance_short}} アクション・エンジンに対して発信します。アクション・エンジンは、テキスト・メッセージを住宅所有者に送信するなど、そのタイプのハザード (危険) についてシールドで定義されているアクションを実行します。

{{site.data.keyword.iotinsurance_short}} は、コンポーネント間でアラート・ペイロードやハザード・ペイロードを渡す上で、{{site.data.keyword.iot_full}} に依存しています。完全に動作するシステムでは、ユーザーとシールドに加えてユーザーとシールドの間の関連付けが必要です。

![{{site.data.keyword.iotinsurance_short}} プロセス。この図については、トピックのメイン本体で説明されています。](images/IoT4I_process.svg "{{site.data.keyword.iotinsurance_short}} プロセス")

# 関連リンク
{: #rellinks}

## チュートリアルとサンプル
{: #samples}
* [GitHub のサンプル・モバイル・アプリ・コード](https://github.com/ibm-watson-iot/ioti-mobile){:new_window}

## API リファレンス
{: #api}
* [{{site.data.keyword.iotinsurance_short}} API](https://iot4i-api-docs.mybluemix.net/){:new_window}
* [{{site.data.keyword.iotinsurance_short}} API サンプル](https://github.com/IBM-Bluemix/iot4i-api-examples-nodejs/#iot-for-insurance-api-examples){:new_window}

## 関連リンク
{: #general}
* [{{site.data.keyword.iot_full}} 資料](https://console.ng.bluemix.net/docs/services/IoT/index.html)
* [開発者サポート・フォーラム](https://developer.ibm.com/answers/search.html?f=&type=question&redirect=search%2Fsearch&sort=relevance&q=%2B[iot]%20%2B[bluemix])
* [Stack overflow サポート・フォーラム](http://stackoverflow.com/questions/tagged/ibm-bluemix)
