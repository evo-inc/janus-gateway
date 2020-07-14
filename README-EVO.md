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

Changes we keep as of Jul 2020:
1. Support for domain names in TURN API response (ip-utils.c; commits d996658 b48fb20 71df9ee)
2. Libmicrohttpd debug logs (transports/janus_http.c)
3. Talkback using u-law over data channel (configure.ac, janus_streaming.c, sctp.c; commits 25c6518 a89bb60)
4. Handle old GCC issue (version.h)
5. RTCP timeout (commit 99718e8).
TODO:
1. Fix REST API use by apps. Currently we can only stream if we set up using RMQ.
