http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create-deploy-python-flask.html#configure-your-flask-application-for-eb

Set up AWS Access Key ID and Access Secret. Add to `~/.aws/credentials` as the `[default]` profile.

Leave out the `--profile dmil` on all commands below unless you are dmil.

```
eb init -p python2.7 hks-flask --profile dmil
eb init --profile dmil
eb create hks-flask --profile dmil
```