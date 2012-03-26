RVM/Bundler Installation Check
==============================

The purpose of this project is to check if the installation of RVM and Bundler worked properly. To run the check, type:

    rake check

If things go well, you should see:

    Success  RVM, Ruby and Bundler appear installed correctly

Troubleshooting
---------------

**cannot load such file -- bundler/setup**
This means that the Bundler gem is not installed. Install it by:

    gem install bundler


**Could not find gem 'thor (>= 0) ruby' in the gems available on this machine. Run 'bundle install' to install missing gems.**

A gem is missing. Run:

    bundle install

**ruby ruby-1.9.3 is not installed. To install do: 'rvm install ruby-1.9.3'**

The Ruby version is missing. Run the installation as instructed:

    rvm install ruby-1.9.3

To install RVM in the first place, see the [offical installation instructions][1]. Be sure to also read through
the [platform-specific notes][2].


[1]: https://rvm.beginrescueend.com/rvm/install/
[2]: https://rvm.beginrescueend.com/os/