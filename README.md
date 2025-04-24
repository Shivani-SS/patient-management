Commands and info
--------------

For aws cdk
first install node.js and the in command prompt
npm install -g aws-cdk

------------------------------
aws configure
AWS Access Key ID [None]: test
AWS Secret Access Key [None]: test
Default region name [None]: us-east-1
Default output format [None]: json

aws --endpoint-url=http://localhost:4566 lambda list-functions
{
  "Functions": []
}
--------------------------------------
get jwt secret key from online
https://jwtsecret.com/
generate key copy and use for environment variable
-------------------------------------
cd analytics-service/

change to required directory

docker build -t analytics-service:latest .
cd ..
cd auth-service/
docker build -t auth-service:latest .

do this for all services to build and run docker images

for api-gateway add different application-prod.yml which has different uri for prod or any environment
cd ..
cd api-gateway/
docker build -t api-gateway:latest .

cd ..
cd infrastructure/
./localstack-deploy.sh



