# Concourse examples

```
fly --target tutorial login --concourse-url http://192.168.100.4:8080
fly -t tutorial sync
```

## First pipeline

```
fly sp -t tutorial -c pipelines/first/pipeline.yml -p diego-pipe
fly -t tutorial pause-pipeline -p diego-pipe
fly -t tutorial trigger-job --job diego-pipe/job_helloworld --watch
```

Show recent builds
```
fly -t tutorial builds
```


