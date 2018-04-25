# pigzfly
Parallel tar/gzip/netcat for use over AWS direct connect *(not encrypted)

Our AWS direct connect to our VPC is 500 mb/sec, but a single stream can only do about 50.  This streams the files over netcat with parallel gzip (pigz) which is probably about as fast as can be expected.

ruby tools/pigzfly.rb --threads 4 --source /home/michael/foo --target remote_host:/tmp/foo/
