FROM fhem/fhem:latest

MAINTAINER Frank Ried

RUN apt-get -y update

RUN apt-get -y upgrade

RUN apt-get install sox

RUN apt-get -y install libsox-fmt-all

RUN apt-get -y install libsodium-dev

RUN apt-get -y install gstreamer1.0-tools

RUN cpan Crypt::Argon2

RUN cpan MIME::Base64

RUN cpan Alien::Base::ModuleBuild

RUN cpan Alien::Sodium
 
RUN cpan Crypt::NaCl::Sodium

RUN cpan IO:String