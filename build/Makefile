.PHONY: all clean
# 注意：huge模块于foo模块和bar模块的关系-->huge模块使用foo模块和bar模块
# 这就导致foo模块和bar模块必须在huge模块之前构建完成，
# 也就是说，以下3行代码的顺序中，必须保证foo和bar在前，huge必须在最后
DIRS = $(ROOT)/source/foo/src \
	   $(ROOT)/source/bar/src \
	   $(ROOT)/source/huge/src

RM = rm
RMFLAGS = -rf
RMS = $(ROOT)/build/exes $(ROOT)/build/libs

all:
	@set -e;\
	export ROOT=~/huge
	for dir in $(DIRS);\
	do \
		cd $$dir && $(MAKE);\
	done
	@echo ""
	@echo ":-) Completed"
	@echo ""

clean:
	@set -e;\
	export ROOT=~/huge
	for dir in $(DIRS);\
	do \
		cd $$dir && $(MAKE) clean;\
	done
	$(RM) $(RMFLAGS) $(RMS)
	@echo ""
	@echo ":-) Completed"
	@echo ""
