PATH += $PATH:/home/i/a/attitude_adjustment/staging_dir/toolchain-mipsel_r2_gcc-4.6-linaro_uClibc-0.9.33.2/usr/bin
CC = mipsel-openwrt-linux-gcc
LIBS = /home/i/a/attitude_adjustment/staging_dir/toolchain-mipsel_r2_gcc-4.6-linaro_uClibc-0.9.33.2/lib/libpcap.a /home/i/a/attitude_adjustment/staging_dir/toolchain-mipsel_r2_gcc-4.6-linaro_uClibc-0.9.33.2/lib/libiconv-stub/lib/libiconv.a
CFLAGS = -Wall -g -O2
INC_DIR=/home/i/a/attitude_adjustment/staging_dir/target-mipsel_r2_uClibc-0.9.33.2/usr/include
LINK_DIR=/home/i/a/attitude_adjustment/staging_dir/target-mipsel_r2_uClibc-0.9.33.2/usr/lib

OBJ  = main.o md5.o zdclient.o 
.PHONY: all

all: zdclient

zdclient: $(OBJ)
	$(CC) $(CFLAGS) -o $@ $(OBJ) $(LIBS) -I$(INC_DIR) -L$(LINK_DIR)

main.o : main.c
	$(CC) $(CFLAGS) -c $< -I$(INC_DIR)

md5.o	: md5.c md5.h
	$(CC) $(CFLAGS) -c $< -I$(INC_DIR)

zdclient.o : zdclient.c
	$(CC) $(CFLAGS) -c $< -I$(INC_DIR)
	
clean :
	rm -v $(OBJ) zdclient
