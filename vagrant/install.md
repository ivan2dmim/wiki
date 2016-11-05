Vagrant
-------

Install latest Vagrant

    $ vagrant_url="https://releases.hashicorp.com/vagrant/"
    $ vagrant_version=$(wget -q "$vagrant_url" -O- | html2text | grep vagrant_ | sed 's/\s*\*\s*vagrant_//g' | head -n1)
    $ vagrant_file="vagrant_${vagrant_version}_x86_64.deb"
    $ wget $vagrant_url/$vagrant_version/$vagrant_file
    $ sudo dpkg -i $vagrant_file
