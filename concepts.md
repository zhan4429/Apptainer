## Why do we use a OS Base Image with Docker if containers have no Guest OS
Since all Linux distributions run the same (yup, it's a bit simplified) Linux kernel and differ only in userland software, it's pretty easy to simulate a different distribution environment - by just installing that userland software and pretending it's another distribution. Being specific, installing CentOS container inside Ubuntu OS will mean that you will get the userland from CentOS, while still running the same kernel, not even another kernel instance.

So lightweight virtualization is like having isolated compartments within same OS. Au contraire real virtualization is having another full-fledged OS inside host OS. That's why docker cannot run FreeBSD or Windows inside Linux.

If that would be easier, you can think docker is kind of very sophisticated and advanced chroot environment.

Docker containers are similar to virtual machines, but don't create an entire virtual operating system. Instead, Docker enables the app to use the same Linux kernel as the system that it's running on. This allows the app package to only require parts not already on the host computer, reducing the package size and improving performance.


https://stackoverflow.com/questions/32756988/what-is-meant-by-shared-kernel-in-docker