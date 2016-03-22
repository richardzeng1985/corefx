# .NET Core Libraries (CoreFX)

The corefx repo contains the library implementation (called "CoreFX") for [.NET Core](http://github.com/dotnet/core). It includes System.Collections, System.IO, System.Xml, and many other components. You can see more information in [Documentation](Documentation/README.md). The corresponding [.NET Core Runtime repo](https://github.com/dotnet/coreclr) contains the runtime implementation (called "CoreCLR") for .NET Core. It includes RyuJIT, the .NET GC, and many other components. Runtime-specific library code - namely [mscorlib][mscorlib] - lives in the CoreCLR repo. It needs to be built and versioned in tandem with the runtime. The rest of CoreFX is agnostic of runtime-implementation and can be run on any compatible .NET runtime.

[mscorlib]: https://github.com/dotnet/coreclr/tree/master/src/mscorlib

## Build Status

|   | Debug | Release |
|---|------:|--------:|
|**CentOS 7.1**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/centos7.1_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/centos7.1_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_centos7.1_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_centos7.1_debug_rc2/)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/centos7.1_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/centos7.1_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_centos7.1_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_centos7.1_release_rc2/)|
|**Debian 8.2**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/debian8.2_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/debian8.2_debug_rc2)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/debian8.2_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/debian8.2_release_rc2)|
|**openSUSE 13.2**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/opensuse13.2_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/opensuse13.2_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_opensuse13.2_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_opensuse13.2_debug_rc2/)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/opensuse13.2_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/opensuse13.2_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_opensuse13.2_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_opensuse13.2_release_rc2/)|
|**OS X 10.11**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/osx_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/osx_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_osx_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_osx_debug_rc2/)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/osx_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/osx_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_osx_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_osx_release_rc2/)|
|**Red Hat 7.2**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/rhel7.2_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/rhel7.2_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_rhel7.2_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_rhel7.2_debug_rc2/)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/rhel7.2_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/rhel7.2_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_rhel7.2_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_rhel7.2_release_rc2/)|
|**Ubuntu 14.04**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/ubuntu_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/ubuntu_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_ubuntu14.04_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_ubuntu14.04_debug_rc2/)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/ubuntu_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/ubuntu_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_ubuntu14.04_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_ubuntu14.04_release_rc2/)|
|**Ubuntu 15.10**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/ubuntu15.10_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/ubuntu15.10_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_ubuntu15.10_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_ubuntu15.10_debug_rc2/)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/ubuntu15.10_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/ubuntu15.10_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_ubuntu15.10_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_ubuntu15.10_release_rc2/)|
|**Windows 7**|[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_win7_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_win7_debug_rc2)|[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_win7_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_win7_release_rc2)|
|**Windows 8**|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/windows_nt_debug_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/windows_nt_debug_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_windows_nt_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_windows_nt_debug_rc2)|[![build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/windows_nt_release_rc2.svg?label=build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/windows_nt_release_rc2)<br/>[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_windows_nt_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_windows_nt_release_rc2)|
|**Windows 10**|[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_win10_debug_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_win10_debug_rc2)|[![outerloop build & test](https://img.shields.io/jenkins/s/http/dotnet-ci.cloudapp.net/job/dotnet_corefx/outerloop_win10_release_rc2.svg?label=outerloop+build+%26+test)](http://dotnet-ci.cloudapp.net/job/dotnet_corefx/job/outerloop_win10_release_rc2)|

## How to Engage, Contribute and Provide Feedback

Some of the best ways to contribute are to try things out, file bugs, and join in design conversations. If you are having issues with the Full .NET Framework or .NET Runtime, the best way to file a bug is at [Connect](http://connect.microsoft.com/VisualStudio) or through [Product Support](https://support.microsoft.com/en-us/contactus?ws=support) if you have a contract.

Want to get more familiar with what's going on in the code?
* [Pull requests](https://github.com/dotnet/corefx/pulls): [Open](https://github.com/dotnet/corefx/pulls?q=is%3Aopen+is%3Apr)/[Closed](https://github.com/dotnet/corefx/pulls?q=is%3Apr+is%3Aclosed)
* [![Backlog](https://cloud.githubusercontent.com/assets/1302850/6260412/38987b1e-b793-11e4-9ade-d3fef4c6bf48.png)](https://github.com/dotnet/corefx/issues?q=is%3Aopen+is%3Aissue+label%3A%220+-+Backlog%22), [![Up Next](https://cloud.githubusercontent.com/assets/1302850/6260418/4c2c7a54-b793-11e4-8ce1-a27ff5378d08.png)](https://github.com/dotnet/corefx/issues?q=is%3Aopen+is%3Aissue+label%3A%221+-+Up+Next%22) and [![In Progress](https://cloud.githubusercontent.com/assets/1302850/6260414/41b0fc30-b793-11e4-9d50-d09563cd138a.png)](https://github.com/dotnet/corefx/issues?q=is%3Aopen+is%3Aissue+label%3A%222+-+In+Progress%22) changes

Looking for something to work on? The list of [up-for-grabs issues](https://github.com/dotnet/corefx/labels/up%20for%20grabs) is a great place to start. See some of our guides for more details:

* [Contributing Guide](Documentation/project-docs/contributing.md)
* [Developer Guide](Documentation/project-docs/developer-guide.md)
* [Issue Guide](Documentation/project-docs/issue-guide.md)

We've also started to share some of our direction via more higher-level documentation, specifically:

* [Road to RTM](Documentation/project-docs/rtm.md)
* [How we triage](Documentation/project-docs/triage.md)
* [Porting to .NET Core](Documentation/project-docs/porting.md)

You are also encouraged to start a discussion by filing an issue or creating a
gist.

You can discuss .NET OSS more generally in the [.NET Foundation forums].

Want to chat with other members of the CoreFX community?

[![Join the chat at https://gitter.im/dotnet/corefx](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/dotnet/corefx?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[.NET Foundation forums]: http://forums.dotnetfoundation.org/

## .NET Core Library Components

The repo contains the source for each of the assemblies that comprises .NET Core.  Each ```Microsoft.*``` or ```System.``` folder under
[src](https://github.com/dotnet/corefx/tree/master/src) represents an individual library.  Each such folder may contain a ```ref``` folder,
which contains the source representing the "contract" or "reference assembly" for that library.  It may also contain a ```src``` folder,
which contains the source for some or all of the implementation for that library (some implementation may live in mscorlib in the 
[coreclr repo](https://github.com/dotnet/coreclr), with the build tooling generating type forwards from the library assembly to mscorlib.)  
It may also contain a ```test``` folder containing the tests associated with that library, whether the implementation source lives in corefx 
or in coreclr.

## Daily Builds

Daily builds of .NET Core components are published to [dotnet-core MyGet gallery](https://www.myget.org/gallery/dotnet-core).
The latest version number of each library can be seen in that gallery.

## License

.NET Core (including the corefx repo) is licensed under the [MIT license](LICENSE).

## .NET Foundation

.NET Core is a [.NET Foundation](http://www.dotnetfoundation.org/projects) project.

## Related Projects
There are many .NET related projects on GitHub.

- The [.NET home repo](https://github.com/Microsoft/dotnet) links to 100s of .NET projects, from Microsoft and the community.
- The [.NET Core repo](https://github.com/dotnet/core) links to .NET Core related projects from Microsoft.
- The [ASP.NET home repo](https://github.com/aspnet/home) is the best place to start learning about ASP.NET 5.
- [dotnet.github.io](http://dotnet.github.io) is a good place to discover .NET Foundation projects.
