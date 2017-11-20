#form_for이용하기

###가상머신 구동
~~~shell
######윈도우 환경#####
git bash
cd ~/project
vagrant up
vagran ssh
#가상머신 구동됨
[Vagrant] cd ~/vagrant #윈도우의 ~/project
#여기서 부터 시작
rails new 어쩌고 --skip-bundle
atom .


#####새로운 vagrant#####
git bash
mkdir project2
vagrant init ubuntu/xenial64 => Vagrantfile(설정 해줌 ex. prot설정)
vagrant up
vagran ssh
#가상머신 구동됨
[윈도우즈] cd ~/vagrant #윈도우의 ~/project
atom .
~~~

~~~shell
rails new form_for --skip-bundle
#gemfile 수정후
bundle install
rails g scaffold blog title content image_url is_active:boolean
# rails d scaffold blog 잘못 만든 경우엔...
rails g controller posts index new create show edit update destroy

rails g controller tweets index new create show edit update destroy
resources : tweets
rails g model tweet title content
model tweet
  title
  content
new -> create
~~~

~~~shell
rails g devise:install
rails d scaffold blog
rails d controller posts
rails d model post
rake db:drop
rake db:migrate
rake db:seed
rails g devise user
rake db:migrate
~~~

~~~ruby
#:..=> 이거랑 ..:이거는 같은 의미이다.
phone_book = Hash.new
phone_book = {:name => "john"}
phone_book = {name: "ashley"}
~~~

~~~shell
rails g migration add_user_id_to_tweets user_id:integer
rake db:migrate
rails g uploader photo
rails g migration add_photo_url_to_tweets photo_url:string
rake db:migrate
~~~
