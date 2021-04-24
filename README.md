一个使用epoll和libco实现的简单web服务器

This is a simple http server realized by cpp.

Main features:
1. Use epoll to realize socket io;
2. Use libco coroutine to avoid file io block.

Usage:

step1: cd simple_cpp_web_server

step2: mkdir build && cd build && cmake .. && make -j4

step3: build directory /data/http_file_dir, and add files that can be get by client

step4: run server by ./my_http_server &

Then you can get files from your server with browser. (example: input [server_ip]:3344/index.html，default port is 3344)

To do:
1. Add config to confirm server port and file directory;
2. When qps getting higher, TCP sticky packet problem need to be solved.
