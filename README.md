# Deploy Reaction Commerce on AWS Elastic Beanstalk
Code to deploy Reaction Commerce on AWS Elastic Beanstalk. This is early stage so there may be issues. Please let me know if you have ideas to make this work better especially for the nginx setup.

## User Guide:
[How To: Deploy Reaction Commerce on AWS Elastic Beanstalk](https://medium.com/@JungleCat/how-to-deploy-reaction-commerce-on-aws-elastic-beanstalk-c0c3dd59a042).

## Enter your:
##### Dockerfile
- ROOT_URL
- MONGO_URL
- REACTION EMAIL, USER & AUTH

- For custom deployments, change FROM yourdockeraccount/yourdockerimage:yourtag
##### Dockerfile.aws.json
- For custom deployments, change 'Name'field to yourdockeraccount/yourdockerimage:yourtag
##### .ebextensions/01-nginx-setup.config
- Replace all occurences of yourdomain.com with your domain

## Notes
If you are on mac, open terminal in your directory an run
./maczip
to create a zip for elastic beanstalk otherwise your zip file may cause EB to fail.
