# k8s_operator_test
## 概要
書籍「実践入門 Kubernetesカスタムコントローラーへの道」を見ながら作成したKubernetesのOperatorのサンプルです。Kubebuilder3.2.0を使用しました。

## テスト方法
- kubectl用の設定ファイル(admin.conf)をプロジェクトのルートにコピー
- Visual Studio Codeでリモートコンテナとしてプロジェクトを開く
- `cd mycontroller`
- `make install`でCRDをKubernetesクラスタに登録
- `kubectl apply -f sample/foo.yml`でFooリソースを登録
- `make run`でOperator起動
