include Makefile.define

# 默认超作
default:all

# 主应用文件列表
PATS = BaseCommand.o TcpTest.o ./IniRead/dictionary.o ./IniRead/iniparser.o

LIB_BASE_OBJS = BaseCommand.o TcpTest.o dictionary.o iniparser.o
LIB_BASE = libTcpTest.so

all: libTcpTest.so clear
			
# 主应用程序
all:$(LIB_BASE) Makefile

$(LIB_BASE):$(PATS)
	$(CC) -shared -o $(LIB_BASE) $(LIB_BASE_OBJS) $(LIBS)

# 清理
clean:
	rm -rf *.o  $(LIB_BASE) $(LIB_BASE_OBJS)
clear:	
	mv libTcpTest.so ../../PurenessScopeServer/Linux_Bin/	
cl:	
	rm -rf *.o 
