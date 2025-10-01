# cat: not the pet, but the command!
The challenge asks to open the terminal in the pwn.college DOJO and use the cat command to read the file.

## My Solution
**Flag:** pwn.college{Eh0t-c-yUEa48seZXnpl-i2YLc3.QXxcTN0wSOzEzNzEzW}

We open the terminal on the linux interface provided by pwn.college and use the command "cat flag" to read the contents of the flag file in the home directory.
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{Eh0t-c-yUEa48seZXnpl-i2YLc3.QXxcTN0wSOzEzNzEzW}
```

## What I learned
I learned how to read a file using the cat command on a linux interface.

## References
None.


# Catting Absolute Paths
The challenge requires us to use the absolute path while using the cat command.

## My Solve
**Flag:** pwn.college{0SnowjTNYUf2pEsHctT1Ficv79f.QX5ETO0wSOzEzNzEzW}
We use the command cat /flag, which shows the absolute path of the flag rather than within the directory.
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{0SnowjTNYUf2pEsHctT1Ficv79f.QX5ETO0wSOzEzNzEzW}
```

## What I learned
I learned how to use the cat command with an absolute path as an argument.

## References
None


# More Catting Practice
In this challenge, we find the flag hidden in a more complex directory.

## My Solve
**Flag:** pwn.college{AB5l9H-hjiGoBZ9lNp6LTXJ8aI6.QXwITO0wSOzEzNzEzW}

 The directory of the flag is given in the console, for which we need to run the command cat /lib/ssl/flag to read the contents of the flag.md file.

```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /lib/ssl/flag. Go cat it out **without** cding into that directory!
hacker@commands~more-catting-practice:~$ cat /lib/ssl/flag
pwn.college{AB5l9H-hjiGoBZ9lNp6LTXJ8aI6.QXwITO0wSOzEzNzEzW}
```

## What I learned
I learned how to use the absolute path of a file to read it using the cat command.

## References
None.


# Grepping for a Needle in a Haystack
In this challenge, we get introduced to the grep command to search for certain keywords within a file

## My solve
**Flag:** pwn.college{EthIuqe52J52DEub0feTsNTgxwr.QX3EDO0wSOzEzNzEzW}
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{EthIuqe52J52DEub0feTsNTgxwr.QX3EDO0wSOzEzNzEzW}
```

I run the command grep pwn.college /challenge/data.txt as the flag was hidden in the data.txt file, which gave the serach result with the flag.

## What I learned
I learned how to use the grep command to search for contents in a file.

## References 
None.


# Comparing Files
In this challenge, we learn how to use the diff command to find out the differences between the contents of two files.

## My Solve
**Flag:** pwn.college{EthIuqe52J52DEub0feTsNTgxwr.QX3EDO0wSOzEzNzEzW}

```
hacker@commands~comparing-files:~$ cd /
hacker@commands~comparing-files:/$ cd challenge
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt
50a51
> pwn.college{05qb6K-H1sTST_88SqE6W2K9ktF.01MwMDOxwSOzEzNzEzW}
```

## What I learned
I learned how to use the diff command and display the difference between the contents in two files.

## References
None.


# Touching Files
In this challenge we learn how to create files using the touch command

## My Solve
**Flag: ** pwn.college{UqVLwmVZygS-5o7aIQ7SPBlBK3a.QXwMDO0wSOzEzNzEzW}

```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{UqVLwmVZygS-5o7aIQ7SPBlBK3a.QXwMDO0wSOzEzNzEzW}

```
## What I learned
I learned how to use the touch command to make files.
## References
None.


# Removing Files
In this challenge we learn how to delete a file using the rm command

## My Solve
**Flag:** pwn.college{AjeihN2XSjN7N-y1Vqy2temuEvw.QX2kDM1wSOzEzNzEzW}

```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{AjeihN2XSjN7N-y1Vqy2temuEvw.QX2kDM1wSOzEzNzEzW}

```

## What I learned
I learned how to use the rm command to delete files.
## References
None.


# Moving Files

## My Solve
**Flag:** pwn.college{k4_87M_QAZL6GEUJASKJSgz3KgM.0VOxEzNxwSOzEzNzEzW}

```
hacker@commands~moving-files:~$ cd /tmp
hacker@commands~moving-files:/tmp$ mv /flag hack-the-planet
Correct! Performing 'mv /flag hack-the-planet'.
hacker@commands~moving-files:/tmp$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{k4_87M_QAZL6GEUJASKJSgz3KgM.0VOxEzNxwSOzEzNzEzW}

