Packer
-------

Install latest Packer

    $ packer_url="https://releases.hashicorp.com/packer"
    $ packer_prefix="packer_"
    $ packer_suffix="_linux_amd64.zip"
    $ packer_version=$(wget -q "$packer_url" -O- | html2text | grep "$packer_prefix" | \
          sed 's/\s*\*\s*'$packer_prefix'//g' | head -n1)
    $ packer_file="${packer_prefix}${packer_version}${packer_suffix}"
    $ wget $packer_url/$packer_version/$packer_file
    $ sudo unzip -d /usr/local/bin/ $packer_file
