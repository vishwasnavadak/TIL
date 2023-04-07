# TIL

## 2023-04-07

Install/Update HomeBrew Package without having to update all of homebrew

```sh
HOMEBREW_NO_AUTO_UPDATE=1 brew install aws/tap/aws-sam-cli
```

Ref: https://github.com/Homebrew/brew/issues/1670#issuecomment-267096602


## 2022-12-16

Change linked Repository of Amplify

https://github.com/aws-amplify/amplify-hosting/issues/288#issuecomment-737192995

<img width="1033" alt="image" src="https://user-images.githubusercontent.com/13111030/208035590-710ef74e-db70-40a1-94ef-e7c4d9270287.png">


## 2022-07-14

Universal Link Validators

* iOS: https://search.developer.apple.com/appsearch-validation-tool/
* Third Party: https://branch.io/resources/aasa-validator/

Common Issues:
1. `/.well-known/apple-app-site-association` files needs to have a custom rewrite if website is a react app. 
<img width="1151" alt="image" src="https://user-images.githubusercontent.com/13111030/178991071-b5ef5303-a8e0-4d88-addc-ced5782989b7.png">
2. If website has www and no www sites / redirects, both of them needs to have in the applinks on ios config.

Documentation: https://developer.apple.com/library/archive/documentation/General/Conceptual/AppSearch/UniversalLinks.html#//apple_ref/doc/uid/TP40016308-CH12-SW2




## 2022-07-13

Remote Inspect from Android Studio and XCode for Capacitor Apps

https://stackoverflow.com/a/67920303


## 2022-05-18

Get Parent Commit hash of a commit hash

https://stackoverflow.com/a/25664507/2526327

```
git rev-list --parents -n 1 <commithash>
```

## 2022-05-17

Rebasing the unverified commits to verified commits on GitHub.

https://stackoverflow.com/a/59351278/2526327

You can do this by re-committing it:

    git rebase -i <commit before first problematic commit>

After this, your text editor will open up. Change every `pick` to `edit`.

After that you'll have to re-commit every commit with the following command:

    git commit --author="<name> <<E-Mail(once in brackets, see example)>>" -S --amend --no-edit
    git rebase --continue

In the end, you'll have to overwrite the remote by doing

    git push --force-with-lease

This is better than `git push -f` but you should also be careful.

If someone knows a way to do this automatically, tell me in the comments.

example of the commit command:

    git commit --author="testuser <testuser@github.com>" -S --amend --no-edit




## 2022-01-18

Fixing misconfigured `.gitignore` 

https://stackoverflow.com/a/38983205

## 2021-12-29

Deleting undeletable AWS Amplify Deployements with Backend

https://github.com/aws-amplify/amplify-console/issues/2456


## 2021-10-26

List all Enums on PostgreSQL

https://stackoverflow.com/questions/9540681/list-postgres-enum-type

## 2021-10-01

UUID for Google Sheet Cells: https://stackoverflow.com/a/51254597/2526327

## 2021-09-26

Pi Hole can be run locally on Macbook: https://www.imore.com/how-run-pi-hole-your-mac


## 2021-08-12

Famous [shortId](https://www.npmjs.com/package/shortid) npm package is depracated. Recommended to use [NanoId](https://github.com/ai/nanoid/) instead.


## 2021-07-23

Tool to Plan and Allocate IP Ranges to VPC and Subnets - https://network00.com/NetworkTools/IPv4AddressPlanner/

## 2021-06-29

Docker image initially built (`docker build`) in local and pushed to ECR will not work if it is build in Apple M1 Processor. Would be better to build in Linux env (Github Action/Other pipeline). 

https://stackoverflow.com/questions/67361936/exec-user-process-caused-exec-format-error-in-aws-fargate-service

## 2021-06-23

AWS Nodejs sdk for s3 getObject call has a limit of 2GB for single part download.
https://github.com/aws/aws-sdk-js/issues/2916


## 2021-06-21

Clear all local docker builds/images,
```sh
# To delete all containers including its volumes use,

docker rm -vf $(docker ps -a -q)

# To delete all the images,

docker rmi -f $(docker images -a -q)

```

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