```
## What I learned
I learned how to use the mv command to move the contents of two files within two different directories.
## References
None.


# Hidden Files
In this challenge we find out how to access hidden files.

## My solve
**Flag:** pwn.college{YlgGdo7DTWkCK7fWFxoL6iLPysz.QXwUDO0wSOzEzNzEzW}

```
hacker@commands~hidden-files:~$ ls -a
.   .ICEauthority  .cache   .dbus  .local    Desktop    a
..  .bash_history  .config  .java  .mozilla  Downloads  core
hacker@commands~hidden-files:~$ cd .
hacker@commands~hidden-files:~$ cd /.
hacker@commands~hidden-files:/$ ls -a
.                     bin        etc    lib64   nix   run   tmp
..                    boot       home   libx32  opt   sbin  usr
.dockerenv            challenge  lib    media   proc  srv   var
.flag-13342301723744  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ ls
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-13342301723744
pwn.college{YlgGdo7DTWkCK7fWFxoL6iLPysz.QXwUDO0wSOzEzNzEzW}

```
## What I Learned
I learned how to access hidden files using the -a flag to the ls command

## References
None.


# An Epic Filesystem Quest
This challenge involves usage of the cd, ls and cat commands.

## My Solve
**Flag:** pwn.college{kmunQilA3Z1dIAJ0wsAGnINqxUU.QX5IDO0wSOzEzNzEzW}
```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
TIP  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin  challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat TIP
Tubular find!
The next clue is in: /opt/linux/linux-5.4/Documentation/hwmon

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/Documentation/hwmon
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/hwmon$ ls
ab8500.rst               k10temp.rst          occ.rst
abituguru-datasheet.rst  k8temp.rst           pc87360.rst
abituguru.rst            lineage-pem.rst      pc87427.rst
abituguru3.rst           lm25066.rst          pcf8591.rst
abx500.rst               lm63.rst             pmbus-core.rst
acpi_power_meter.rst     lm70.rst             pmbus.rst
ad7314.rst               lm73.rst             powr1220.rst
adc128d818.rst           lm75.rst             pwm-fan.rst
adm1021.rst              lm77.rst             pxe1610.rst
adm1025.rst              lm78.rst             raspberrypi-hwmon.rst
adm1026.rst              lm80.rst             sch5627.rst
adm1031.rst              lm83.rst             sch5636.rst
adm1275.rst              lm85.rst             scpi-hwmon.rst
adm9240.rst              lm87.rst             sht15.rst
ads7828.rst              lm90.rst             sht21.rst
adt7410.rst              lm92.rst             sht3x.rst
adt7411.rst              lm93.rst             shtc1.rst
adt7462.rst              lm95234.rst          sis5595.rst
adt7470.rst              lm95245.rst          smm665.rst
adt7475.rst              lochnagar.rst        smsc47b397.rst
amc6821.rst              ltc2945.rst          smsc47m1.rst
asb100.rst               ltc2978.rst          smsc47m192.rst
asc7621.rst              ltc2990.rst          submitting-patches.rst
aspeed-pwm-tacho.rst     ltc3815.rst          sysfs-interface.rst
coretemp.rst             ltc4151.rst          tc654.rst
da9052.rst               ltc4215.rst          tc74.rst
da9055.rst               ltc4245.rst          thmc50.rst
dme1737.rst              ltc4260.rst          tmp102.rst
ds1621.rst               ltc4261.rst          tmp103.rst
ds620.rst                max16064.rst         tmp108.rst
emc1403.rst              max16065.rst         tmp401.rst
emc2103.rst              max1619.rst          tmp421.rst
emc6w201.rst             max1668.rst          tps40422.rst
f71805f.rst              max197.rst           twl4030-madc-hwmon.rst
f71882fg.rst             max20751.rst         ucd9000.rst
fam15h_power.rst         max31722.rst         ucd9200.rst
ftsteutates.rst          max31785.rst         userspace-tools.rst
g760a.rst                max31790.rst         vexpress.rst
g762.rst                 max34440.rst         via686a.rst
gl518sm.rst              max6639.rst          vt1211.rst
hih6130.rst              max6642.rst          w83627ehf.rst
hwmon-kernel-api.rst     max6650.rst          w83627hf.rst
ibm-cffps.rst            max6697.rst          w83773g.rst
ibmaem.rst               max8688.rst          w83781d.rst
ibmpowernv.rst           mc13783-adc.rst      w83791d.rst
ina209.rst               mcp3021.rst          w83792d.rst
ina2xx.rst               menf21bmc.rst        w83793.rst
ina3221.rst              mlxreg-fan.rst       w83795.rst
index.rst                nct6683.rst          w83l785ts.rst
inspur-ipsps1.rst        nct6775.rst          w83l786ng.rst
ir35221.rst              nct7802.rst          wm831x.rst
ir38064.rst              nct7904.rst          wm8350.rst
isl68137.rst             npcm750-pwm-fan.rst  xgene-hwmon.rst
it87.rst                 nsa320.rst           zl6100.rst
jc42.rst                 ntc_thermistor.rst
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/hwmon$ ls -a
.                        it87.rst             ntc_thermistor.rst
..                       jc42.rst             occ.rst
.INFO                    k10temp.rst          pc87360.rst
ab8500.rst               k8temp.rst           pc87427.rst
abituguru-datasheet.rst  lineage-pem.rst      pcf8591.rst
abituguru.rst            lm25066.rst          pmbus-core.rst
abituguru3.rst           lm63.rst             pmbus.rst
abx500.rst               lm70.rst             powr1220.rst
acpi_power_meter.rst     lm73.rst             pwm-fan.rst
ad7314.rst               lm75.rst             pxe1610.rst
adc128d818.rst           lm77.rst             raspberrypi-hwmon.rst
adm1021.rst              lm78.rst             sch5627.rst
adm1025.rst              lm80.rst             sch5636.rst
adm1026.rst              lm83.rst             scpi-hwmon.rst
adm1031.rst              lm85.rst             sht15.rst
adm1275.rst              lm87.rst             sht21.rst
adm9240.rst              lm90.rst             sht3x.rst
ads7828.rst              lm92.rst             shtc1.rst
adt7410.rst              lm93.rst             sis5595.rst
adt7411.rst              lm95234.rst          smm665.rst
adt7462.rst              lm95245.rst          smsc47b397.rst
adt7470.rst              lochnagar.rst        smsc47m1.rst
adt7475.rst              ltc2945.rst          smsc47m192.rst
amc6821.rst              ltc2978.rst          submitting-patches.rst
asb100.rst               ltc2990.rst          sysfs-interface.rst
asc7621.rst              ltc3815.rst          tc654.rst
aspeed-pwm-tacho.rst     ltc4151.rst          tc74.rst
coretemp.rst             ltc4215.rst          thmc50.rst
da9052.rst               ltc4245.rst          tmp102.rst
da9055.rst               ltc4260.rst          tmp103.rst
dme1737.rst              ltc4261.rst          tmp108.rst
ds1621.rst               max16064.rst         tmp401.rst
ds620.rst                max16065.rst         tmp421.rst
emc1403.rst              max1619.rst          tps40422.rst
emc2103.rst              max1668.rst          twl4030-madc-hwmon.rst
emc6w201.rst             max197.rst           ucd9000.rst
f71805f.rst              max20751.rst         ucd9200.rst
f71882fg.rst             max31722.rst         userspace-tools.rst
fam15h_power.rst         max31785.rst         vexpress.rst
ftsteutates.rst          max31790.rst         via686a.rst
g760a.rst                max34440.rst         vt1211.rst
g762.rst                 max6639.rst          w83627ehf.rst
gl518sm.rst              max6642.rst          w83627hf.rst
hih6130.rst              max6650.rst          w83773g.rst
hwmon-kernel-api.rst     max6697.rst          w83781d.rst
ibm-cffps.rst            max8688.rst          w83791d.rst
ibmaem.rst               mc13783-adc.rst      w83792d.rst
ibmpowernv.rst           mcp3021.rst          w83793.rst
ina209.rst               menf21bmc.rst        w83795.rst
ina2xx.rst               mlxreg-fan.rst       w83l785ts.rst
ina3221.rst              nct6683.rst          w83l786ng.rst
index.rst                nct6775.rst          wm831x.rst
inspur-ipsps1.rst        nct7802.rst          wm8350.rst
ir35221.rst              nct7904.rst          xgene-hwmon.rst
ir38064.rst              npcm750-pwm-fan.rst  zl6100.rst
isl68137.rst             nsa320.rst
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/hwmon$ cat .INFO
Congratulations, you found the clue!
The next clue is in: /usr/share/emacs/26.3/etc/images/icons/allout-widgets

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/hwmon$ cd ..
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation$ cd ..
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4$ cd ..
hacker@commands~an-epic-filesystem-quest:/opt/linux$ cd ..
hacker@commands~an-epic-filesystem-quest:/opt$ cd ..
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/share/emacs/26.3/etc/images/icons/allout-widgets
NOTE-TRAPPED  dark-bg  light-bg
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/emacs/26.3/etc/images/icons/allout-widgets/NOTE-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/lib/debug/.build-id/22

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/debug/.build-id/22
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/22$ ls
86722b153e831464650fd7a2fda29a014e3519.debug  DISPATCH
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/22$ cat DISPATCH
Tubular find!
The next clue is in: /usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/22$ cd /usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ ls
EVIDENCE  distro-test_rkt.dep  distro-test_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ cat EVIDENCE
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/arch/powerpc/math-emu

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ ls -a /opt/linux/linux-5.4/arch/powerpc/math-emu
.         fcmpu.c   fmsub.c    fnmsub.c    fsqrt.c     mcrfs.c   stfs.c
..        fctiw.c   fmsubs.c   fnmsubs.c   fsqrts.c    mffs.c    udivmodti4.c
.TRACE    fctiwz.c  fmul.c     fre.c       fsub.c      mtfsb0.c
Makefile  fdiv.c    fmuls.c    fres.c      fsubs.c     mtfsb1.c
fabs.c    fdivs.c   fnabs.c    frsp.c      lfd.c       mtfsf.c
fadd.c    fmadd.c   fneg.c     frsqrte.c   lfs.c       mtfsfi.c
fadds.c   fmadds.c  fnmadd.c   frsqrtes.c  math.c      stfd.c
fcmpo.c   fmr.c     fnmadds.c  fsel.c      math_efp.c  stfiwx.c
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ cat /opt/linux/linux5.4/arch/powerpc/math-emu/.TRACE
cat: /opt/linux/linux5.4/arch/powerpc/math-emu/.TRACE: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ cat /opt/linux/linux-5.4/arch/powerpc/math-emu/.TRACE
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/sound
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ ls /opt/linux/linux-5.4/include/sound
NUGGET             hda_register.h     seq_oss.h
ac97               hda_regmap.h       seq_oss_legacy.h
ac97_codec.h       hda_verbs.h        seq_virmidi.h
aci.h              hdaudio.h          sh_dac_audio.h
ad1816a.h          hdaudio_ext.h      sh_fsi.h
ad1843.h           hdmi-codec.h       simple_card.h
adau1373.h         hwdep.h            simple_card_utils.h
aess.h             i2c.h              snd_wavefront.h
ak4113.h           info.h             soc-acpi-intel-match.h
ak4114.h           initval.h          soc-acpi.h
ak4117.h           intel-nhlt.h       soc-component.h
ak4531_codec.h     jack.h             soc-dai.h
ak4641.h           l3.h               soc-dapm.h
ak4xxx-adda.h      madera-pdata.h     soc-dpcm.h
alc5623.h          max9768.h          soc-topology.h
asequencer.h       max98088.h         soc.h
asound.h           max98090.h         sof
asoundef.h         max98095.h         sof.h
compress_driver.h  memalloc.h         soundfont.h
control.h          minors.h           spear_dma.h
core.h             mixer_oss.h        spear_spdif.h
cs35l33.h          mpu401.h           sta32x.h
cs35l34.h          omap-hdmi-audio.h  sta350.h
cs35l35.h          opl3.h             tas2552-plat.h
cs35l36.h          opl4.h             tas5086.h
cs4231-regs.h      pcm-indirect.h     tea6330t.h
cs4271.h           pcm.h              timer.h
cs42l52.h          pcm_drm_eld.h      tlv.h
cs42l56.h          pcm_iec958.h       tlv320aic32x4.h
cs42l73.h          pcm_oss.h          tlv320aic3x.h
cs8403.h           pcm_params.h       tlv320dac33-plat.h
cs8427.h           pt2258.h           tpa6130a2-plat.h
da7213.h           pxa2xx-lib.h       uda134x.h
da7218.h           rawmidi.h          uda1380.h
da7219-aad.h       rt286.h            util_mem.h
da7219.h           rt298.h            vx_core.h
da9055.h           rt5514.h           wavefront.h
designware_i2s.h   rt5645.h           wm0010.h
dmaengine_pcm.h    rt5659.h           wm1250-ev1.h
emu10k1.h          rt5660.h           wm2000.h
emu10k1_synth.h    rt5663.h           wm2200.h
emu8000.h          rt5665.h           wm5100.h
emu8000_reg.h      rt5668.h           wm8903.h
emux_legacy.h      rt5670.h           wm8904.h
emux_synth.h       rt5682.h           wm8955.h
es1688.h           s3c24xx_uda134x.h  wm8960.h
gus.h              sb.h               wm8962.h
hda_chmap.h        sb16_csp.h         wm8993.h
hda_codec.h        seq_device.h       wm8996.h
hda_component.h    seq_kernel.h       wm9081.h
hda_hwdep.h        seq_midi_emul.h    wm9090.h
hda_i915.h         seq_midi_event.h   wss.h
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ cat /opt/linux/linux-5.4/include/sound/NUGGET
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/gui-lib/racket/gui/private/compiled$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular$ ls
INSIGHT  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular$ cat INSIGHT
Great sleuthing!
The next clue is in: /usr/lib/python3/dist-packages/rpy2/tests/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular$ ls -a /usr/lib/python3/dist-packages/rpy2/tests/__pycache__
.  ..  .ALERT  __init__.cpython-38.pyc  utils.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular$ cat -a /usr/lib/python3/dist-packages/rpy2/tests/__pycache__/.ALERT
cat: invalid option -- 'a'
Try 'cat --help' for more information.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/Normal/Regular$ cat /usr/lib/python3/dist-packages/rpy2/tests/__pycache__/.ALERT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{kmunQilA3Z1dIAJ0wsAGnINqxUU.QX5IDO0wSOzEzNzEzW}

