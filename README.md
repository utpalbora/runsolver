# runsolver v3.4.0

Clone of runsolver v3.4.0 from http://www.cril.univ-artois.fr/~roussel/runsolver/.  

Tool to customize system limit and timeout while running benchmarks.

## Compile

cd src  
``make -j `nproc```  

## Useage

`./runsolver --timestamp -C 1200 -W 180 -R 10000 -V 10000 -w watch.log -v values.log -o tool_output.log ./tool_name tool_args`  

1. -C is for CPU time limit in seconds. Sum total of all the threads.  
2. -W is the Wall clock time limit in seconds.  
3. -R is the maximum resident segment size limit in Kilo Bytes.  
4. -V is the maximum virtual memory limit in Kilo Bytes.  
5. -w is the watcher log file. It logs thread specific details.  
6. -v is the key value pair log file. Smaller and easier to parse.  
7. -o is the log file for stdout and stderr redirect of the tool being run.  
