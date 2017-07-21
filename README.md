# TPM2-sealed LUKS encryption keys

See [this post](https://robertou.com/tpm2-sealed-luks-encryption-keys.html) for
more information.

## This is an updated version for general use. It also includes setup scripts and will work without modifications to the IBM TSS2 Stack.

It was modified to do the following things:
 * Encrypt all LUKS Containers with the same key (you want to have your swap encrypted, right?)
 * Do the setup automatically
 * Generate a backup key (to store on backup volumes, usb drives or maybe dna)
 * Don't modify the make process of IBM TSS2. Let's be honest: This will only break compability when the IBM project changes
 * It assumes default passwords (default password is "luks") for the existing luks devices and can remove them. This is mainly for mass deployment of machines.
 
