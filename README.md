obs-studio-retroglx
===================================

OBS Studio application with retrofited GLX support.

What is this repo?
-------------------

This is just a fork of the original OBS-Studio repository, which reimplements the original GLX support as legacy, in order to be compatible with plugins that require it.

But why?
---------

OBSProject team deprecated GLX-specific code on their 28.0.0 release tag in favour of EGL.
Despite this change making total sense due to GLX being poorly optimized for modern hardware, on linux particularly 
some older and even modern sttuborn drivers (*cough* nvidia *cough*) dont fully support all of their features on EGL,
leaving a big gap of what can be done in EGL vs GLX.

There are plugins out there for OBS that relies heavily on features specifically provided by the GLX portion of these drivers, that simply couldnt work anymore on the new EGL implementation.

This repository added back GLX support in order for those plugins to be still usable in modern OBS versions.


Will this be supported in the future?
---------------------------------------

I doubt it. This solution is far from ideal, but until those drivers finally receive the love they deserve from their developers, there is no choice but to keep older implementations around.


Something doesnt work, can i get support?
--------------------------------------------

Nope, neither from me nor the original OBSProject team.

This fork is provided as is, if some plugins dont work on this modified version then you are out of luck.
You can contribute with the fixes required by downloading the repository and making the appropriate changes, then sending me a PR.

If you are reading this, then you are out of the OBSProject support scope anyways.



Which builds are available?
------------------------------

Right now the project can be built manually on the same platforms as the unmodified obs-studio.
But since I dont have any particular reason to provide binaries for all platforms, im adding prebuilt packages only for my target: `DEB Ubuntu Focal amd64`

If there is any particular binary you may need, open an issue on the repo and I may add it when I have time.


Quick Links
-----------

- Original repository: https://github.com/obsproject/obs-studio

- Original Website: https://obsproject.com

- Original Help/Documentation/Guides: https://github.com/obsproject/obs-studio/wiki

- Original Build Instructions: https://github.com/obsproject/obs-studio/wiki/Install-Instructions


- Please donate to the original project at: https://obsproject.com/contribute
