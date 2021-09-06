## Permissions for RSE-ops vs. DevOps

One of the biggest challenges of using an HPC system is likely
permissions. Although users can pull from container registries or
install software from repositories, they are not permitted to write to
anywhere other than a standard home or scratch space. While some users
have project spaces that are shared by multiple users, they can be a
pain to manage. This is in contrast to a cloud environment where it's
fairly easy to spin up a new instance and be root to do whatever you
please. This is unlikely to change, and will be a factor that needs to
be worked around.

This isn't to say that root should be always required, or that allowing
the user to have it is best practice. Container technologies are
increasingly going \"rootless,\" meaning they can operate fairly
successfully in user space [@charlie; @podman; @Priedhorsky2021-xx].
Arguably, if the HPC community had been more involved with the Open
Container Initiative (OCI) earlier, \"rootless\" containers would have
been a prominent point earlier and we'd be farther along now. There is
clearly no \"fix\" to give a user extended permissions, but rather
software that can empower them to deploy their user stacks without
asking for permission. Along with rootless container technologies,
package managers like [pip](https://pypi.org/project/pip/) or
[conda](https://docs.conda.io/en/latest/) can make it easy to install
software in user space.