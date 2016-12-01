# Concourse examples

## Create an space

```
fly --target tutorial login --concourse-url http://192.168.100.4:8080
fly --target tutorial sync
```

## First pipeline

```
fly sp --target tutorial -c pipelines/first/pipeline.yml -p diego-pipe
fly --target tutorial unpause-pipeline -p diego-pipe
fly --target tutorial trigger-job --job diego-pipe/job_helloworld --watch
```

Show recent builds
```
fly --target tutorial builds
```

## Delete pipeline
```
fly destroy-pipeline --target tutorial -p diego-pipe
```
