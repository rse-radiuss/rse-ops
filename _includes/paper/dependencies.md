## Dependency Management for RSE-ops vs. DevOps

Dependency management refers to a set of practices used to manage
software versions. It is arguably a subtopic of software distribution.
Every piece of scientific software requires a specific set of versioned
dependencies, and these dependencies must co-exist alongside one another
on a shared resource. This also means that architectures must be
maintained for possibly older dependencies that require them. Tools have
grown out of this need that allow for flexible management of
dependencies and software, including easybuild [@easybuild], spack
[@spack], and environment modules [@LMOD; @environment-modules].
Development of these projects has also led to a powerful model of
development -- bringing many people (administrators and users) together
to collaborate on the software. It's not hard to read user surveys
[@spack-user-survey] and see that the open source model of development,
when done right, is successful. People are using the software, excited
about it, and working together to make it better. It also doesn't hurt
that some of these projects have the backing of entire institutions and
within- and inter-institutional funding programs and resources.

These success stories give us a hint that working together on software,
likely in an open source, collaboration fashion, is a good model for
successful distribution and improvement of the software. This does not
imply that collaboration is always, universally better
[@noauthor_undated-bo], but the authors here believe that it's an
honorable if not idealistic goal to strive for. The challenge here, of
course, is the extra work that it takes to seek out, interact with, and
inform contributors. Not everyone may agree that software can and should
be open and collaborative, and it may even depend on the kind of
software in question.

DevOps is different because you only install what you need, and when you
need it. It's uncommon to require older versions of the same software to
co-exist for a service. Is there any kind of mapping of this freedom to
research software engineering? Yes, arguably containerization, primarily
with container technologies suitable for an HPC environment
[@singularity; @charlie; @shifter], has allowed for encapsulation of an
entire operating system and software stack that can be used in a
portable manner. However, as was noted in the description of testing,
development and deployment of these containers is unlikely to be on the
resource itself. Ultimately, if we can better use unprivileged container
technologies, running builds on clusters could be possible.

There also, until recently [@shpc] has not been an easy way for a
cluster user or Linux administrator to install, manage, and provide
containers. External registries that might be used
[@sregistry; @distribution-spec] must exist alongside a resource and
then require an individual to explicitly pull a container binary. While
this is better than not having containers available at all, it creates
redundancy of file-system space, and requires the individual to be a
stickler about container versions pulled, good practices, and
organization of said containers. This is not an easy thing to do, and
thus it's hard to follow best practices [@ten-simple-rules]. Development
of these technologies, however, hinted at the idea that with some
innovation, it could be possible to empower users to better embrace more
DevOps style practices of developing, testing, and deploying research
software (RSEops). It also hinted at a more modular strategy for
dependency management. Interestingly, containers are used heavily by
both cloud and HPC developers, but developing them and ensuring security
in their execution adds additional challenges.