# Local MacPorts repository

This is a local MacPorts repository, containing some packages that
aren't available in the main MacPorts tree.  To use it, create a clone
of the git repository:

    git clone git://github.com/dcreager/ports.git

This will create a *ports* directory in the current directory.  Next,
add the following line to your */opt/local/etc/macports/sources.conf*
file:

    file://«path to ports directory»

For instance, if you checked out the git repository into
*/Users/dcreager/ports*, then the line would be:


    file:///Users/dcreager/ports

Yes, that's three slashes at the beginning.

## Adding Ports

To add more Ports to this repository, just create the appropriate
Portfiles as described in the [MacPorts Users
Guide](http://guide.macports.org/).  Before committing the new
Portfile into the Git repository, please ensure that you run

    portindex

from the top-level directory.  This will ensure that the repository
will be usable immediately after checkout.
