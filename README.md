# pjproject_es
Developed based on open source PJSIP-2.3.

Official link:
https://www.pjsip.org/
https://github.com/pjsip/pjproject/releases
https://github.com/pjsip/pjproject

Since our main chip uses little-endian mode, we need to define the following macros in our own project:
#define PJ_IS_LITTLE_ENDIAN 1
#define PJ_IS_BIG_ENDIAN 0
