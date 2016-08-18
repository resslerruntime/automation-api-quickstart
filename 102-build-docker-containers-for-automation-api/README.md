## Automation api container
How to building container with pre installed and pre configured automation-api

**HOST** - Control-M endpoint host  
**USER** - Control-M user account for automation  

```bash
SRC_DIR=.
HOST=<host>
USER=<user>
PASSWORD=<password>
sudo docker build --tag=controlm \
  --build-arg HOST=$HOST \
  --build-arg USER=$USER \
  --build-arg PASSWORD=$PASSWORD $SRC_DIR
```

Examples for running automation commands using the container
```bash
sudo docker run              -it controlm  ctm conf servers::get  
sudo docker run -v $PWD:/src -it controlm  ctm build /src/AutomationAPISampleFlow.json
```

See the [Automation API - Services](https://docs.bmc.com/docs/display/public/workloadautomation/Control-M+Automation+API+-+Services) documentation for more information.  
See the [Automation API - Code Reference](https://docs.bmc.com/docs/display/public/workloadautomation/Control-M+Automation+API+-+Code+Reference) documentation for more information.