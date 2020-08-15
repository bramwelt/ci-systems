# Jenkins

Jenkins doesn't have a native caching solution due to it's execution model and history. There might be ways to emulate it with jobs that save caches to Jenkins' artifact storage, but that won't work as well as other CI system implementations.

When running jobs in [containers](https://jenkins.io/doc/book/pipeline/docker/#caching-data-for-containers) on Jenkins users can take advantage of reusing volumes for their dependencies - These could be named / mounted based on a semi-consistent identifier \(job name, file sha-sum, etc.\) but doesn't provide any strategies for cache eviction or cleanup.

```text
pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
}
```

