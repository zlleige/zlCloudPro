
# 使用的编译器
CC=gcc
# 预处理参数
CPPLFAGS=-I
CFLAGS=-Wall
# 需要链接的动态库
LIBS=

# 子目标, 因为是测试,所有需要单独生成很多子目标
main=./main

# 最终目标
target=$(main)
ALL:$(target)

# 生成所有的.o 文件
%.o:%.c
	$(CC) -c $< -o $@ $(CPPLFAGS) $(CFLAGS)

# 生成每一个子目标, 
# main程序
$(main):test/main.o test/fdfs_api.o make_log.o
	$(CC) $^ $(LIBS) -o $@

# 项目清除
clean:
	-rm -rf *.o $(target) ./test/*.o

# 声明伪文件
.PHONY:clean ALL
