#
# Makefile for the kernel security code
#

obj-$(CONFIG_KEYS)			+= keys/
subdir-$(CONFIG_SECURITY_SELINUX)	+= selinux
subdir-$(CONFIG_SECURITY_SMACK)		+= smack
subdir-$(CONFIG_SECURITY_TOMOYO)        += tomoyo
subdir-$(CONFIG_SECURITY_APPARMOR)	+= apparmor
subdir-$(CONFIG_SECURITY_YAMA)		+= yama
subdir-$(CONFIG_SECURITY_LOADPIN)	+= loadpin
subdir-$(CONFIG_SECURITY_DEFEX)		+= defex_lsm
subdir-$(CONFIG_SECURITY_DSMS)		+= dsms

# always enable default capabilities
obj-y					+= commoncap.o
obj-$(CONFIG_MMU)			+= min_addr.o

# Object file lists
obj-$(CONFIG_SECURITY)			+= security.o
obj-$(CONFIG_SECURITYFS)		+= inode.o
obj-$(CONFIG_SECURITY_SELINUX)		+= selinux/
obj-$(CONFIG_SECURITY_SMACK)		+= smack/
obj-$(CONFIG_AUDIT)			+= lsm_audit.o
obj-$(CONFIG_SECURITY_TOMOYO)		+= tomoyo/
obj-$(CONFIG_SECURITY_APPARMOR)		+= apparmor/
obj-$(CONFIG_SECURITY_YAMA)		+= yama/
obj-$(CONFIG_SECURITY_LOADPIN)		+= loadpin/
obj-$(CONFIG_CGROUP_DEVICE)		+= device_cgroup.o
obj-$(CONFIG_SECURITY_DEFEX)		+= defex_lsm/built-in.o
obj-$(CONFIG_SECURITY_DSMS)		+= dsms/

# Object integrity file lists
subdir-$(CONFIG_INTEGRITY)		+= integrity
obj-$(CONFIG_INTEGRITY)			+= integrity/

# Knox SDP
ifndef CONFIG_NO_SDP_BASE
obj-y += sdp/
obj-y += sdp/built-in.o
endif

# TIMA uevent
obj-$(CONFIG_TIMA)     += tima_uevent/tima_uevent.o

# TZ ICCC
obj-$(CONFIG_TZ_ICCC)	  += tz_iccc/

# MST driver
obj-$(CONFIG_MST_LDO)	  += mstdrv/

