# product_management_repository
プロダクト管理の勉強用リポジトリ



# ルール
## ブランチのルール
- release: 難読化対応したリリース用
- source_code_god: 神様
- develop:　開発用のメインブランチ（ここ自体は編集不可）maintenance?
  - develop-xxxxxxxx: 作業ブランチ。ここをメインに編集し、終了次第`develop`ブランチにプッシュ
    xxxxxxxxはわかりやすいように任意に指定。例、develop-fix_rdma_server
    ここは各作業者が自由に作業できることとする。基本的にこの階層のみで大丈夫と思う。  
    大規模な改修が起こった場合はここを起点とし、ブランチを新たに作成して管理していくことも考える。  


## リリース/タグルール
リリースできるのは、`release`ブラインチのみ。
リリース後は「Action」を確認し、エラーが出ていないか確認を行う。（GithubActionにより、リリースを行った際にreleaseブランチかどうか判定を行っている。）  
他のブランチをリリースしようとすると、エラーは発出されるので、速やかにリリースとタグの削除を行う。

タグの命名規則
（例）1.0.0.xxxx

a.b.c.d
a: メジャーアップデート（年度跨ぎ（デフォルトキーを更新することとする？） or 暗号化機能など新規機能が追加された場合。）  
b: 仕様変更  （各機能のI/F変更など。）
c: バグ修正  （リリース先でバグが見つかった場合など。）
d: optional, リリース先ごと特殊な対応をした場合など。 （グループ企業以外のリリース時のミニマム化？サンプルの提供なども？） 

なお、マニュアルについても、ソースコードのバージョンと対応させることとし、変更がなくともともにアップデートしていくこととする。


# リリースノート

|    | バージョン          |     概要            |    リリース日     |            備考                       |
|----|--------------------|---------------------|------------------|--------------------------------------|
|    |    1.0.0           |   初回リリース       |    2025/2/1      |                                      |
|    |    1.0.1           |   バグ修正           |    2025/4/1      |                                      |
| ✔ |    1.0.2.b         |   ～機能PoC対応       |    2025/2/1      |           b社、個別対応               |




# リリース状況
|             |     A社             |   B社               |   C社               |   D社                |   E社               |   TBD               |
|-------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|
|   1.0.0     |    ✔ (2025/2/1)    |    ✔ (2025/2/1)     |   ✔ (2025/2/1)     |    ✔ (2025/2/1)     |    ✔ (2025/2/1)    |                      | 
|   1.0.1     |                     |                     |                    |    ✔ (2025/3/1)     |                     |                      | 
|   1.0.2.b   |                     |    ✔ (2025/4/1)    |                     |                     |                      |                     | 