```

Involved multiple uses of the cat command, the ls command along with the flag -a, and the cd command to move between folders.

# What I learnt
I learnt how to effectively use the three commands.

# References
None.


# Making Directories
In this challenge we learn how to use the mkdir command

## My Solve
**Flag:** pwn.college{MfWOyuNd5scZa62DkzqqzIP-Daa.QXxMDO0wSOzEzNzEzW}
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{MfWOyuNd5scZa62DkzqqzIP-Daa.QXxMDO0wSOzEzNzEzW}
```
The folder is first created and then accessed, after which a file is made within the folder.

## What I learnt
I learnt how to use the mkdir command to make a directory in linux.

## References
None.


# Finding Files
In this challenge we learn how to use the find command in linux

## My Solve

**Flag:** pwn.college{k-az0Cqw-XLxgLctB-yi6c_tFw4.QXyMDO0wSOzEzNzEzW}

```
hacker@commands~finding-files:~$ find
.
./.config
./.config/xfce4
./.config/xfce4/xfconf
./.config/xfce4/xfconf/xfce-perchannel-xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xsettings.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/thunar.xml
./.config/xfce4/xfwm4
./.config/xfce4/desktop
./.config/xfce4/desktop/accels.scm
./.config/xfce4/desktop/icons.screen0.yaml
./.config/xfce4/panel
./.config/xfce4/panel/launcher-7
./.config/xfce4/panel/launcher-7/17587302031.desktop
./.config/xfce4/panel/launcher-20
./.config/xfce4/panel/launcher-20/17587302032.desktop
./.config/xfce4/panel/launcher-17
./.config/xfce4/panel/launcher-17/17587302033.desktop
./.config/xfce4/panel/launcher-13
./.config/xfce4/panel/launcher-13/17587302034.desktop
./.config/xfce4/panel/launcher-14
./.config/xfce4/panel/launcher-14/17587302035.desktop
./.config/xfce4/panel/launcher-18
./.config/xfce4/panel/launcher-18/17587302036.desktop
./.config/Thunar
./.config/Thunar/uca.xml
./.config/Thunar/accels.scm
./.config/wireshark
./.config/wireshark/profiles
./.config/wireshark/recent
./.config/wireshark/recent_common
./.config/ghidra
./.config/ghidra/ghidra_11.3.2_NIX
./.config/ghidra/ghidra_11.3.2_NIX/java_home.save
./.config/ghidra/ghidra_11.3.2_NIX/application.log
./.config/ghidra/ghidra_11.3.2_NIX/script.log
./.config/ghidra/ghidra_11.3.2_NIX/preferences
./.config/dconf
./.config/dconf/user
./.local
./.local/share
./.local/share/code-server
./.local/share/code-server/coder-logs
./.local/share/code-server/coder-logs/code-server-stdout.log
./.local/share/code-server/coder-logs/code-server-stderr.log
./.local/share/code-server/heartbeat
./.local/share/code-server/User
./.local/share/code-server/User/globalStorage
./.local/share/code-server/User/globalStorage/storage.json
./.local/share/code-server/User/History
./.local/share/code-server/User/snippets
./.local/share/code-server/User/machineid
./.local/share/code-server/User/customBuiltinExtensionsCache.json
./.local/share/code-server/User/systemExtensionsCache.json
./.local/share/code-server/Machine
./.local/share/code-server/logs
./.local/share/code-server/logs/20250924T160839
./.local/share/code-server/logs/20250924T160839/remoteagent.log
./.local/share/code-server/logs/20250924T160839/network.log
./.local/share/code-server/logs/20250924T160839/exthost1
./.local/share/code-server/logs/20250924T160839/exthost1/remoteexthost.log
./.local/share/code-server/logs/20250924T160839/exthost1/vscode.git
./.local/share/code-server/logs/20250924T160839/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20250924T160839/exthost1/vscode.github
./.local/share/code-server/logs/20250924T160839/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20250924T160839/ptyhost.log
./.local/share/code-server/logs/20250924T160959
./.local/share/code-server/logs/20250924T160959/remoteagent.log
./.local/share/code-server/logs/20250924T160959/network.log
./.local/share/code-server/coder.json
./.local/share/code-server/CachedProfilesData
./.local/share/code-server/CachedProfilesData/__default__profile__
./.local/share/code-server/CachedProfilesData/__default__profile__/extensions.builtin.cache
./.local/share/code-server/CachedProfilesData/__default__profile__/extensions.user.cache
./.local/share/code-server/code-server-ipc.sock
./.cache
./.cache/Microsoft
./.cache/Microsoft/DeveloperTools
./.cache/Microsoft/DeveloperTools/deviceid
./.cache/sessions
./.cache/fontconfig
./.cache/fontconfig/CACHEDIR.TAG
./.cache/fontconfig/8da3a4a6e298214e11fec7992269df72-x86_64.cache-9
./.cache/fontconfig/91e6fd8df8eae133e8cc910311cd171d-x86_64.cache-9
./.cache/fontconfig/59fe905d471e974f8569b4c68e40c0bc-x86_64.cache-9
./.cache/fontconfig/111d16ad01ec7e96a1fc2ee34d740d2d-x86_64.cache-9
./.cache/fontconfig/2dd34e4edf77becb7027cbd7211848f3-x86_64.cache-9
./.cache/fontconfig/2d3c4120bdd17ba2468f8e780c7e02a5-x86_64.cache-9
./.cache/fontconfig/e7e594e6ae9c68bbd207f7467d0da23a-x86_64.cache-9
./.cache/fontconfig/4c599c202bc5c08e2d34565a40eac3b2-x86_64.cache-9
./.cache/fontconfig/3830d5c3ddfd5cd38a049b759396e72e-x86_64.cache-9
./.cache/fontconfig/573ec803664ed168555e0e8b6d0f0c7f-x86_64.cache-9
./.cache/fontconfig/7ef2298fde41cc6eeb7af42e48b7d293-x86_64.cache-9
./.cache/fontconfig/d0972c3d32f097851eb916381fc38920-x86_64.cache-9
./.cache/fontconfig/d589a48862398ed80a3d6066f4f56f4c-x86_64.cache-9
./.cache/fontconfig/c57959a16110560c8d0fcea73374aeeb-x86_64.cache-9
./.cache/fontconfig/de156ccd2eddbdc19d37a45b8b2aac9c-x86_64.cache-9
./.cache/dconf
./.cache/dconf/user
./.cache/mozilla
./.cache/mozilla/firefox
./.cache/mozilla/firefox/736gzby4.default
./.cache/mozilla/firefox/736gzby4.default/startupCache
./.cache/mozilla/firefox/736gzby4.default/startupCache/startupCache.8.little
./.cache/mozilla/firefox/736gzby4.default/startupCache/scriptCache-child-current.bin
./.cache/mozilla/firefox/736gzby4.default/startupCache/urlCache-current.bin
./.cache/mozilla/firefox/736gzby4.default/startupCache/scriptCache-current.bin
./.cache/mozilla/firefox/736gzby4.default/startupCache/webext.sc.lz4
./.cache/mozilla/firefox/736gzby4.default/startupCache/urlCache.bin
./.cache/mozilla/firefox/736gzby4.default/startupCache/scriptCache.bin
./.cache/mozilla/firefox/736gzby4.default/startupCache/scriptCache-child.bin
./.cache/mozilla/firefox/736gzby4.default/cache2
./.cache/mozilla/firefox/736gzby4.default/cache2/entries
./.cache/mozilla/firefox/736gzby4.default/cache2/entries/0EDDF8C091E2FED62E44BEDDDC1723F5BF38FE4F
./.cache/mozilla/firefox/736gzby4.default/cache2/entries/F18D85F52EBBBA2AB081EF739ED0D6E8A76D497C
./.cache/mozilla/firefox/736gzby4.default/cache2/entries/D0F48A0632B6C451791F4257697E861961F06A6F
./.cache/mozilla/firefox/736gzby4.default/cache2/ce_T151c2VyQ29udGV4dElkPTUs
./.cache/mozilla/firefox/736gzby4.default/cache2/ce_T151c2VyQ29udGV4dElkPTUsYSw=
./.cache/mozilla/firefox/736gzby4.default/cache2/trash1002825834
./.cache/mozilla/firefox/736gzby4.default/cache2/trash1002825834/451572020
./.cache/mozilla/firefox/736gzby4.default/cache2/trash1002825834/1432078970
./.cache/mozilla/firefox/736gzby4.default/cache2/trash1002825834/140939982
./.cache/mozilla/firefox/736gzby4.default/cache2/trash1002825834/388248340
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed/1083846229
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed/991169062
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed/1911655209
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed/1078113268
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed/2058913635
./.cache/mozilla/firefox/736gzby4.default/cache2/doomed/609933416
./.cache/mozilla/firefox/736gzby4.default/safebrowsing
./.cache/mozilla/firefox/736gzby4.default/safebrowsing/google4
./.cache/mozilla/firefox/736gzby4.default/thumbnails
./.cache/mozilla/firefox/736gzby4.default/activity-stream.discovery_stream.json
./.cache/mozilla/firefox/736gzby4.default/activity-stream.weather_feed.json
./.cache/mozilla/firefox/736gzby4.default/activity-stream.inferred_personalization_feed.json
./.cache/.pwntools-cache-3.12
./.cache/.pwntools-cache-3.12/update
./.cache/thumbnails
./.cache/thumbnails/normal
./.cache/thumbnails/normal/b8314d511ba7f1257d55ce44ded156c4.png
./.cache/thumbnails/normal/63b4ec38cafdfe55cd96946508082192.png
./.cache/thumbnails/normal/ad0a2bde94f72b3e6d335ce4c4365ba3.png
./Desktop
./.mozilla
./.mozilla/firefox
./.mozilla/firefox/Crash Reports
./.mozilla/firefox/Crash Reports/events
./.mozilla/firefox/Crash Reports/InstallTime20250717180000
./.mozilla/firefox/Crash Reports/crash_helper_server.log
./.mozilla/firefox/Pending Pings
./.mozilla/firefox/736gzby4.default
./.mozilla/firefox/736gzby4.default/times.json
./.mozilla/firefox/736gzby4.default/.parentlock
./.mozilla/firefox/736gzby4.default/minidumps
./.mozilla/firefox/736gzby4.default/crashes
./.mozilla/firefox/736gzby4.default/crashes/events
./.mozilla/firefox/736gzby4.default/compatibility.ini
./.mozilla/firefox/736gzby4.default/cookies.sqlite
./.mozilla/firefox/736gzby4.default/storage.sqlite
./.mozilla/firefox/736gzby4.default/storage
./.mozilla/firefox/736gzby4.default/storage/ls-archive.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/.metadata-v2
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/3870112724rsegmnoittet-es.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/3870112724rsegmnoittet-es.sqlite-wal
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/3870112724rsegmnoittet-es.files
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/3561288849sdhlie.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/3561288849sdhlie.sqlite-wal
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/3561288849sdhlie.files
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/1451318868ntouromlalnodry--epcr.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/1451318868ntouromlalnodry--epcr.sqlite-wal
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/1451318868ntouromlalnodry--epcr.files
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/2918063365piupsah.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/2918063365piupsah.sqlite-wal
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/2918063365piupsah.files
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/1657114595AmcateirvtiSty.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/1657114595AmcateirvtiSty.sqlite-wal
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/1657114595AmcateirvtiSty.files
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/2823318777ntouromlalnodry--naod.sqlite
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/2823318777ntouromlalnodry--naod.sqlite-wal
./.mozilla/firefox/736gzby4.default/storage/permanent/chrome/idb/2823318777ntouromlalnodry--naod.files
./.mozilla/firefox/736gzby4.default/storage/temporary
./.mozilla/firefox/736gzby4.default/storage/default
./.mozilla/firefox/736gzby4.default/pkcs11.txt
./.mozilla/firefox/736gzby4.default/cert9.db
./.mozilla/firefox/736gzby4.default/key4.db
./.mozilla/firefox/736gzby4.default/security_state
./.mozilla/firefox/736gzby4.default/permissions.sqlite
./.mozilla/firefox/736gzby4.default/extension-store
./.mozilla/firefox/736gzby4.default/bounce-tracking-protection.sqlite
./.mozilla/firefox/736gzby4.default/content-prefs.sqlite
./.mozilla/firefox/736gzby4.default/places.sqlite
./.mozilla/firefox/736gzby4.default/favicons.sqlite
./.mozilla/firefox/736gzby4.default/favicons.sqlite-wal
./.mozilla/firefox/736gzby4.default/places.sqlite-wal
./.mozilla/firefox/736gzby4.default/bookmarkbackups
./.mozilla/firefox/736gzby4.default/datareporting
./.mozilla/firefox/736gzby4.default/datareporting/state.json
./.mozilla/firefox/736gzby4.default/datareporting/session-state.json
./.mozilla/firefox/736gzby4.default/datareporting/archived
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09/1758730254125.e89cee4f-3203-49f4-a3fa-32147726ae12.new-profile.jsonlz4
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09/1758730254130.2ef77ad8-1f8b-476d-abed-d3fe6d6a8434.event.jsonlz4
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09/1758730254139.6194caf1-a29b-4047-a3f7-8f4ba5ec7bcb.main.jsonlz4
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09/1758730254142.f096589c-36e2-4422-8dab-865f72d6fe38.first-shutdown.jsonlz4
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09/1758730295104.0cb681d7-9dec-49b7-90d4-9eb71630c2db.event.jsonlz4
./.mozilla/firefox/736gzby4.default/datareporting/archived/2025-09/1758730295109.a0e69e55-5299-41a4-871a-f27e0ca156f5.main.jsonlz4
./.mozilla/firefox/736gzby4.default/datareporting/glean
./.mozilla/firefox/736gzby4.default/datareporting/glean/events
./.mozilla/firefox/736gzby4.default/datareporting/glean/events/events
./.mozilla/firefox/736gzby4.default/datareporting/glean/db
./.mozilla/firefox/736gzby4.default/datareporting/glean/db/data.safe.bin
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/b3b2347b-d768-4749-87ee-6043fd23ca5a
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/0b3c5488-8f39-49ae-bf0b-d5dbfae28eff
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/cc83b83d-eedd-475c-8189-ffef64f05a91
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/e1bbb910-e060-439f-afb3-f00d1af287af
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/b706003c-d925-40c1-9930-176ee9d2fe2e
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/83ab5463-b711-493b-888f-585d74cca98d
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/0bfdd676-f782-4d75-b543-9a7204c62b8c
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/fb7011c2-5725-4740-8da5-14783860868c
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/b974b820-8dfa-45a4-bf4e-2524d6d129e5
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/3f9dbdb7-5e91-4dd3-b3ce-3d0f88f657dc
./.mozilla/firefox/736gzby4.default/datareporting/glean/pending_pings/7d65fe73-a984-4a77-869e-dc3716d07348
./.mozilla/firefox/736gzby4.default/datareporting/glean/tmp
./.mozilla/firefox/736gzby4.default/addons.json
./.mozilla/firefox/736gzby4.default/domain_to_categories.sqlite
./.mozilla/firefox/736gzby4.default/domain_to_categories.sqlite-journal
./.mozilla/firefox/736gzby4.default/addonStartup.json.lz4
./.mozilla/firefox/736gzby4.default/extension-preferences.json
./.mozilla/firefox/736gzby4.default/shield-preference-experiments.json
./.mozilla/firefox/736gzby4.default/sessionstore-backups
./.mozilla/firefox/736gzby4.default/sessionstore-backups/previous.jsonlz4
./.mozilla/firefox/736gzby4.default/sessionstore-backups/upgrade.jsonlz4-20250717180000
./.mozilla/firefox/736gzby4.default/containers.json
./.mozilla/firefox/736gzby4.default/handlers.json
./.mozilla/firefox/736gzby4.default/protections.sqlite
./.mozilla/firefox/736gzby4.default/webappsstore.sqlite
./.mozilla/firefox/736gzby4.default/webappsstore.sqlite-wal
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings/e89cee4f-3203-49f4-a3fa-32147726ae12
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings/2ef77ad8-1f8b-476d-abed-d3fe6d6a8434
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings/6194caf1-a29b-4047-a3f7-8f4ba5ec7bcb
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings/f096589c-36e2-4422-8dab-865f72d6fe38
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings/0cb681d7-9dec-49b7-90d4-9eb71630c2db
./.mozilla/firefox/736gzby4.default/saved-telemetry-pings/a0e69e55-5299-41a4-871a-f27e0ca156f5
./.mozilla/firefox/736gzby4.default/lock
./.mozilla/firefox/736gzby4.default/cookies.sqlite-wal
./.mozilla/firefox/736gzby4.default/search.json.mozlz4
./.mozilla/firefox/736gzby4.default/formhistory.sqlite
./.mozilla/firefox/736gzby4.default/sessionstore.jsonlz4
./.mozilla/firefox/736gzby4.default/settings
./.mozilla/firefox/736gzby4.default/extensions.json
./.mozilla/firefox/736gzby4.default/prefs.js
./.mozilla/firefox/736gzby4.default/xulstore.json
./.mozilla/firefox/736gzby4.default/sessionCheckpoints.json
./.mozilla/firefox/profiles.ini
./.mozilla/firefox/Profile Groups
./.mozilla/firefox/Profile Groups/bde1d5a6.sqlite
./.mozilla/firefox/Profile Groups/bde1d5a6.sqlite-wal
./.mozilla/firefox/Profile Groups/bde1d5a6.sqlite-shm
./.mozilla/extensions
./Downloads
./.java
./.java/fonts
./.java/fonts/21.0.7
./.java/fonts/21.0.7/fcinfo-1-welcome~getting-help-debian-12-en-US.properties
./.dbus
./.dbus/session-bus
./.dbus/session-bus/beaa6870143341099de48fb979405e74-0
./.dbus/session-bus/f7d2a8a818fc4c9fb4442f20f2c39e9b-0
./.bash_history
./a
./core
./.ICEauthority
hacker@commands~finding-files:~$ find -name flag
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/doc/libxau6/flag
^C
hacker@commands~finding-files:~$ ls -a /root
ls: cannot open directory '/root': Permission denied
hacker@commands~finding-files:~$ cat /usr/share/doc/libxau6/flag
pwn.college{k-az0Cqw-XLxgLctB-yi6c_tFw4.QXyMDO0wSOzEzNzEzW}hacker@commands~finding-files:~$ ^C
hacker@commands~finding-files:~$ 
```

The find command is used to find the files named flag

## What I learned
I learned how to navigate through files using the find command



