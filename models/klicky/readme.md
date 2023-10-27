Ender 7 Klicky Z probe 

You will need to be running klipper (see the config files, your park position will be around 5mm further on the X than mine - I broke my X endstop and replaced it with a larger one, so I lose about 5mm on X)
Uses 5mm by 1.5mm magnets (6), magnets are either press fit or super glued (press is better as the glue can effect the electrical contact)
The microswitch is NC (normally closed) - so can be wired in series with the existing endstop.
The dock mounts on the right pillar and is adjustable (up and down), when mounting the dock:
* move the gantry by hand to get the dock hieght adjustment correct.
* Adjust the height on the pillar so the probe lifts slightly to make contact with the probe mount (this helps it overcome the magnetic force of the pillar as it moves away).
* The probe can either be wired in series with the existing end stop or completely replace it.
* When working out the dock position - before updating the klipper config home your z axis by manually triggering the endstop with your finger (with the build plate down the build volume to give you some room).
* Using the manual x,y movement buttons align the pickup with the entrance to the dock and record the position
* The pickup probe is multi step (to try and avoid colisions) we want the probe to move to the dock entry first, then slowly move the X to pickup, then move the X back out again.
* Docking is similar, where it moves to the dock entry, then slowy moves X into the dock position, by instead of moving X away, move Y away (towards the front, if you move towards the back the fans will colide with the dock)
* in the klicky.cfg adjust the X,Y positions of the probe_out and probe_in
* in klicky.cfg ajust the [probe] z_offset, about 1.7 would be a good starting point but you will need to adjust it (I don't know an easy way of doing it, other than making micro adjustments until it is correct) a higher number brings the nozzle closer to the bed, and a lower number brings it further away.
