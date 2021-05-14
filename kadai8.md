@startuml
opt 未登録
ユーザー -> webサーバー : ユーザー登録
webサーバー -> DBサーバー : ユーザー登録
DBサーバー -> DBサーバー : 登録処理
DBサーバー -> webサーバー : 登録結果

alt 登録成功
webサーバー -> ユーザー登録:メッセージを表示
else 登録失敗
webサーバー -> ユーザー失敗:メッセージを表示

end
end

@enduml
