### Example Performance Test for Welcome-Service
You may run this either in the GUI, or on the CLI. 
For getting actual Performance Results, use the CLI. 
For debugging and test suite development, use the GUI. 

### Run Jmeter Via Cli and Generate html report
_this assumes you have set JMETER_HOME environment variable and exported the path to the bin directory_
```
jmeter -n -t welcome-service/welcome-service.jmx -l ./out -e -o ./html/ -f -Dwelcome.service.threads=5000 -Dwelcome.service.ramp=1 -Dwelcome.service.loops=1 -Dhost=localhost -Dport=8081
```
### Flags
[See all CLI flag options here: Jmeter Cli Reference](https://jmeter.apache.org/usermanual/get-started.html#non_gui)

```
-n  starts jmeter in non-gui (cli) mode

-f  force deletes any prior html report 
    or files in the specified output directory
    so the current test results can take its place

-t  specifies the Jmeter Test suite location

-l  Specifies where to put the logfile that 
    the html report generator will use

-e  Tells jmeter to generate an html report

-o  Specifies the output directory
```

