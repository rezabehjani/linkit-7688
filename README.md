# linkit-7688

* compile 
```
#for download dependency make
sudo make download

#openwrt 15
sudo make -j1 V=s -i

#openwrt 19
sudo make -j1 V=s FORCE_UNSAFE_CONFIGURE=1


#note for flag make
#- Verbose = V
#- Verbosity level 1 = w (warnings/errors only)
#- Verbosity level 99 = s (This gives stdout+stderr) 
#job =1 
#-i, --ignore-errors 	Ignore all errors in commands executed to remake files. 
#-k, --keep-going 	Continue as much as possible after an error. While the target that failed, and those that depend on #it, cannot be remade, the other dependencies of these targets can be processed all the same. 

```

* note if make file not curectly work 
```
./scripts/feeds update
./scripts/feeds install a
```


*for download package for reposetory 
```
./scripts/feeds install mountd
# name packege mountd
```


*for go back defult config
```
make clean
make dirclean
make distclean
```
