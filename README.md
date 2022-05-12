# nats_cheet
## run nats tools in docker 
```
docker run -it --rm -v ${PWD}:/app -w /app  synadia/nats-box 
```
## run nats tools in k8s 
```
kubectl run --rm -it --image synadia/nats-box nats-test

```
## import operator
```
nsc add operator -u ./stage_eu20/operator.jwt  --force
```


## check account jwt remote
```
nats request "\$SYS.REQ.ACCOUNT.$ACCOUNT_ID.CLAIMS.LOOKUP" "" --creds 
```
## list all accounts remote
```
nats request "\$SYS.REQ.CLAIMS.LIST" "" --creds 
```

### others
```
nsc list accounts
nsc import account -j dts_account.jwt --force --private-key SOAGYFQHHEKQ3IPTDX2LEREGT75AYHYOXCODAWPWGFPDAYRNULSK6IPZSY.nk 

```
