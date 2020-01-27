Nginx 1.17.8 / ModSecurity v3 Connector v1.0.1 for Debian Buster Backports
==========================================================================

 Builds newer upstream release of [Engine X (Nginx) 1.17.8](https://nginx.org) , as well as
 [ModSecurity v3 Nginx Connector v1.0.1 module](https://github.com/SpiderLabs/ModSecurity-nginx)
 from unstable [Debian Packaging for Nginx](http://deb.debian.org/debian/pool/main/n/nginx/nginx_1.16.1-3.debian.tar.xz) hack
 
 Includes [b2evolution](https://b2evolution.net) *The most integrated CMS ever* sample configuration file for *Nginx*, as well. 

 Of course, you need the proper Debian tools to build packages, as well as libmodsecurity3 already installed,
 as elaborated at [Metztli IT's Tonalamatl 'Blog'](https://metztli.blog/index.php/build-libmodsecurity3-module-and-its?blog=4) 

 Nginx 1.17.8-1 most recent ModSecurity v3 builds for Metztli Reiser4 / Debian Buster backports for AMD64:
 [libmodsecurity3_3.0.4-1_amd64.deb](https://metztli.it/readOnlyEphemeral/ModSecurity3_3.0.4-for-buster/libmodsecurity3_3.0.4-1_amd64.deb)
 [libmodsecurity3_3.0.4-1_amd64.deb.SHA256SUM](https://metztli.it/readOnlyEphemeral/ModSecurity3_3.0.4-for-buster/libmodsecurity3_3.0.4-1_amd64.deb.SHA256SUM)

 [libmodsecurity-dev_3.0.4-1_amd64.deb](https://metztli.it/readOnlyEphemeral/ModSecurity3_3.0.4-for-buster/libmodsecurity-dev_3.0.4-1_amd64.deb) 
 [libmodsecurity-dev_3.0.4-1_amd64.deb.SHA256SUM](https://metztli.it/readOnlyEphemeral/ModSecurity3_3.0.4-for-buster/libmodsecurity-dev_3.0.4-1_amd64.deb.SHA256SUM)

 Make sure dependencies in debian/control are fulfilled before build.

 Please review the debian/changelog file.
 :first_quarter_moon_with_face: feel free to use *dch* to modify the debian/changelog file.

 Apply debian patches with:
 `quilt push -a --fuzz=0`
 
 Build with:
 `fakeroot debian/rules binary`


 Huelmati [Enjoy]!
