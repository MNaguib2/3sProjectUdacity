# 3sProjectUdacity

URL Front end :
      http://mena-udagram.s3-website-us-east-1.amazonaws.com
      
firstly 
  configuration Database in aws from service RDS after this made database accessable to any Ip from vpc security group 
  then get url specialist databse and add in project to can package sequalize to connect to db 
  
second 
  prepare user from IAM and select from tabe users after create select from permission administrator Access to control in all to avaliable use terminal pc by 
  AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY and REGION this data will show one item and not show again after this you can made second step
  
  prepare Elastic Beanstalk to update app api node js after made all configuration special DB Cloud 
  upload and create environment via terminal first  'eb init --udagram-api --platform node.js --region us-east-1' 
                                                    this command create file configuration spcial EB and 
  'eb create --sample udagram-api-dev' to create defualt or simple test to confirm every thing is ok and 
  'eb deploy udagram-api-dev' write this command but don't forget made 'npm run build' first bfore command eb deploy to upload your project api to cloud 
  Don't forget add all environment variables from right tab and select configuration and software edite  
 
 third 
  prepare s3 bucket to upload app frontend after create bucket go to tabe permission and select edit from tabe 'Bucket policy'
  to add this policy 
                     {
                          "Version": "2012-10-17",
                          "Statement": [
                              {
                                  "Sid": "PublicReadGetObject",
                                  "Effect": "Allow",
                                  "Principal": "*",
                                  "Action": "s3:GetObject",
                                  "Resource": "arn:aws:s3:::mena-udagram/*"
                              }
                          ]
                      }
   and go to tabe 'Block public access (bucket settings)' to confirm not select on any checkbox specialist block to made bucket access from outside and public 
fourth and finaly create file configuration circleCI 
to made first check if node package install or not if not install package
2- save every package in special project if api or frontend in path node_module
3- run test to all application
  to confirm not found any error before made deploy in cloude
4- made build to all project api and frontend 
5- deploy all project to change in frontend or in backend 
