# pjproject_es
Developed based on open source PJSIP-2.3.  
Official link:  
https://www.pjsip.org/  
https://github.com/pjsip/pjproject/releases  
https://github.com/pjsip/pjproject  


Related dependencies:  
https://github.com/uuidjs/uuid/releases
(we use 1.0.3)

Sample cross-compilation configuration  
./configure --prefix=`pwd`/__install --host=arm-dspg-linux CC=arm-dspg-linux-uclibceabi-gcc AR=arm-dspg-linux-uclibceabi-ar LINK=arm-dspg-linux-uclibceabi-gcc CXX=arm-dspg-linux-uclibceabi-g++ --disable-v4l2 --disable-openh264  

Since our main chip uses little-endian mode, we need to define the following macros in our own project:  

#define PJ_IS_LITTLE_ENDIAN 1  
#define PJ_IS_BIG_ENDIAN 0  

E.g
#define PJ_IS_LITTLE_ENDIAN			1  
#define PJ_IS_BIG_ENDIAN			  0  

#include <pj/log.h>  
#include <pjlib.h>  
#include <pjlib-util.h>  
#include <pjnath.h>  
#include <pjmedia.h>  
#include <pjmedia-codec.h>  
#include <pjsip.h>  
#include <pjsip_simple.h>  
#include <pjsip_ua.h>  
#include <pjsua-lib/pjsua.h>  
#include <pjsua-lib/pjsua_internal.h>  
