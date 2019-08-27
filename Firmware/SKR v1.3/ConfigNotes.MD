# Migration from MKS GEN L:
Boards are almost exactly same in size and ports location, mount holes.
I just removed MKS GEN L and put SKR v1.3 in place.

# HW Changes:
* Z Capacitive probe - I removed optocupler that I was using and connected to my printer directly.
* TMC2208 Drivers - I had to solder down back legs since TMC2208 has all the connections routed under the driver.
* None of my existing displays were working - I've tried re-assiging pins and creating adapter cables. Nope.