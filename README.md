# BipedController
A Biped Controller for fully procedural hand/feel movements


## VR introduction
A series of steps was derived to achieve the minimum viable VR layout with HMD and controller tracking, here:
- [VR MVP](VR_MVP.md)

## Unity Package Manager support /#upm

Add to your project via the Unity Package Manager. 
1. In the Package Manger, select "Add package from Git URL..."
2. Type in 
```
https://github.com/yohash/BipedController.git#upm
```

The `upm` branch is maintained us a current subtree via:
```
git subtree split --prefix=Assets/BipedController --branch upm
```

## Dependencies

This package has dependencies on other custom packages. To allow for automatic installion of dependencies
- [yohash.fabrik](https://github.com/yohash/Fabrik)

Please first install the [mob-sakai/GitDependencyResolverForUnity](https://github.com/mob-sakai/GitDependencyResolverForUnity). The git dependency resolver can be installed in the Unity package manager with this direct git link:
```
https://github.com/mob-sakai/GitDependencyResolverForUnity.git
```
