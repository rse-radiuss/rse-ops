## Maintenance for RSE-ops vs. DevOps

RSE-ops on HPC means that a number of systems are running all the time.
They require a team to monitor, maintain, and take care of them. Cloud
development does not require the resource requester to think about
maintenance of a system any longer than the resource is needed. The
resources are truly \"on demand.\" An instance, or small container
cluster, might be requested when it's needed, and brought down and
forgotten about when the work is done. This is a much easier interaction
for the user, as they can request what they need when they need it. For
a DevOps team, even if they are deploying container-based services, they
don't need to worry about long term care or maintenance of servers.

From the user perspective (the researcher or end-user of a cloud
service), both HPC and cloud users don't need to think about maintenance
of the system. The resources are available and can be requested. Thus,
the stark difference is that organizations with HPC typically host them
on-premise, meaning that the organization needs to pay for everything
from people to maintain and operate to the energy and cooling of the
systems [@Carlyle2010-ga]. On the other hand, although operational costs
might be reduced using a cloud resource, that cost can explode quickly
depending on the kind and scale of cloud resource that is needed (e.g.,
GPUs) [@Li2020-lm]. There is much knowledge in the HPC community about
hidden costs from the cloud, and doing comparisons between cloud and
on-premise to find that on-premise can be half the costs
[@Morgan2021-em; @nersc-cloud-study]. One of the challenges is that the
costs are constantly changing. Despite wanting to ultimately maximize
profits, cloud providers typically provide cost calculators to help with
this, provide free-tiers and \"spot instances\" at a lower cost, high
use discounts, and do not charge for services (e.g., instances) that are
turned off [@Power2018-ru].

While we cannot suggest universal best practices for maintenance, it is
logical that each institution needing resources do a cost benefit
analysis to compare all options that meet a set of community needs. It
might be more logical for small organizations (that perhaps cannot
afford hosting and maintaining their own) to use cloud resources, and
for larger organizations that are constantly using resources to host
their own to save money.