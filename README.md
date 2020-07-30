# lab.kurniawan.dev

Place for experiments! https://lab.kurniawan.dev

```shell script
aws cloudformation deploy \
  --stack-name "ku-lab" \
  --template-file "site.yml" \
  --parameter-overrides $(cat "site.params" | tr '\n' ' ') \
  --capabilities CAPABILITY_NAMED_IAM \
  --no-fail-on-empty-changeset
```

Upload
```shell script
aws s3 sync ../src s3://ku-lab-websitebucket-jked6f73blhz
```
