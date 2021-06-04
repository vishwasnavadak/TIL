# TIL

2021-06-02:

In Sequelize (ORM), To do a bulk `upsert`, we can use `bulkCreate` with `updateOnDuplicate` parameter. 

https://stackoverflow.com/questions/48124949/nodejs-sequelize-bulk-upsert
https://sequelize.org/master/class/lib/model.js~Model.html#static-method-bulkCreate

2021-05-31: 

For RDS Databases on AWS, `max_connections` could be calculated using the memory class of the RDS instances. 

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.MaxConnections
