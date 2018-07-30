# hello-r
This is a basic hello world R app which loads the *stringr* package to output capitalised text to the console. This was pulled from https://github.com/cloudfoundry/r-buildpack/tree/master/fixtures/simple_packages

After `cf push`, the app will fail but you can view the results using `cf logs <APPNAME> --recent` 

```
   2018-07-30T11:04:35.87+1000 [APP/PROC/WEB/0] OUT > x <- "hello world"
   2018-07-30T11:04:35.87+1000 [APP/PROC/WEB/0] OUT > cat("R program running")
   2018-07-30T11:04:35.87+1000 [APP/PROC/WEB/0] OUT R program running> print(stringr::str_to_upper(x))
   2018-07-30T11:04:35.90+1000 [APP/PROC/WEB/0] OUT [1] "HELLO WORLD"
   2018-07-30T11:04:35.90+1000 [APP/PROC/WEB/0] OUT > 
   2018-07-30T11:04:35.91+1000 [APP/PROC/WEB/0] OUT Exit status 0
```

When content, `cf stop` the app so it doesn't trigger any internal monitoring alerts.
