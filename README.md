# perlstuff

## Basic concepts

### [Module management](http://www.cpan.org/modules/INSTALL.html)

- Module search: http://www.cpan.org/modules/index.html

#### Setup

** Using [`perlbrew`](https://perlbrew.pl/) seems attractive, but build is super long: **
Sort of like `nvm`
```
curl -L https://install.perlbrew.pl | bash
source ~/perl5/perlbrew/etc/bashrc
perlbrew install perl-5.34.0
perlbrew switch perl-5.34.0
```
- This actual builds perl from source.  Time consuming.  Put it into Dockerfile build perhaps.

** The official way seems brittle and high maintenance: **
- Use `cpanm` to install modules
```
# Basic setup for new machine
sudo apt-get -y cpanminus  && \
    sudo cpan App::cpanminus  # Run configuration app
```
- Installing a module:

[LWP::UserAgent](https://metacpan.org/pod/LWP::UserAgent#NAME)  implements a web client:
```
cpan install LWP::UserAgent
# If you don't do sudo, you get a user-only install
```


