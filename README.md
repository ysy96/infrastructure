# infrastructure

**Switch AWS Profile**
```
export AWS_PROFILE=prod
```
**Create Stack and Resources**
```
aws cloudformation create-stack \
--stack-name myStack1 \
--template-body file://cicd-infra.yaml \
--capabilities CAPABILITY_NAMED_IAM
```

```
aws cloudformation create-stack \
--stack-name myStack2 \
--template-body file://csye6225-infra.yaml \
--capabilities CAPABILITY_NAMED_IAM
```
**Delete Stack and Resources**
```
aws cloudformation delete-stack --stack-name myStack
```

**Import SSL Certificate**
```
aws acm import-certificate --certificate fileb://prod_songyue_me.crt \
    --certificate-chain fileb://prod_songyue_me.ca-bundle \
    --private-key fileb://prod.songyue.mekey
```