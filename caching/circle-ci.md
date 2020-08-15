# Circle-CI

https://circleci.com/docs/2.0/caching/  
https://circleci.com/docs/2.0/configuration-reference/\#save\_cache  
https://circleci.com/docs/2.0/configuration-reference/\#restore\_cache  


```text
- save_cache:
  steps:
    - save_cache:
        key: my-cache
        paths:
          - my-file.txt
          - my-project/my-dependencies-directory

- restore_cache:
  steps:
      - restore_cache:
        keys:
          - v1-deps-{{ checksum "package-lock.json" }}
          - v1-deps
```



