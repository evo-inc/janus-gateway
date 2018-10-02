To get upstream's changes:
```
$ git clone git@github.com:evo-inc/janus-gateway
$ cd janus-gateway
$ git remote add upstream git@github.com:meetecho/janus-gateway
$ git fetch upstream
$ git checkout --track origin/evo-dev
$ git merge upstream/master OR git merge [tag]
```
Fix conflicts

To see the original change set:
`$ git diff 90fa6b6 71df9ee`

Changes we have dropped as of 20 Sep 2018:
 - sdeslen in `ice.c`, upstream fixed this
 - cnamelen in `rtcp.c`, upstream fixed this
 - logs in `utils.c`

Changes we keep as of 20 Sep 2018:
 - add name resolution to `janus_network_string_to_address` in `ip-utils.c`
 - add `set_tokens` in `janus.c`
 - add SEI/SPS/PPS, `last_received_rtcp`, `janus_streaming_stop`, `janus_streaming_send_event`, stopping on timeout in `janus_streaming_relay_rtp_packet`, `janus_streaming_is_nal_type` in `plugins/janus_streaming.c`
 - error logs to libmicrohttpd in `transports/janus_http.c`
 
