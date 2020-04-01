# HAProxy RPM tools

Mount in a .gitconfig if you want. Make a directory like `dist-git` to work in.

    docker run --rm -it -v $PWD/dist-git:/dist-git -v $PWD/.gitconfig:/root/.gitconfig quay.io/dmace/haproxyrpmtools
    
    kinit dmace
    
    rhpkg clone haproxy --branch rhaos-3.11-rhel-7
    rhpkg clone haproxy --branch rhaos-4.4-rhel-8
    
    rpmdev-bumpspec -c "Fix ..." haproxy.spec
    
    rhpkg srpm
    rhpkg scratch-build --srpm <rpm>

    rhpkg push
    rhpkg build

