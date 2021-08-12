# TIL


## 2021-08-12

Famous [shortId](https://www.npmjs.com/package/shortid) npm package is depracated. Recommended to use [NanoId](https://github.com/ai/nanoid/) instead.


## 2021-06-29

Docker image initially built (`docker build`) in local and pushed to ECR will not work if it is build in Apple M1 Processor. Would be better to build in Linux env (Github Action/Other pipeline). 

https://stackoverflow.com/questions/67361936/exec-user-process-caused-exec-format-error-in-aws-fargate-service

## 2021-06-23

AWS Nodejs sdk for s3 getObject call has a limit of 2GB for single part download.
https://github.com/aws/aws-sdk-js/issues/2916


## 2021-06-21

Clear all local docker builds/images

https://stackoverflow.com/questions/44785585/docker-how-to-delete-all-local-docker-images

## 2021-06-11

`mysqldump` supports exporting the table structure without the data when we pass `--no-data`

https://stackoverflow.com/questions/6175473/mysql-export-schema-without-data


## 2021-06-02

In Sequelize (ORM), To do a bulk `upsert`, we can use `bulkCreate` with `updateOnDuplicate` parameter. 

https://stackoverflow.com/questions/48124949/nodejs-sequelize-bulk-upsert
https://sequelize.org/master/class/lib/model.js~Model.html#static-method-bulkCreate

## 2021-05-31

For RDS Databases on AWS, `max_connections` could be calculated using the memory class of the RDS instances. 

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.MaxConnections
