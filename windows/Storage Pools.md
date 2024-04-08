These are a pretty straight forward way of collapsing multiple drives into a single "pool" of data - in a similar way to how ZFS works.

The UI is very straight forward, and if you have a series of empty drives that are identical it just makes sense (at least to use the simple scenario).

Do note, you're going to lose _some_ storage space in the process, since a portion of the pool needs to be kept back for actually handling the pool itself etc.

## Gotchas

I've seen it where a drive is not able to be added to the pool due to an error surrounding the cluster size.

People on the internet suggest to increase that, but when I went to format the drive with a different block size it was still unable to be added to the pool.