# startmoduletut
wip tutorial how to start a module / script distribution

In the early days of programming no installing software wasn't done so at worst you had to find your script in a maze of folders most often the installation was also cumbersome and often avoided. 

The perl language is a practical language but after a while to effective maintain your scripts and module you will need a way to install /  test and to distribute your software.

# initiating
- module-starter found by installing 'libmodule-starter-perl' from the ubuntu apt repo. The way you use this depends on the way you want to use your software in the future an automatically configures the most basic things by default so you can worry about actual writing code. example `module-starter --module Example::Module --builder=ExtUtils::MakeMaker --author=YourName --email=gg@gmail.com --ignores=git --ignores=generic --minperl=5.22.1` with the oftions explained by the manual. 

```
Usage:
    module-starter [options]

    Options:

        --module=module  Module name (required, repeatable)
        --distro=name    Distribution name (optional)
        --dir=dirname    Directory name to create new module in (optional)

        --builder=module Build with 'ExtUtils::MakeMaker' or 'Module::Build'
        --eumm           Same as --builder=ExtUtils::MakeMaker
        --mb             Same as --builder=Module::Build
        --mi             Same as --builder=Module::Install

        --author=name    Author's name (taken from getpwuid if not provided)
        --email=email    Author's email (taken from EMAIL if not provided)

        --ignores=type   Ignore type files to include (repeatable)
        --license=type   License under which the module will be distributed
                         (default is artistic2)
        --minperl=ver    Minimum Perl version required (optional;
                         default is 5.006)

        --fatalize       Generate code that causes all warnings to be fatal with:
                         use warnings FATAL => 'all'

        --verbose        Print progress messages while working
        --force          Delete pre-existing files if needed

        --help           Show this message

    Available Licenses:

        perl, artistic, artistic2, mit, mozilla, mozilla2, bsd, freebsd, cc0,
        gpl, lgpl, gpl3, lgpl3, agpl3, apache, qpl

    Available Ignore Types:

        cvs, git, hg, manifest, generic
        (NOTE: If manifest is included, the MANIFEST file will be skipped
        and only a MANIFEST.SKIP file will be included.)

    Example:

        module-starter --module=Foo::Bar,Foo::Bat \
            --author="Andy Lester" --email=andy@petdance.com

```

# Version/file tracking
- git 
- cvs
- hg, manifest (Rarely used)

# distributing

- github -> Development work
- bitbucket ->Dev also
- cpan -> Have something working and is good and want to share it?

# installation

Three different modules. I use the first.

- ExtUtils::MakeMaker
- Module::Build
- Module::Install

