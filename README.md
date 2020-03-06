# Custom-OPA-Policies
This is a repo of several examples of OPA policies that would be key to facilitating DoD DSOP.

There are three in particular.
# dropAllCapabilitiesUnlessClearedNamespace
This custom OPA constraint template and constraint allows for configuration as to what linux capabilities are permitted and what namespaces are excluded from that limitation.
The original constraint template from Google operated under a blacklist philosophy (list what namespaces this policy constraint applies to), not a whitelist philosophy. I edited the template to permit the passing of an excluded namespace list which the constraint would not apply to.

# dcarOnlyAllowedRepo
This custom OPA constraint would allow for the configuration of DSOPs to only be able to pull images from IronBank or some other trusted source of containers in that particular impact levl.

# allIngressMustBeHttps
This is actually not custom, but was important enough to ISO 27001 that I felt it should be included. This constraint template and constraint prevent kubernetes ingresses from being created that do not leverage TLS.
