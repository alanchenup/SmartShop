# README

它开发的初衷是能在 **微信** **百度轻应用** **UC平台** 上简单的搭建搭建一款单用户商城。

你可以自由的更改代码本地跑着玩，但因为所使用的 theme 是购买的，如果部署供人使用你可能会因为这个问题侵权哦。

## Ruby version

* ruby >= 2.0.0-p0
* rails >= 4.0.2

## System dependencies

## 关键文件配置

```ruby
touch config/initializers/secrets.yml
rake secret
then config your `secret_key_base`
```

因为 rails 4.1 仍在 beta 版本，所以你还需要添加如下文件

```ruby
touch config/initializers/secret_token.rb
rake secret
SmartShop::Application.config.secret_key_base = 'YOUR KEY'
```

## 数据库创建和初始化

先配置 ```config/database.yml```

```ruby
rake db:rebuild
```
### 配置开发习惯文件

此文件不纳入版本控制

```ruby
touch /config/initializers/dev_config.rb
then edit it...

# example:
# Read: http://guides.rubyonrails.org/generators.html#customizing-your-workflow
SmartShop::Application.config.generators do |g|
  g.test_framework  false
  g.stylesheets     false
  # g.javascripts     false
  # g.helpers         false
end
```
