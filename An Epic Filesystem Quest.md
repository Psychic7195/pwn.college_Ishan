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


