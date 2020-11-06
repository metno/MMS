# Command line framework
We pick urfave/cli as a framework due to simpler design. If needed we can switch to spf13/cobra when we see the need, there are some good arguments for using it:
https://www.reddit.com/r/golang/comments/5sdvoh/what_is_the_essential_difference_between/

# Command line syntax

We pick nr. 1 (redis inspired) as it is explicit and gives least complexity of possible combinations.

nr. 1 redis inspired
```
mms list-production-hubs
mms list-events
mms subscribe-events
mms post-event --from-file=<blurgH>
mms post-event --data='{"name": "Arome Arctic"}'
```

nr. 2 kubectl inspired
```
mms list events
mms list production-hubs
```

nr. 3 azure and openstack inspired
```
mms events list
mms production-hub subscribe
```