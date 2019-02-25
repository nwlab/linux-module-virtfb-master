# linux-module-virtfb-master
Virtual frame buffer driver for embedded devices

Virtual Framebuffer driver:

The VFB driver is a very basic framebuffer driver that allows creation and management
of an arbitrary number of framebuffer devices.

This is a basic driver which allows the user to create N virtual framebuffers.
These framebuffers are no more than contiguous physical memory regions that
are wrapped by the standard framebuffer device interface.

Further information regarding this driver can be found at the Freescale community.
https://community.freescale.com/message/292215#29221

Building the kernel module:
In virtual_fb source directory: 
  make -C <path to kernel sources>  M=`pwd`

Use:
The kernel module takes a single argument vfbcount which is an integer
number of virtual framebuffers which will be created. The default size of the
framebuffers is 128x128 16bpp, but this can be reconfigured using fbset after
the module is loaded.
