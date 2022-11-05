# nftguard
This is a simple wrapper that makes (remote) working with nftables (more) safe.

# Usage
To edit the configuration use `nftguard edit`.
After you've edited your configuration you can commit the changes with `nftguard commit`.
You'll be asked to confirm the commited changes.
There is a 30 second timeout so if you lock yourself out `nftguard` will revert to the previous configuration and you'll (hopefully) have access again.

If you want to revert your changes you can do that with `nftguard abort`.

# Requirements
`nftguard` requires Python 3.5 or newer.
This tool assumes the nftables configuration is located at /etc/nftables.conf

# Installation
Copy the `nftguard` file somewhere on `$PATH` and ensure it is executable (if not run `chmod +x /path/to/nftguard`).
