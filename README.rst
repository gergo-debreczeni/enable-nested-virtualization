**Enable nested virtualization in ESXI 5.1 for KVM**

add this at the end of the .vmx file, but make sure that there is no other instruction named the same. also, after downloading the .vmx file, delete it from ESXI and delete the .vmx~ (backup file).

vcpu.hotadd = "FALSE"
featMask.vm.hv.capable = "Min:1"
vhv.enable = "TRUE"



**Enable nested virtualization in ESXI 5.1 for hyper-v**

modify the value of "guestOS" to "winhyperv".