## arena serve tensorflow

Submit tensorflow serving job to deploy and serve machine learning models.

### Synopsis

Submit tensorflow serving job to deploy and serve machine learning models.

```
arena serve tensorflow [flags]
```

### Options

```
      --command string           the command will inject to container's command.
      --cpu string               the request cpu of each replica to run the serve.
  -d, --data stringArray         specify the trained models datasource to mount for serving, like <name_of_datasource>:<mount_point_on_job>
      --enableIstio              enable Istio for serving or not (disable Istio by default)
  -e, --envs stringArray         the environment variables
      --gpus int                 the limit GPU count of each replica to run the serve.
  -h, --help                     help for tensorflow
      --image string             the docker image name of serve job, default image is tensorflow/serving:latest (default "tensorflow/serving:latest")
      --memory string            the request memory of each replica to run the serve.
      --modelConfigFile string   Corresponding with --model_config_file in tensorflow serving
      --modelName string         the model name for serving
      --modelPath string         the model path for serving in the container
      --port int                 the port of tensorflow gRPC listening port (default 8500)
      --replicas int             the replicas number of the serve job. (default 1)
      --restfulPort int          the port of tensorflow RESTful listening port (default 8501)
      --servingName string       the serving name
      --servingVersion string    the serving version
      --versionPolicy string     support latest, latest:N, specific:N, all
```

### Options inherited from parent commands

```
      --arenaNamespace string   The namespace of arena system service, like TFJob (default "arena-system")
      --config string           Path to a kube config. Only required if out-of-cluster
      --loglevel string         Set the logging level. One of: debug|info|warn|error (default "info")
      --namespace string        the namespace of the job (default "default")
      --pprof                   enable cpu profile
```

### SEE ALSO

* [arena serve](arena_serve.md)	 - Serve a job.

###### Auto generated by spf13/cobra on 7-Sep-2018