
IOP_BIN = pademu.irx
IOP_OBJS = pademu.o sys_utils.o imports.o exports.o
IOP_OBJS_DIR = obj.pademu/

ifeq ($(VMC),1)
IOP_CFLAGS += -DVMC
endif

IOP_OBJS := $(IOP_OBJS:%=$(IOP_OBJS_DIR)%)

IOP_CFLAGS += -Wall -fno-builtin -DUSE_SMSUTILS
IOP_LDFLAGS += -s

all: OBJ_DIR $(IOP_BIN)

clean:
	rm -f $(IOP_BIN) $(IOP_OBJS)

rebuild: clean all

OBJ_DIR:
	mkdir -p $(IOP_OBJS_DIR)

include $(PS2SDK)/Defs.make
include Rules.make
