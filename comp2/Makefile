# 组件B的Makefile（生成动态库）
CC ?= gcc
CFLAGS ?= -Wall -Wextra -fPIC  # -fPIC：位置无关代码（动态库必需）
LDFLAGS ?= -shared             # -shared：生成动态库
TARGET = $(INCLUDE_DEPENDENCIES)/libcomp2.so              # 动态库目标文件（命名规则：libxxx.so）

# 编译规则：生成动态库
all: $(TARGET)

$(TARGET):comp2.c comp2.h
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $<
	cp comp2.h $(INCLUDE_DEPENDENCIES)
# 清理编译产物
clean:
	rm -f $(TARGET)
