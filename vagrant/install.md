Vagrant
-------

Install latest Vagrant

    $ vagrant_url="https://releases.hashicorp.com/vagrant"
    $ vagrant_prefix="vagrant_"
    $ vagrant_suffix="_x86_64.deb"
    $ vagrant_version=$(wget -q "$vagrant_url" -O- | html2text | grep "$vagrant_prefix" | \
          sed 's/\s*\*\s*'$vagrant_prefix'//g' | head -n1)
    $ vagrant_file="${vagrant_prefix}${vagrant_version}${vagrant_suffix}"
    $ wget $vagrant_url/$vagrant_version/$vagrant_file
    $ sudo dpkg -i $vagrant_file
