# 環境構築
1. git clone
2. cd rspec_dojo
3. bundle install --path vendor/bundle

# テスト実施方法
```sh
bundle exec rspec
```

# 問題
## 問題１
spec/user_spec.rb のTODO部分のテストを完成させてください

## 問題２
まず、User#helloを以下のように変更してください。
```ruby
class User
  def hello(name)
    "hello #{name}"
  end
end
```

引数に"world"を渡したときのテストを書いてください。

## 問題３
describe, context, it を使って、テストの意図を構造化して、仕様書のように書いてください

## 問題４
引数にnilが渡された場合は、 "ERROR: no one there" と返す機能追加とテスト追加をしてください

## 問題５
引数が"太郎"のときは、"こんにちは 太郎さん"と返す機能追加を、まずテストを書いてから行ってください

## 問題６（副作用のテスト）
まずUserを、このように変更してください。
```ruby
class User
  attr_accessor :name

  def initialize(name)
    @name = name
  end

  def hello(name)
    "hello #{name}"
  end
end
```

```ruby
User.new('Vincent')
```
という処理をしたときの戻り値がfalse, nilでないことと、副作用(オブジェクトの状態変化)のテストをしてください。

### 文法上のヒント１
expect(x).to be_truthy で、戻り値がtrueっぽい値であることを検証できます



