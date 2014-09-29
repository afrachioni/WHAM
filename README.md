This is a modified copy of version 2.0.9 of Alan Grossfield's implementation of the Weighted Histogram Analysis Method (see [http://membrane.urmc.rochester.edu/content/wham]).

For any timeseries file named in the metadata file, with a name ending in `.hist`, an alternate file parsing routine is used.  Rather than the existing method of specifying one sample per line, each line now specifies the population of one histogram bin.  The first whitespace-delimited column represents the bin indices, and the second represents the counts.  No particular order is required, and unspecified bins are set to zero counts.  Additional columns are ignored.  The histogram limits and bin count are passed as command line arguments, exactly as before.

Histogram reading is not yet implemented for two dimensional WHAM.
