As I've been playing around with dual-booting Linux and Windows in the past, I managed to get my system into a state where I had [Windows](intro.md) on one drive and the [Windows Boot Manager](boot-manager.md) on another drive.

The problem with this, is if you want to reclaim the entirety of the old drive's space you're not really able to as one of the partitions on it is required for Windows to boot.

`diskmgmt` won't allow you to delete the partition at all if it thinks there's some sort of Windows installation on there.
