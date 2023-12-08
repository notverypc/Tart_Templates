# Tart Templates for macOS VMs

This is based on the templates created by Cirrus Labs
https://github.com/cirruslabs/macos-image-templates

# Requirements

Tart 
https://tart.run

Packer
https://www.packer.io

macOS IPSW file.

# Using the Template

To create a macOS VM run the following command:

```
packer build -var vm_name=<NameOfVM> -var ipsw_path=<Path/To/IPSW> macos_template.pkr.hcl
```

Changing <NameOfVM> to the name of the VM and <Path/To/IPSW> to the path of your IPSW file

The `vm_name=<NameOfVM>` is optional. If left out the default name `macOS` will be used:

```
packer build -var ipsw_path=<Path/To/IPSW> macos_template.pkr.hcl
```

To change the default username & password edit the `ssh_username` & `ssh_password` variables in the macos_template.pkr.hcl

Once the VM has been built you can use Screen Sharing to access the VM.