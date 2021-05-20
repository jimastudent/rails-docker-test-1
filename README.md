[For heroku]
export PATH=/usr/local/bin:$PATH
sudo su
curl https://cli-assets.heroku.com/install.sh | sh

heroku login

heroku config:add BLOG_DATABASE='heroku_eafdb61123ab929' -a rails-docker-test-1    
heroku config:add BLOG_DATABASE_USERNAME='b358168ac58eab' -a rails-docker-test-1    
heroku config:add BLOG_DATABASE_PASSWORD='2df581bd' -a rails-docker-test-1    
heroku config:add BLOG_DATABASE_HOST='us-cdbr-east-03.cleardb.com' -a rails-docker-test-1    


[AWS Cloud9 First command for installs]
For docker-compose: 
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

[For rails]
docker-compose run web rails new . --force --database=mysql
sudo chown -R ec2-user:ec2-user blog/
sudo chown -R ec2-user:ec2-user src/
docker-compose build

docker-compose run web db:create

[change permission]
sudo chown -R ec2-user:ec2-user blog/
sudo chown -R ec2-user:ec2-user src/

aaa