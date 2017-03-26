This role handles up to 8 EC2 ephemeral disks. For use on Ubuntu only as it uses the /dev/xvdb syntax for mount points.
All disks are added to a ZFS pool. Role would need additional options if you wanted to do more than add disks to a single pool and
let ZFS stripe it and add a filesystem as it does by default - but its purpose is simply to aggregate all ephemeral disks present
into a usable volume via the simplest means possible.
