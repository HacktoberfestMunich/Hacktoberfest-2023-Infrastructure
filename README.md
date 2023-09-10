# Hacktoberfest-2023-Infrastructure

This is the infrastructure of the Crazy Canvas Challenges at Hacktoberfest 2023.

## Notes

To make sure the participants can only test with the test pixelflut server and not the challenge one a iptable rule needs to be applied.
This will block the port `1234` from the outside of `localhost`.
Since the challenges are all communicating from inside the host, this is fine.

The command for that:

```shell
iptables -I INPUT --proto tcp --dport 1234 -j REJECT
```
