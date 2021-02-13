.PHONY : all clean cleanall

TARGET = LD.BIN
all : $(TARGET)

SRCS = LD.ASM LDCALL.ASM LDCCP.ASM LDDEF.ASM LDDIO.ASM \
LDDISK.ASM LDDPB.ASM LDFILE.ASM LDFILE2.ASM LDINIT.ASM \
LDIO.ASM LDOS.ASM LDWORK.ASM

OBJS = binhead.bin LD_0.bin

AS     = pasmo
AOPT   = --bin


$(TARGET) : $(OBJS)
	cat $(OBJS) > $@

LD_0.bin : $(SRCS)
	$(AS) $(AOPT) LD.ASM $@ LD.lst

clean :
	-rm $(OBJS) $(OBJS:%.bin=%.lst)

cleanall : clean
	-rm $(TARGET)
