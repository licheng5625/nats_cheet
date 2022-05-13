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

## nats connect to jetstream
```
nats consumer next 9c73d047-bab3-4d31-9197-67ca2fa0e235 resampled_moaa-6007983E9FB3415390C3CA796AB26900-65FBC58D1DE447AB9FD41DCB71399A24-847D2247C80B476986B4E509AB4159C6  --js-api-prefix=NEWTON.API --trace --creds  
```


### others
```
nsc list accounts
nsc import account -j dts_account.jwt --force --private-key SOAGYFQHHEKQ3IPTDX2LEREGT75AYHYOXCODAWPWGFPDAYRNULSK6IPZSY.nk 

```
