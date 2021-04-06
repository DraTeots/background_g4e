Documentation:

[How to run on farms with Spack](https://escalate.readthedocs.io/en/latest/300_farms.html)


```sh
ifarm1802.jlab.org> source /cvmfs/eic.opensciencegrid.org/packages/setup-env.csh 
ifarm1802.jlab.org> spack load /ef7rk23
```

Group installation (Alternative to previous):

```sh
> source /group/eic/escalate/escalate/escalate.csh
> (esc) ifarm1901.jlab.org> g4e
g4e - Geant 4 Electron Ion Collider - is a full simulation part of ESCalate framework.

There is no macro files provided. Please look at $G4E_HOME/examples folder macros examples or how to run g4e from python
You can get more help here: 
https://g4e.readthedocs.io/
https://geant4.web.cern.ch/

```

## Run G4E

```sh
(esc) ifarm1901.jlab.org> mkdir rung4e
(esc) ifarm1901.jlab.org> cp $G4E_HOME/examples/* rung4e/
(esc) ifarm1901.jlab.org> cd rung4e/
(esc) ifarm1901.jlab.org> g4e --gui cone_pgun_ip6_vis.mac
ifarm1801.jlab.org> ls -latrh
total 679K
-rw-r--r--  1 romanov ENP  783 Apr  5 14:57 beagle.mac
-rw-r--r--  1 romanov ENP  284 Apr  5 14:57 build_g4e.py
-rw-r--r--  1 romanov ENP  190 Apr  5 14:57 check_overlaps.py
-rw-r--r--  1 romanov ENP 2.4K Apr  5 14:57 cone_particle_gun.py
-rw-r--r--  1 romanov ENP 2.7K Apr  5 14:57 cone_particle_gun_vis.py
-rw-r--r--  1 romanov ENP 3.6K Apr  5 14:57 cone_pgun_ip6_vis.mac
-rw-r--r--  1 romanov ENP 3.7K Apr  5 14:57 cone_pgun_ip8_vis.mac
-rw-r--r--  1 romanov ENP  120 Apr  5 14:57 event_display.py
-rw-r--r--  1 romanov ENP 1.3K Apr  5 14:57 g4e_simulation.py
-rw-r--r--  1 romanov ENP  909 Apr  5 14:57 herwig.mac
-rw-r--r--  1 romanov ENP  705 Apr  5 14:57 pythia.mac
-rw-r--r--  1 romanov ENP  582 Apr  5 14:57 simple_commands.py
-rw-r--r--  1 romanov ENP  281 Apr  5 14:57 simple_run_ip8.py
-rw-r--r--  1 romanov ENP  262 Apr  5 14:57 simple_run.py
-rw-r--r--  1 romanov ENP 4.8K Apr  5 14:57 vis_beampipe_only.mac
-rw-r--r--  1 romanov ENP 4.5K Apr  5 14:57 vis_ce_emcal.py
-rw-r--r--  1 romanov ENP 4.8K Apr  5 14:57 vis_drich_only.mac
-rw-r--r--  1 romanov ENP 1.8K Apr  5 14:57 vis_new.mac
-rw-r--r--  1 romanov ENP 1.5K Apr  5 14:57 vis.run.mac
-rw-r--r--  1 romanov ENP  602 Apr  5 15:10 g4e_output.geo.root
drwx------ 72 romanov ENP 4.0K Apr  5 15:12 ..
-rw-r--r--  1 romanov ENP   29 Apr  5 15:14 g4e_output.bgn.rndm
drwxr-xr-x  2 romanov ENP  788 Apr  5 15:21 .
-rw-r--r--  1 romanov ENP   29 Apr  5 15:21 g4e_output.end.rndm
-rw-r--r--  1 romanov ENP 8.5K Apr  5 15:21 g4e_output.root
```

## More documentation

[g4e.readthedocs.io](g4e.readthedocs.io)

[build on your machine](https://escalate.readthedocs.io/projects/g4e/en/latest/01_install.html#cmake-build)

[Root output format](https://escalate.readthedocs.io/projects/g4e/en/latest/root_output.html)

Visualization Cone particle gun on ip6:

```
g4e --gui /home/romanov/eic/soft/g4e/g4e-dev/examples/cone_pgun_ip6_vis.mac
```
