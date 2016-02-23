This project is for building a .deb package from the Apache Qpid source.

Current requirements (as far as I've deduced)
From debian repositories:
build-essential debhelper libboost-all-dev uuid-dev libsasl2-dev libxqilla-dev libxmltooling-dev libibverbs-dev librdmacm-dev libnspr4-dev libnss3-dev libssl-dev sasl2-bin corosync-dev libxerces-c-dev doxygen help2man valgrind zip procps libnss3-tools pkg-config dpkg-dev chrpath libqpid-proton2-dev cmake swig ruby python-dev python-qpid libaio-dev libdb5.3++-dev libdb++-dev corosync-dev libxmltooling-dev libqpid-proton2-dev 

From pip:
qpid-tools

Build command (note: this skips tests. probably not a great idea):
DEB_BUILD_OPTIONS=nocheck dpkg-buildpackage -us -uc

