obj-m := kobject-wq.o

all: modules
modules:
	make -C /lib/modules/${shell uname -r}/build M=$(PWD) modules

clean:
	make -C /lib/modules/${shell uname -r}/build M=$(PWD) clean
