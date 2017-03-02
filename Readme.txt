李云《驾驭Makefile》中的huge项目的完整源代码，
对于书中的代码进行了细微的调整：
（1）在huge/build/Makefile文件中的调整如下：
all:
	@set -e;\
	export ROOT=~huge;\  -----> 加了这行代码
	for dir in $(DIRS)
