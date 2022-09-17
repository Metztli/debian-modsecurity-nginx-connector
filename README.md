Nginx 1.23.1 / ModSecurity v3 Connector v1.0.3 for Debian Bullseye Backports
============================================================================

 Builds newer upstream release of [Engine X (Nginx) 1.23.1](https://nginx.org) , as well as
 [ModSecurity v3 Nginx Connector v1.0.3 module](https://github.com/SpiderLabs/ModSecurity-nginx)
 based on git unstable [Debian Packaging for Nginx 1.22.0-3](https://salsa.debian.org/nginx-team/nginx.git) hack.
 
 Includes [b2evolution](https://b2evolution.net) *The most integrated CMS ever* sample configuration file for *Nginx*, as well. 

 Of course, you need the proper Debian tools to build packages, as well as libmodsecurity3 already installed,
 as elaborated at [Metztli IT's Tonalamatl ](https://metztli.blog/nochtli/build-libmodsecurity3-module-and-its)

 Before installing libmodsecurity3 make sure you have/do:

 `apt-get -t bullseye-backports install libyajl2 libmaxminddb0 liblua5.4-0 libgeoip1 libfuzzy2 libcurl4`

 Then, download:
 Nginx 1.23.1-3 most recent ModSecurity v3 builds for Metztli Reiser4 / Debian Bullseye backports for AMD64:

 [libmodsecurity3_3.0.7-1_amd64.deb](https://metztli.it/readOnlyEphemeral/libmodsecurity3_3.0.7-1-for-Bullseye/libmodsecurity3_3.0.7-1_amd64.deb)
 [libmodsecurity3_3.0.7-1_amd64.deb.SHA256SUM](https://metztli.it/readOnlyEphemeral/libmodsecurity3_3.0.7-1-for-Bullseye/libmodsecurity3_3.0.7-1_amd64.deb.SHA256SUM)

 [libmodsecurity-dev_3.0.7-1_amd64.deb](https://metztli.it/readOnlyEphemeral/libmodsecurity3_3.0.7-1-for-Bullseye/libmodsecurity-dev_3.0.7-1_amd64.deb)
 [libmodsecurity-dev_3.0.7-1_amd64.deb.SHA256SUM](https://metztli.it/readOnlyEphemeral/libmodsecurity3_3.0.7-1-for-Bullseye/libmodsecurity-dev_3.0.7-1_amd64.deb.SHA256SUM)

 install:
 `dpkg -i libmodsecurity3_3.0.7-1_amd64.deb libmodsecurity-dev_3.0.7-1_amd64.deb`


 Make sure dependencies in debian/control are fulfilled before build.

 Please review the debian/changelog file.
 :first_quarter_moon_with_face: I used *dch* to modify/upgrade the debian/changelog file, i.e.,

 `dch -v 1.23.1-3 -D metztli`

 *-D metztli* was optional, of course.

 Once inside the cloned directory, make a symbolic link:
 `ln -s debian/patches`

 Apply debian patches with:
 `quilt push -a --fuzz=0`
 
 Build with:
 `fakeroot debian/rules binary`


 Huelmati [Enjoy]!
