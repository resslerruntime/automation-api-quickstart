## Create Your First Hadoop Job Flow

Tutorial on the [product web page](https://docs.bmc.com/docs/display/ctmSaaSAPI/Running+applications+and+programs+in+your+environment)  that explains how to write jobs that execute Spark and HDFS commands.

```javascript
"ProcessData": {
    "Type": "Job:Hadoop:Spark:Python",
    "SparkScript": "file:///home/[USER]/automation-api-quickstart/controlm-saas/101-running-hadoop-spark-job-flow/processData.py",

    "Arguments": [
        "file:///home/[USER]/automation-api-quickstart/controlm-saas/101-running-hadoop-spark-job-flow/processData.py",
        "file:///home/[USER]/automation-api-quickstart/controlm-saas/101-running-hadoop-spark-job-flow/processDataOutDir"
    ],

    "PreCommands" : {
        "Commands" : [
            { "rm":"-R -f file:///home/[USER]/automation-api-quickstart/controlm-saas/101-running-hadoop-spark-job-flow/processDataOutDir" }
        ]                   
    }
}
```

See the [Automation API - Services](https://docs.bmc.com/docs/display/ctmSaaSAPI/Services) documentation for more information.  
See the [Automation API - Code Reference](https://docs.bmc.com/docs/display/ctmSaaSAPI/Code+Reference) documentation for more information.
