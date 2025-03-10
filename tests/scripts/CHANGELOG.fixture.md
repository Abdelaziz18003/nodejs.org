# Node.js v4 ChangeLog

<table>
<tr>
<th>LTS 'Argon'</th>
<th>Stable</th>
</tr>
<tr>
<td valign="top">
<a href="#4.4.4">4.4.4</a><br/>
<a href="#4.4.3">4.4.3</a><br/>
<a href="#4.4.2">4.4.2</a><br/>
<a href="#4.4.1">4.4.1</a><br/>
<a href="#4.4.0">4.4.0</a><br/>
<a href="#4.3.2">4.3.2</a><br/>
<a href="#4.3.1">4.3.1</a><br/>
<a href="#4.3.0">4.3.0</a><br/>
<a href="#4.2.6">4.2.6</a><br/>
<a href="#4.2.5">4.2.5</a><br/>
<a href="#4.2.4">4.2.4</a><br/>
<a href="#4.2.3">4.2.3</a><br/>
<a href="#4.2.2">4.2.2</a><br/>
<a href="#4.2.1">4.2.1</a><br/>
<a href="#4.2.0">4.2.0</a><br/>
</td>
<td valign="top">
<a href="#4.1.2">4.1.2</a><br/>
<a href="#4.1.1">4.1.1</a><br/>
<a href="#4.1.0">4.1.0</a><br/>
<a href="#4.0.0">4.0.0</a><br/>
</td>
</tr>
</table>

* Other Versions
  * [6.x](CHANGELOG_V6.md)
  * [5.x](CHANGELOG_V5.md)
  * [0.12.x](CHANGELOG_V012.md)
  * [0.10.x](CHANGELOG_V010.md)
  * [io.js](CHANGELOG_IOJS.md)
  * [Archive](CHANGELOG_ARCHIVE.md)

**Note:** Node.js v4 is covered by the
[Node.js Long Term Support Plan](https://github.com/nodejs/LTS) and
will be supported actively until April 2017 and maintained until April 2018.

<a id="4.4.4"></a>
## 2016-05-05, Version 4.4.4 'Argon' (LTS), @thealphanerd

### Notable changes

* **deps**:
  * update openssl to 1.0.2h. (Shigeki Ohtsu) [#6551](https://github.com/nodejs/node/pull/6551)
    - Please see our [blog post](https://nodejs.org/en/blog/vulnerability/openssl-may-2016/) for more info on the security contents of this release.

### Commits

* [[`f46952e727`](https://github.com/nodejs/node/commit/f46952e727)] - **buffer**: safeguard against accidental kNoZeroFill (Сковорода Никита Андреевич) [nodejs/node-private#30](https://github.com/nodejs/node-private/pull/30)
* [[`4f1c82f995`](https://github.com/nodejs/node/commit/4f1c82f995)] - **streams**: support unlimited synchronous cork/uncork cycles (Matteo Collina) [#6164](https://github.com/nodejs/node/pull/6164)
* [[`1efd96c767`](https://github.com/nodejs/node/commit/1efd96c767)] - **deps**: update openssl asm and asm_obsolete files (Shigeki Ohtsu) [#6551](https://github.com/nodejs/node/pull/6551)
* [[`c450f4a293`](https://github.com/nodejs/node/commit/c450f4a293)] - **deps**: add -no_rand_screen to openssl s_client (Shigeki Ohtsu) [nodejs/io.js#1836](https://github.com/nodejs/io.js/pull/1836)
* [[`baedfbae6a`](https://github.com/nodejs/node/commit/baedfbae6a)] - **openssl**: fix keypress requirement in apps on win32 (Shigeki Ohtsu) [iojs/io.js#1389](https://github.com/iojs/io.js/pull/1389)
* [[`ff3045e40b`](https://github.com/nodejs/node/commit/ff3045e40b)] - **deps**: fix asm build error of openssl in x86_win32 (Shigeki Ohtsu) [iojs/io.js#1389](https://github.com/iojs/io.js/pull/1389)
* [[`dc8dc97db3`](https://github.com/nodejs/node/commit/dc8dc97db3)] - **deps**: fix openssl assembly error on ia32 win32 (Fedor Indutny) [iojs/io.js#1389](https://github.com/iojs/io.js/pull/1389)
* [[`2dfeb01213`](https://github.com/nodejs/node/commit/2dfeb01213)] - **deps**: copy all openssl header files to include dir (Shigeki Ohtsu) [#6551](https://github.com/nodejs/node/pull/6551)
* [[`72f9952516`](https://github.com/nodejs/node/commit/72f9952516)] - **deps**: upgrade openssl sources to 1.0.2h (Shigeki Ohtsu) [#6551](https://github.com/nodejs/node/pull/6551)

<a id="4.4.3"></a>
## 2016-04-12, Version 4.4.3 'Argon' (LTS), @thealphanerd

### Notable Changes

* **deps**:
  - Fix `--gdbjit` for embedders. Backported from v8 upstream. (Ben Noordhuis) [#5577](https://github.com/nodejs/node/pull/5577)
* **etw**:
  - Correctly display descriptors for ETW events 9 and 23 on the windows platform. (João Reis) [#5742](https://github.com/nodejs/node/pull/5742)
* **querystring**:
  - Restore throw when attempting to stringify bad surrogate pair. (Brian White) [#5858](https://github.com/nodejs/node/pull/5858)

### Commits

* [[`f949c273cd`](https://github.com/nodejs/node/commit/f949c273cd)] - **assert**: Check typed array view type in deepEqual (Anna Henningsen) [#5910](https://github.com/nodejs/node/pull/5910)
* [[`132acea0d4`](https://github.com/nodejs/node/commit/132acea0d4)] - **build**: introduce ci targets for lint/benchmark (Johan Bergström) [#5921](https://github.com/nodejs/node/pull/5921)
* [[`9a8f922dee`](https://github.com/nodejs/node/commit/9a8f922dee)] - **build**: add missing `openssl_fips%` to common.gypi (Fedor Indutny) [#5919](https://github.com/nodejs/node/pull/5919)
* [[`d275cdf202`](https://github.com/nodejs/node/commit/d275cdf202)] - **child_process**: refactor self=this in socket_list (Benjamin Gruenbaum) [#5860](https://github.com/nodejs/node/pull/5860)
* [[`aadf356aa2`](https://github.com/nodejs/node/commit/aadf356aa2)] - **deps**: backport 8d00c2c from v8 upstream (Ben Noordhuis) [#5577](https://github.com/nodejs/node/pull/5577)
* [[`200f763c43`](https://github.com/nodejs/node/commit/200f763c43)] - **deps**: completely upgrade npm in LTS to 2.15.1 (Forrest L Norvell) [#5989](https://github.com/nodejs/node/pull/5989)
* [[`86e3903626`](https://github.com/nodejs/node/commit/86e3903626)] - **dns**: Use object without protoype for map (Benjamin Gruenbaum) [#5843](https://github.com/nodejs/node/pull/5843)
* [[`9a33f43f73`](https://github.com/nodejs/node/commit/9a33f43f73)] - **doc**: update openssl LICENSE using license-builder.sh (Steven R. Loomis) [#6065](https://github.com/nodejs/node/pull/6065)
* [[`9679e2dc70`](https://github.com/nodejs/node/commit/9679e2dc70)] - **doc**: clarify that __dirname is module local (James M Snell) [#6018](https://github.com/nodejs/node/pull/6018)
* [[`86d2af58d6`](https://github.com/nodejs/node/commit/86d2af58d6)] - **doc**: simple doc typo fix (Brendon Pierson) [#6041](https://github.com/nodejs/node/pull/6041)
* [[`f16802f3ca`](https://github.com/nodejs/node/commit/f16802f3ca)] - **doc**: note about Android support (Rich Trott) [#6040](https://github.com/nodejs/node/pull/6040)
* [[`8c2befe176`](https://github.com/nodejs/node/commit/8c2befe176)] - **doc**: note assert.throws() pitfall (Rich Trott) [#6029](https://github.com/nodejs/node/pull/6029)
* [[`0870ac65f2`](https://github.com/nodejs/node/commit/0870ac65f2)] - **doc**: use HTTPS for links where possible (Rich Trott) [#6019](https://github.com/nodejs/node/pull/6019)
* [[`56755de96e`](https://github.com/nodejs/node/commit/56755de96e)] - **doc**: clarify stdout/stderr arguments to callback (James M Snell) [#6015](https://github.com/nodejs/node/pull/6015)
* [[`bb603b89a2`](https://github.com/nodejs/node/commit/bb603b89a2)] - **doc**: add 'Command Line Options' to 'View on single page' (firedfox) [#6011](https://github.com/nodejs/node/pull/6011)
* [[`c91f3d897a`](https://github.com/nodejs/node/commit/c91f3d897a)] - **doc**: add copy about how to curl SHA256.txt (Myles Borins) [#6120](https://github.com/nodejs/node/pull/6120)
* [[`f9cf232284`](https://github.com/nodejs/node/commit/f9cf232284)] - **doc**: add example using algorithms not directly exposed (Brad Hill) [#6108](https://github.com/nodejs/node/pull/6108)
* [[`f60ce1078d`](https://github.com/nodejs/node/commit/f60ce1078d)] - **doc**: document unspecified behavior for buf.write* methods (James M Snell) [#5925](https://github.com/nodejs/node/pull/5925)
* [[`02401a6cbd`](https://github.com/nodejs/node/commit/02401a6cbd)] - **doc**: fix scrolling on iOS devices (Luigi Pinca) [#5878](https://github.com/nodejs/node/pull/5878)
* [[`aed22d0855`](https://github.com/nodejs/node/commit/aed22d0855)] - **doc**: path.format provide more examples (John Eversole) [#5838](https://github.com/nodejs/node/pull/5838)
* [[`6e2bfbe1fd`](https://github.com/nodejs/node/commit/6e2bfbe1fd)] - **doc**: fix doc for Buffer.readInt32LE() (ghaiklor) [#5890](https://github.com/nodejs/node/pull/5890)
* [[`940d204401`](https://github.com/nodejs/node/commit/940d204401)] - **doc**: consolidate timers docs in timers.markdown (Bryan English) [#5837](https://github.com/nodejs/node/pull/5837)
* [[`505faf6360`](https://github.com/nodejs/node/commit/505faf6360)] - **doc**: refine child_process detach behaviour (Robert Jefe Lindstaedt) [#5330](https://github.com/nodejs/node/pull/5330)
* [[`feedca7879`](https://github.com/nodejs/node/commit/feedca7879)] - **doc**: add topic - event loop, timers, `nextTick()` (Jeff Harris) [#4936](https://github.com/nodejs/node/pull/4936)
* [[`6d3822c12b`](https://github.com/nodejs/node/commit/6d3822c12b)] - **etw**: fix descriptors of events 9 and 23 (João Reis) [#5742](https://github.com/nodejs/node/pull/5742)
* [[`56dda6f336`](https://github.com/nodejs/node/commit/56dda6f336)] - **fs**: Remove unused branches (Benjamin Gruenbaum) [#5289](https://github.com/nodejs/node/pull/5289)
* [[`dfe9e157c1`](https://github.com/nodejs/node/commit/dfe9e157c1)] - **governance**: remove target size for CTC (Rich Trott) [#5879](https://github.com/nodejs/node/pull/5879)
* [[`c4103b154f`](https://github.com/nodejs/node/commit/c4103b154f)] - **lib**: refactor code with startsWith/endsWith (Jackson Tian) [#5753](https://github.com/nodejs/node/pull/5753)
* [[`16216a81de`](https://github.com/nodejs/node/commit/16216a81de)] - **meta**: add "joining a wg" section to WORKING_GROUPS.md (Matteo Collina) [#5488](https://github.com/nodejs/node/pull/5488)
* [[`65fc4e36ce`](https://github.com/nodejs/node/commit/65fc4e36ce)] - **querystring**: don't stringify bad surrogate pair (Brian White) [#5858](https://github.com/nodejs/node/pull/5858)
* [[`4f683ab912`](https://github.com/nodejs/node/commit/4f683ab912)] - **src,tools**: use template literals (Rich Trott) [#5778](https://github.com/nodejs/node/pull/5778)
* [[`ac40a4510d`](https://github.com/nodejs/node/commit/ac40a4510d)] - **test**: explicitly set global in test-repl (Rich Trott) [#6026](https://github.com/nodejs/node/pull/6026)
* [[`a7b3a7533a`](https://github.com/nodejs/node/commit/a7b3a7533a)] - **test**: be explicit about polluting of `global` (Rich Trott) [#6017](https://github.com/nodejs/node/pull/6017)
* [[`73e3b7b9a8`](https://github.com/nodejs/node/commit/73e3b7b9a8)] - **test**: make use of globals explicit (Rich Trott) [#6014](https://github.com/nodejs/node/pull/6014)
* [[`e7877e61b6`](https://github.com/nodejs/node/commit/e7877e61b6)] - **test**: fix flaky test-net-socket-timeout-unref (Rich Trott) [#6003](https://github.com/nodejs/node/pull/6003)
* [[`a39051f5b3`](https://github.com/nodejs/node/commit/a39051f5b3)] - **test**: make arch available in status files (Santiago Gimeno) [#5997](https://github.com/nodejs/node/pull/5997)
* [[`ccf90b651a`](https://github.com/nodejs/node/commit/ccf90b651a)] - **test**: fix test-dns.js flakiness (Rich Trott) [#5996](https://github.com/nodejs/node/pull/5996)
* [[`1994ac0912`](https://github.com/nodejs/node/commit/1994ac0912)] - **test**: add test for piping large input from stdin (Anna Henningsen) [#5949](https://github.com/nodejs/node/pull/5949)
* [[`cc1aab9f6a`](https://github.com/nodejs/node/commit/cc1aab9f6a)] - **test**: mitigate flaky test-https-agent (Rich Trott) [#5939](https://github.com/nodejs/node/pull/5939)
* [[`10fe79b809`](https://github.com/nodejs/node/commit/10fe79b809)] - **test**: fix offending max-len linter error (Sakthipriyan Vairamani) [#5980](https://github.com/nodejs/node/pull/5980)
* [[`63d82960fd`](https://github.com/nodejs/node/commit/63d82960fd)] - **test**: stdin is not always a net.Socket (Jeremiah Senkpiel) [#5935](https://github.com/nodejs/node/pull/5935)
* [[`fe0233b923`](https://github.com/nodejs/node/commit/fe0233b923)] - **test**: add known_issues test for GH-2148 (Rich Trott) [#5920](https://github.com/nodejs/node/pull/5920)
* [[`d59be4d248`](https://github.com/nodejs/node/commit/d59be4d248)] - **test**: ensure _handle property existence (Rich Trott) [#5916](https://github.com/nodejs/node/pull/5916)
* [[`9702153107`](https://github.com/nodejs/node/commit/9702153107)] - **test**: fix flaky test-repl (Brian White) [#5914](https://github.com/nodejs/node/pull/5914)
* [[`a0a2e69097`](https://github.com/nodejs/node/commit/a0a2e69097)] - **test**: move dns test to test/internet (Ben Noordhuis) [#5905](https://github.com/nodejs/node/pull/5905)
* [[`8462d8f465`](https://github.com/nodejs/node/commit/8462d8f465)] - **test**: fix flaky test-net-socket-timeout (Brian White) [#5902](https://github.com/nodejs/node/pull/5902)
* [[`e0b283af73`](https://github.com/nodejs/node/commit/e0b283af73)] - **test**: fix flaky test-http-set-timeout (Rich Trott) [#5856](https://github.com/nodejs/node/pull/5856)
* [[`5853fec36f`](https://github.com/nodejs/node/commit/5853fec36f)] - **test**: fix test-debugger-client.js (Rich Trott) [#5851](https://github.com/nodejs/node/pull/5851)
* [[`ea83c382f9`](https://github.com/nodejs/node/commit/ea83c382f9)] - **test**: ensure win32.isAbsolute() is consistent (Brian White) [#6043](https://github.com/nodejs/node/pull/6043)
* [[`c33a23fd1e`](https://github.com/nodejs/node/commit/c33a23fd1e)] - **tools**: fix json doc generation (firedfox) [#5943](https://github.com/nodejs/node/pull/5943)
* [[`6f0bd64122`](https://github.com/nodejs/node/commit/6f0bd64122)] - **tools,doc**: fix incomplete json produced by doctool (firedfox) [#5966](https://github.com/nodejs/node/pull/5966)
* [[`f7eb48302c`](https://github.com/nodejs/node/commit/f7eb48302c)] - **win,build**: build and test add-ons on test-ci (Bogdan Lobor) [#5886](https://github.com/nodejs/node/pull/5886)

<a id="4.4.2"></a>
## 2016-03-31, Version 4.4.2 'Argon' (LTS), @thealphanerd

### Notable Changes

* **https**:
  - Under certain conditions ssl sockets may have been causing a memory leak when keepalive is enabled. This is no longer the case. (Alexander Penev) [#5713](https://github.com/nodejs/node/pull/5713)
* **lib**:
  - The way that we were internally passing arguments was causing a potential leak. By copying the arguments into an array we can avoid this. (Nathan Woltman) [#4361](https://github.com/nodejs/node/pull/4361)
* **npm**:
  - Upgrade to v2.15.1. Fixes a security flaw in the use of authentication tokens in HTTP requests that would allow an attacker to set up a server that could collect tokens from users of the command-line interface. Authentication tokens have previously been sent with every request made by the CLI for logged-in users, regardless of the destination of the request. This update fixes this by only including those tokens for requests made against the registry or registries used for the current install. (Forrest L Norvell)
* **repl**:
  - Previously if you were using the repl in strict mode the column number would be wrong in a stack trace. This is no longer an issue. (Prince J Wesley) [#5416](https://github.com/nodejs/node/pull/5416)

### Commits

* [[`96e163a79f`](https://github.com/nodejs/node/commit/96e163a79f)] - **buffer**: changing let in for loops back to var (Gareth Ellis) [#5819](https://github.com/nodejs/node/pull/5819)
* [[`0c6f6742f2`](https://github.com/nodejs/node/commit/0c6f6742f2)] - **console**: check that stderr is writable (Rich Trott) [#5635](https://github.com/nodejs/node/pull/5635)
* [[`55c3f804c4`](https://github.com/nodejs/node/commit/55c3f804c4)] - **deps**: upgrade npm in LTS to 2.15.1 (Forrest L Norvell)
* [[`1d0e4a987d`](https://github.com/nodejs/node/commit/1d0e4a987d)] - **deps**: remove unused openssl files (Ben Noordhuis) [#5619](https://github.com/nodejs/node/pull/5619)
* [[`d55599f4d8`](https://github.com/nodejs/node/commit/d55599f4d8)] - **dns**: use template literals (Benjamin Gruenbaum) [#5809](https://github.com/nodejs/node/pull/5809)
* [[`42bbdc9dd1`](https://github.com/nodejs/node/commit/42bbdc9dd1)] - **doc** Add @mhdawson back to the CTC (James M Snell) [#5633](https://github.com/nodejs/node/pull/5633)
* [[`8d86d232e7`](https://github.com/nodejs/node/commit/8d86d232e7)] - **doc**: typo: interal->internal. (Corey Kosak) [#5849](https://github.com/nodejs/node/pull/5849)
* [[`60ddab841e`](https://github.com/nodejs/node/commit/60ddab841e)] - **doc**: add instructions to only sign a release (Jeremiah Senkpiel) [#5876](https://github.com/nodejs/node/pull/5876)
* [[`040263e0f3`](https://github.com/nodejs/node/commit/040263e0f3)] - **doc**: grammar, clarity and links in timers doc (Bryan English) [#5792](https://github.com/nodejs/node/pull/5792)
* [[`8c24bd25a6`](https://github.com/nodejs/node/commit/8c24bd25a6)] - **doc**: fix order of end tags of list after heading (firedfox) [#5874](https://github.com/nodejs/node/pull/5874)
* [[`7c837028da`](https://github.com/nodejs/node/commit/7c837028da)] - **doc**: use consistent event name parameter (Benjamin Gruenbaum) [#5850](https://github.com/nodejs/node/pull/5850)
* [[`20faf9097d`](https://github.com/nodejs/node/commit/20faf9097d)] - **doc**: explain error message on missing main file (Wolfgang Steiner) [#5812](https://github.com/nodejs/node/pull/5812)
* [[`79d26ae196`](https://github.com/nodejs/node/commit/79d26ae196)] - **doc**: explain path.format expected properties (John Eversole) [#5801](https://github.com/nodejs/node/pull/5801)
* [[`e43e8e3a31`](https://github.com/nodejs/node/commit/e43e8e3a31)] - **doc**: add a cli options doc page (Jeremiah Senkpiel) [#5787](https://github.com/nodejs/node/pull/5787)
* [[`c0a24e4a1d`](https://github.com/nodejs/node/commit/c0a24e4a1d)] - **doc**: fix multiline return comments in querystring (Claudio Rodriguez) [#5705](https://github.com/nodejs/node/pull/5705)
* [[`bf1fe4693c`](https://github.com/nodejs/node/commit/bf1fe4693c)] - **doc**: Add windows example for Path.format (Mithun Patel) [#5700](https://github.com/nodejs/node/pull/5700)
* [[`3b8fc4fddc`](https://github.com/nodejs/node/commit/3b8fc4fddc)] - **doc**: update crypto docs to use good defaults (Bill Automata) [#5505](https://github.com/nodejs/node/pull/5505)
* [[`a6ec8a6cb7`](https://github.com/nodejs/node/commit/a6ec8a6cb7)] - **doc**: fix crypto update() signatures (Brian White) [#5500](https://github.com/nodejs/node/pull/5500)
* [[`eb0ed46665`](https://github.com/nodejs/node/commit/eb0ed46665)] - **doc**: reformat & improve node.1 manual page (Jeremiah Senkpiel) [#5497](https://github.com/nodejs/node/pull/5497)
* [[`b70ca4a4b4`](https://github.com/nodejs/node/commit/b70ca4a4b4)] - **doc**: updated fs #5862 removed irrelevant data in fs.markdown (topal) [#5877](https://github.com/nodejs/node/pull/5877)
* [[`81876612f7`](https://github.com/nodejs/node/commit/81876612f7)] - **https**: fix ssl socket leak when keepalive is used (Alexander Penev) [#5713](https://github.com/nodejs/node/pull/5713)
* [[`6daebdbd9b`](https://github.com/nodejs/node/commit/6daebdbd9b)] - **lib**: simplify code with String.prototype.repeat() (Jackson Tian) [#5359](https://github.com/nodejs/node/pull/5359)
* [[`108fc90dd7`](https://github.com/nodejs/node/commit/108fc90dd7)] - **lib**: reduce usage of `self = this` (Jackson Tian) [#5231](https://github.com/nodejs/node/pull/5231)
* [[`3c8e59c396`](https://github.com/nodejs/node/commit/3c8e59c396)] - **lib**: copy arguments object instead of leaking it (Nathan Woltman) [#4361](https://github.com/nodejs/node/pull/4361)
* [[`8648420586`](https://github.com/nodejs/node/commit/8648420586)] - **net**: make `isIPv4` and `isIPv6` more efficient (Vladimir Kurchatkin) [#5478](https://github.com/nodejs/node/pull/5478)
* [[`07b7172d76`](https://github.com/nodejs/node/commit/07b7172d76)] - **net**: remove unused `var self = this` from old code (Benjamin Gruenbaum) [#5224](https://github.com/nodejs/node/pull/5224)
* [[`acbce4b72b`](https://github.com/nodejs/node/commit/acbce4b72b)] - **repl**: fix stack trace column number in strict mode (Prince J Wesley) [#5416](https://github.com/nodejs/node/pull/5416)
* [[`0a1eb168e0`](https://github.com/nodejs/node/commit/0a1eb168e0)] - **test**: fix `test-cluster-worker-kill` (Santiago Gimeno) [#5814](https://github.com/nodejs/node/pull/5814)
* [[`86b876fe7b`](https://github.com/nodejs/node/commit/86b876fe7b)] - **test**: smaller chunk size for smaller person.jpg (Jérémy Lal) [#5813](https://github.com/nodejs/node/pull/5813)
* [[`1135ee97e7`](https://github.com/nodejs/node/commit/1135ee97e7)] - **test**: strip non-free icc profile from person.jpg (Jérémy Lal) [#5813](https://github.com/nodejs/node/pull/5813)
* [[`0836d7e2fb`](https://github.com/nodejs/node/commit/0836d7e2fb)] - **test**: fix flaky test-cluster-shared-leak (Claudio Rodriguez) [#5802](https://github.com/nodejs/node/pull/5802)
* [[`e57355c2f4`](https://github.com/nodejs/node/commit/e57355c2f4)] - **test**: make test-net-connect-options-ipv6.js better (Michael Dawson) [#5791](https://github.com/nodejs/node/pull/5791)
* [[`1b266fc15c`](https://github.com/nodejs/node/commit/1b266fc15c)] - **test**: remove the use of curl in the test suite (Santiago Gimeno) [#5750](https://github.com/nodejs/node/pull/5750)
* [[`7e45d4f076`](https://github.com/nodejs/node/commit/7e45d4f076)] - **test**: minimize test-http-get-pipeline-problem (Rich Trott) [#5728](https://github.com/nodejs/node/pull/5728)
* [[`78effc3484`](https://github.com/nodejs/node/commit/78effc3484)] - **test**: add batch of known issue tests (cjihrig) [#5653](https://github.com/nodejs/node/pull/5653)
* [[`d506eea4b7`](https://github.com/nodejs/node/commit/d506eea4b7)] - **test**: improve test-npm-install (Santiago Gimeno) [#5613](https://github.com/nodejs/node/pull/5613)
* [[`7520100e8b`](https://github.com/nodejs/node/commit/7520100e8b)] - **test**: add test-npm-install to parallel tests suite (Myles Borins) [#5166](https://github.com/nodejs/node/pull/5166)
* [[`b258dddb8c`](https://github.com/nodejs/node/commit/b258dddb8c)] - **test**: repl tab completion test (Santiago Gimeno) [#5534](https://github.com/nodejs/node/pull/5534)
* [[`f209effe8b`](https://github.com/nodejs/node/commit/f209effe8b)] - **test**: remove timer from test-http-1.0 (Santiago Gimeno) [#5129](https://github.com/nodejs/node/pull/5129)
* [[`3a901b0e3e`](https://github.com/nodejs/node/commit/3a901b0e3e)] - **tools**: remove unused imports (Sakthipriyan Vairamani) [#5765](https://github.com/nodejs/node/pull/5765)

<a id="4.4.1"></a>
## 2016-03-22, Version 4.4.1 'Argon' (LTS), @thealphanerd

This LTS release comes with 113 commits, 56 of which are doc related,
18 of which are build / tooling related, 16 of which are test related
and 7 which are benchmark related.

### Notable Changes
* **build**:
  - Updated Logos for the OSX + Windows installers
    - (Rod Vagg) [#5401](https://github.com/nodejs/node/pull/5401)
    - (Robert Jefe Lindstaedt) [#5531](https://github.com/nodejs/node/pull/5531)
  - New option to select your VS Version in the Windows installer
    - (julien.waechter) [#4645](https://github.com/nodejs/node/pull/4645)
  - Support Visual C++ Build Tools 2015
    - (João Reis) [#5627](https://github.com/nodejs/node/pull/5627)
* **tools**:
  - Gyp now works on OSX without XCode
    - (Shigeki Ohtsu) [nodejs/node#1325](https://github.com/nodejs/node/pull/1325)

### Commits

* [[`df283f8a03`](https://github.com/nodejs/node/commit/df283f8a03)] - **benchmark**: fix linting issues (Rich Trott) [#5773](https://github.com/nodejs/node/pull/5773)
* [[`c901741c60`](https://github.com/nodejs/node/commit/c901741c60)] - **benchmark**: use strict mode (Rich Trott) [#5773](https://github.com/nodejs/node/pull/5773)
* [[`4be2065dbc`](https://github.com/nodejs/node/commit/4be2065dbc)] - **benchmark**: refactor to eliminate redeclared vars (Rich Trott) [#5773](https://github.com/nodejs/node/pull/5773)
* [[`ddac368533`](https://github.com/nodejs/node/commit/ddac368533)] - **benchmark**: fix lint errors (Rich Trott) [#5773](https://github.com/nodejs/node/pull/5773)
* [[`03b20a73b9`](https://github.com/nodejs/node/commit/03b20a73b9)] - **benchmark**: add benchmark for buf.compare() (Rich Trott) [#5441](https://github.com/nodejs/node/pull/5441)
* [[`b816044845`](https://github.com/nodejs/node/commit/b816044845)] - **buffer**: remove duplicated code in fromObject (HUANG Wei) [#4948](https://github.com/nodejs/node/pull/4948)
* [[`067ce9b905`](https://github.com/nodejs/node/commit/067ce9b905)] - **build**: don't install github templates (Johan Bergström) [#5612](https://github.com/nodejs/node/pull/5612)
* [[`a1772dc515`](https://github.com/nodejs/node/commit/a1772dc515)] - **build**: update Node.js logo on OSX installer (Rod Vagg) [#5401](https://github.com/nodejs/node/pull/5401)
* [[`9058fc0383`](https://github.com/nodejs/node/commit/9058fc0383)] - **build**: correctly detect clang version (Stefan Budeanu) [#5553](https://github.com/nodejs/node/pull/5553)
* [[`1165ecc6f7`](https://github.com/nodejs/node/commit/1165ecc6f7)] - **build**: update Node.js logo on Win installer (Robert Jefe Lindstaedt) [#5531](https://github.com/nodejs/node/pull/5531)
* [[`4990ddad72`](https://github.com/nodejs/node/commit/4990ddad72)] - **build**: remove --quiet from eslint invocation (firedfox) [#5519](https://github.com/nodejs/node/pull/5519)
* [[`46a5d519dd`](https://github.com/nodejs/node/commit/46a5d519dd)] - **build**: skip msi build if WiX is not found (Tsarevich Dmitry) [#5220](https://github.com/nodejs/node/pull/5220)
* [[`dac4e64491`](https://github.com/nodejs/node/commit/dac4e64491)] - **build**: add option to select VS version (julien.waechter) [#4645](https://github.com/nodejs/node/pull/4645)
* [[`7a10fd3a56`](https://github.com/nodejs/node/commit/7a10fd3a56)] - **collaborator_guide**: clarify commit message rules (Wyatt Preul) [#5661](https://github.com/nodejs/node/pull/5661)
* [[`97e95d04c2`](https://github.com/nodejs/node/commit/97e95d04c2)] - **crypto**: PBKDF2 works with `int` not `ssize_t` (Fedor Indutny) [#5397](https://github.com/nodejs/node/pull/5397)
* [[`57b02e6a3e`](https://github.com/nodejs/node/commit/57b02e6a3e)] - **debugger**: remove unneeded callback check (Rich Trott) [#5319](https://github.com/nodejs/node/pull/5319)
* [[`19ae308867`](https://github.com/nodejs/node/commit/19ae308867)] - **deps**: update openssl config (Shigeki Ohtsu) [#5630](https://github.com/nodejs/node/pull/5630)
* [[`d7b81b5bc7`](https://github.com/nodejs/node/commit/d7b81b5bc7)] - **deps**: cherry-pick 2e4da65 from v8's 4.8 upstream (Michael Dawson) [#5293](https://github.com/nodejs/node/pull/5293)
* [[`1e05f371d6`](https://github.com/nodejs/node/commit/1e05f371d6)] - **doc**: fix typo in synchronous randomBytes example (Andrea Giammarchi) [#5781](https://github.com/nodejs/node/pull/5781)
* [[`5f54bd2088`](https://github.com/nodejs/node/commit/5f54bd2088)] - **doc**: topic blocking vs non-blocking (Jarrett Widman) [#5326](https://github.com/nodejs/node/pull/5326)
* [[`0943001563`](https://github.com/nodejs/node/commit/0943001563)] - **doc**: fix invalid path doc comments (Rich Trott) [#5797](https://github.com/nodejs/node/pull/5797)
* [[`bb423bb1e6`](https://github.com/nodejs/node/commit/bb423bb1e6)] - **doc**: update release tweet template (Jeremiah Senkpiel) [#5628](https://github.com/nodejs/node/pull/5628)
* [[`1e877f10aa`](https://github.com/nodejs/node/commit/1e877f10aa)] - **doc**: fix typo in child_process docs (Benjamin Gruenbaum) [#5681](https://github.com/nodejs/node/pull/5681)
* [[`d53dcc599b`](https://github.com/nodejs/node/commit/d53dcc599b)] - **doc**: update fansworld-claudio username on README (Claudio Rodriguez) [#5680](https://github.com/nodejs/node/pull/5680)
* [[`4332f8011e`](https://github.com/nodejs/node/commit/4332f8011e)] - **doc**: fix return value of write methods (Felix Böhm) [#5736](https://github.com/nodejs/node/pull/5736)
* [[`e572542de5`](https://github.com/nodejs/node/commit/e572542de5)] - **doc**: Add note about use of JSON.stringify() (Mithun Patel) [#5723](https://github.com/nodejs/node/pull/5723)
* [[`daf3ef66ef`](https://github.com/nodejs/node/commit/daf3ef66ef)] - **doc**: explain path.format() algorithm (Rich Trott) [#5688](https://github.com/nodejs/node/pull/5688)
* [[`f6d4982aa0`](https://github.com/nodejs/node/commit/f6d4982aa0)] - **doc**: clarify type of first argument in zlib (Kirill Fomichev) [#5685](https://github.com/nodejs/node/pull/5685)
* [[`07e71b2d44`](https://github.com/nodejs/node/commit/07e71b2d44)] - **doc**: fix typo in api/addons (Daijiro Wachi) [#5678](https://github.com/nodejs/node/pull/5678)
* [[`c6dc56175b`](https://github.com/nodejs/node/commit/c6dc56175b)] - **doc**: remove non-standard use of hyphens (Stefano Vozza)
* [[`4c92316972`](https://github.com/nodejs/node/commit/4c92316972)] - **doc**: add fansworld-claudio to collaborators (Claudio Rodriguez) [#5668](https://github.com/nodejs/node/pull/5668)
* [[`0a6e883f85`](https://github.com/nodejs/node/commit/0a6e883f85)] - **doc**: add thekemkid to collaborators (Glen Keane) [#5667](https://github.com/nodejs/node/pull/5667)
* [[`39c7d8a972`](https://github.com/nodejs/node/commit/39c7d8a972)] - **doc**: add AndreasMadsen to collaborators (Andreas Madsen) [#5666](https://github.com/nodejs/node/pull/5666)
* [[`eec3008970`](https://github.com/nodejs/node/commit/eec3008970)] - **doc**: add whitlockjc to collaborators (Jeremy Whitlock) [#5665](https://github.com/nodejs/node/pull/5665)
* [[`e5f254d83c`](https://github.com/nodejs/node/commit/e5f254d83c)] - **doc**: add benjamingr to collaborator list (Benjamin Gruenbaum) [#5664](https://github.com/nodejs/node/pull/5664)
* [[`3f718643c9`](https://github.com/nodejs/node/commit/3f718643c9)] - **doc**: add phillipj to collaborators (Phillip Johnsen) [#5663](https://github.com/nodejs/node/pull/5663)
* [[`2d5527fe69`](https://github.com/nodejs/node/commit/2d5527fe69)] - **doc**: add mattloring to collaborators (Matt Loring) [#5662](https://github.com/nodejs/node/pull/5662)
* [[`51763462bc`](https://github.com/nodejs/node/commit/51763462bc)] - **doc**: include typo in 'unhandledRejection' example (Robert C Jensen) [#5654](https://github.com/nodejs/node/pull/5654)
* [[`cae5da2f0a`](https://github.com/nodejs/node/commit/cae5da2f0a)] - **doc**: fix markdown links (Steve Mao) [#5641](https://github.com/nodejs/node/pull/5641)
* [[`b1b17efcb7`](https://github.com/nodejs/node/commit/b1b17efcb7)] - **doc**: move build instructions to a new document (Johan Bergström) [#5634](https://github.com/nodejs/node/pull/5634)
* [[`13a8bde1fa`](https://github.com/nodejs/node/commit/13a8bde1fa)] - **doc**: fix dns.resolveCname description typo (axvm) [#5622](https://github.com/nodejs/node/pull/5622)
* [[`1faea43c40`](https://github.com/nodejs/node/commit/1faea43c40)] - **doc**: fix typo in fs.symlink (Michaël Zasso) [#5560](https://github.com/nodejs/node/pull/5560)
* [[`98a1bb6989`](https://github.com/nodejs/node/commit/98a1bb6989)] - **doc**: document directories in test directory (Michael Barrett) [#5557](https://github.com/nodejs/node/pull/5557)
* [[`04d3f8a741`](https://github.com/nodejs/node/commit/04d3f8a741)] - **doc**: update link green to match homepage (silverwind) [#5548](https://github.com/nodejs/node/pull/5548)
* [[`1afab6ac9c`](https://github.com/nodejs/node/commit/1afab6ac9c)] - **doc**: add clarification on birthtime in fs stat (Kári Tristan Helgason) [#5479](https://github.com/nodejs/node/pull/5479)
* [[`d871ae2349`](https://github.com/nodejs/node/commit/d871ae2349)] - **doc**: fix typo in child_process documentation (Evan Lucas) [#5474](https://github.com/nodejs/node/pull/5474)
* [[`97a18bdbad`](https://github.com/nodejs/node/commit/97a18bdbad)] - **doc**: update NAN urls in ROADMAP.md and doc/releases.md (ronkorving) [#5472](https://github.com/nodejs/node/pull/5472)
* [[`d4a1fc7acd`](https://github.com/nodejs/node/commit/d4a1fc7acd)] - **doc**: add Testing WG (Rich Trott) [#5461](https://github.com/nodejs/node/pull/5461)
* [[`1642078580`](https://github.com/nodejs/node/commit/1642078580)] - **doc**: fix crypto function indentation level (Brian White) [#5460](https://github.com/nodejs/node/pull/5460)
* [[`2b0c7ad985`](https://github.com/nodejs/node/commit/2b0c7ad985)] - **doc**: fix links in tls, cluster docs (Alexander Makarenko) [#5364](https://github.com/nodejs/node/pull/5364)
* [[`901dbabea6`](https://github.com/nodejs/node/commit/901dbabea6)] - **doc**: fix relative links in net docs (Evan Lucas) [#5358](https://github.com/nodejs/node/pull/5358)
* [[`38d429172d`](https://github.com/nodejs/node/commit/38d429172d)] - **doc**: fix typo in pbkdf2Sync code sample (Marc Cuva) [#5306](https://github.com/nodejs/node/pull/5306)
* [[`d4cfc6f97c`](https://github.com/nodejs/node/commit/d4cfc6f97c)] - **doc**: add missing property in cluster example (Rafael Cepeda) [#5305](https://github.com/nodejs/node/pull/5305)
* [[`b66d6b1458`](https://github.com/nodejs/node/commit/b66d6b1458)] - **doc**: improve httpVersionMajor / httpVersionMajor (Jackson Tian) [#5296](https://github.com/nodejs/node/pull/5296)
* [[`70c872c9c4`](https://github.com/nodejs/node/commit/70c872c9c4)] - **doc**: improve unhandledException doc copy (James M Snell) [#5287](https://github.com/nodejs/node/pull/5287)
* [[`ba5e0b6110`](https://github.com/nodejs/node/commit/ba5e0b6110)] - **doc**: fix buf.readInt16LE output (Chinedu Francis Nwafili) [#5282](https://github.com/nodejs/node/pull/5282)
* [[`1624d5b049`](https://github.com/nodejs/node/commit/1624d5b049)] - **doc**: document base64url encoding support (Tristan Slominski) [#5243](https://github.com/nodejs/node/pull/5243)
* [[`b1d580c9d2`](https://github.com/nodejs/node/commit/b1d580c9d2)] - **doc**: update removeListener behaviour (Vaibhav) [#5201](https://github.com/nodejs/node/pull/5201)
* [[`ca17f91ba8`](https://github.com/nodejs/node/commit/ca17f91ba8)] - **doc**: add note for binary safe string reading (Anton Andesen) [#5155](https://github.com/nodejs/node/pull/5155)
* [[`0830bb4950`](https://github.com/nodejs/node/commit/0830bb4950)] - **doc**: clarify when writable.write callback is called (Kevin Locke) [#4810](https://github.com/nodejs/node/pull/4810)
* [[`17a74305c8`](https://github.com/nodejs/node/commit/17a74305c8)] - **doc**: add info to docs on how to submit docs patch (Sequoia McDowell) [#4591](https://github.com/nodejs/node/pull/4591)
* [[`470a9ca909`](https://github.com/nodejs/node/commit/470a9ca909)] - **doc**: add onboarding resources (Jeremiah Senkpiel) [#3726](https://github.com/nodejs/node/pull/3726)
* [[`3168e6b486`](https://github.com/nodejs/node/commit/3168e6b486)] - **doc**: update V8 URL (Craig Akimoto) [#5530](https://github.com/nodejs/node/pull/5530)
* [[`04d16eb7e8`](https://github.com/nodejs/node/commit/04d16eb7e8)] - **doc**: document fs.datasync(Sync) (Ron Korving) [#5402](https://github.com/nodejs/node/pull/5402)
* [[`29646200f8`](https://github.com/nodejs/node/commit/29646200f8)] - **doc**: add Evan Lucas to the CTC (Rod Vagg)
* [[`a2a32b7810`](https://github.com/nodejs/node/commit/a2a32b7810)] - **doc**: add Rich Trott to the CTC (Rod Vagg) [#5276](https://github.com/nodejs/node/pull/5276)
* [[`4e469d5e47`](https://github.com/nodejs/node/commit/4e469d5e47)] - **doc**: add Ali Ijaz Sheikh to the CTC (Rod Vagg) [#5277](https://github.com/nodejs/node/pull/5277)
* [[`d09b44f59b`](https://github.com/nodejs/node/commit/d09b44f59b)] - **doc**: add Сковорода Никита Андреевич to the CTC (Rod Vagg) [#5278](https://github.com/nodejs/node/pull/5278)
* [[`ebbc64bc97`](https://github.com/nodejs/node/commit/ebbc64bc97)] - **doc**: add "building node with ninja" guide (Jeremiah Senkpiel) [#4767](https://github.com/nodejs/node/pull/4767)
* [[`67245fa0e3`](https://github.com/nodejs/node/commit/67245fa0e3)] - **doc**: clarify code of conduct reporting (Julie Pagano) [#5107](https://github.com/nodejs/node/pull/5107)
* [[`cd78ff9706`](https://github.com/nodejs/node/commit/cd78ff9706)] - **doc**: fix links in Addons docs (Alexander Makarenko) [#5072](https://github.com/nodejs/node/pull/5072)
* [[`20539954ff`](https://github.com/nodejs/node/commit/20539954ff)] - **docs**: fix man pages link if tok type is code (Mithun Patel) [#5721](https://github.com/nodejs/node/pull/5721)
* [[`38d7b0b6ea`](https://github.com/nodejs/node/commit/38d7b0b6ea)] - **docs**: update link to iojs+release ci job (Myles Borins) [#5632](https://github.com/nodejs/node/pull/5632)
* [[`f982632f90`](https://github.com/nodejs/node/commit/f982632f90)] - **http**: remove old, confusing comment (Brian White) [#5233](https://github.com/nodejs/node/pull/5233)
* [[`ca5d7a8bb6`](https://github.com/nodejs/node/commit/ca5d7a8bb6)] - **http**: remove unnecessary check (Brian White) [#5233](https://github.com/nodejs/node/pull/5233)
* [[`2ce83bd8f9`](https://github.com/nodejs/node/commit/2ce83bd8f9)] - **http,util**: fix typos in comments (Alexander Makarenko) [#5279](https://github.com/nodejs/node/pull/5279)
* [[`b690916e5a`](https://github.com/nodejs/node/commit/b690916e5a)] - **lib**: freelist: use .pop() for allocation (Anton Khlynovskiy) [#2174](https://github.com/nodejs/node/pull/2174)
* [[`e7f45f0a17`](https://github.com/nodejs/node/commit/e7f45f0a17)] - **repl**: handle quotes within regexp literal (Prince J Wesley) [#5117](https://github.com/nodejs/node/pull/5117)
* [[`7c3b844f78`](https://github.com/nodejs/node/commit/7c3b844f78)] - **src**: return UV_EAI_NODATA on empty lookup (cjihrig) [#4715](https://github.com/nodejs/node/pull/4715)
* [[`242a65e930`](https://github.com/nodejs/node/commit/242a65e930)] - **stream**: prevent object map change in TransformState (Evan Lucas) [#5032](https://github.com/nodejs/node/pull/5032)
* [[`fb5ba6b928`](https://github.com/nodejs/node/commit/fb5ba6b928)] - **stream**: prevent object map change in ReadableState (Evan Lucas) [#4761](https://github.com/nodejs/node/pull/4761)
* [[`04db9efd78`](https://github.com/nodejs/node/commit/04db9efd78)] - **stream**: fix no data on partial decode (Brian White) [#5226](https://github.com/nodejs/node/pull/5226)
* [[`cc0e36ff98`](https://github.com/nodejs/node/commit/cc0e36ff98)] - **string_decoder**: fix performance regression (Brian White) [#5134](https://github.com/nodejs/node/pull/5134)
* [[`666d3690d8`](https://github.com/nodejs/node/commit/666d3690d8)] - **test**: eval a strict function (Kári Tristan Helgason) [#5250](https://github.com/nodejs/node/pull/5250)
* [[`9952bcf203`](https://github.com/nodejs/node/commit/9952bcf203)] - **test**: bug repro for vm function redefinition (cjihrig) [#5528](https://github.com/nodejs/node/pull/5528)
* [[`063f22f1f0`](https://github.com/nodejs/node/commit/063f22f1f0)] - **test**: check memoryUsage properties The properties on memoryUsage were not checked before, this commit checks them. (Wyatt Preul) [#5546](https://github.com/nodejs/node/pull/5546)
* [[`7a0fcfc127`](https://github.com/nodejs/node/commit/7a0fcfc127)] - **test**: remove broken debugger scenarios (Rich Trott) [#5532](https://github.com/nodejs/node/pull/5532)
* [[`ba9ad2662c`](https://github.com/nodejs/node/commit/ba9ad2662c)] - **test**: apply Linux workaround to Linux only (Rich Trott) [#5471](https://github.com/nodejs/node/pull/5471)
* [[`4aa2c03d31`](https://github.com/nodejs/node/commit/4aa2c03d31)] - **test**: increase timeout for test-tls-fast-writing (Rich Trott) [#5466](https://github.com/nodejs/node/pull/5466)
* [[`b4ef644ce4`](https://github.com/nodejs/node/commit/b4ef644ce4)] - **test**: retry on known SmartOS bug (Rich Trott) [#5454](https://github.com/nodejs/node/pull/5454)
* [[`d681bf24b5`](https://github.com/nodejs/node/commit/d681bf24b5)] - **test**: fix flaky child-process-fork-regr-gh-2847 (Santiago Gimeno) [#5422](https://github.com/nodejs/node/pull/5422)
* [[`b4fbe04514`](https://github.com/nodejs/node/commit/b4fbe04514)] - **test**: fix test-timers.reliability on OS X (Rich Trott) [#5379](https://github.com/nodejs/node/pull/5379)
* [[`99269ffdbf`](https://github.com/nodejs/node/commit/99269ffdbf)] - **test**: increase timeouts on some unref timers tests (Jeremiah Senkpiel) [#5352](https://github.com/nodejs/node/pull/5352)
* [[`85f927a774`](https://github.com/nodejs/node/commit/85f927a774)] - **test**: prevent flakey test on pi2 (Trevor Norris) [#5537](https://github.com/nodejs/node/pull/5537)
* [[`c86902d800`](https://github.com/nodejs/node/commit/c86902d800)] - **test**: mitigate flaky test-http-agent (Rich Trott) [#5346](https://github.com/nodejs/node/pull/5346)
* [[`f242e62817`](https://github.com/nodejs/node/commit/f242e62817)] - **test**: remove flaky designation from fixed tests (Rich Trott) [#5459](https://github.com/nodejs/node/pull/5459)
* [[`a39aacf035`](https://github.com/nodejs/node/commit/a39aacf035)] - **test**: refactor test-dgram-udp4 (Santiago Gimeno) [#5339](https://github.com/nodejs/node/pull/5339)
* [[`6386f62221`](https://github.com/nodejs/node/commit/6386f62221)] - **test**: remove unneeded bind() and related comments (Aayush Naik) [#5023](https://github.com/nodejs/node/pull/5023)
* [[`068b0cbd12`](https://github.com/nodejs/node/commit/068b0cbd12)] - **test**: move cluster tests to parallel (Rich Trott) [#4774](https://github.com/nodejs/node/pull/4774)
* [[`a673c9ae2d`](https://github.com/nodejs/node/commit/a673c9ae2d)] - **tls**: fix assert in context._external accessor (Ben Noordhuis) [#5521](https://github.com/nodejs/node/pull/5521)
* [[`8ffef48fee`](https://github.com/nodejs/node/commit/8ffef48fee)] - **tools**: fix gyp to work on MacOSX without XCode (Shigeki Ohtsu) [nodejs/node#1325](https://github.com/nodejs/node/pull/1325)
* [[`4b6a8f4321`](https://github.com/nodejs/node/commit/4b6a8f4321)] - **tools**: update gyp to b3cef02 (Imran Iqbal) [#3487](https://github.com/nodejs/node/pull/3487)
* [[`7501ddc878`](https://github.com/nodejs/node/commit/7501ddc878)] - **tools**: support testing known issues (cjihrig) [#5528](https://github.com/nodejs/node/pull/5528)
* [[`10ec1d2a6b`](https://github.com/nodejs/node/commit/10ec1d2a6b)] - **tools**: enable linting for benchmarks (Rich Trott) [#5773](https://github.com/nodejs/node/pull/5773)
* [[`deec8bc5f5`](https://github.com/nodejs/node/commit/deec8bc5f5)] - **tools**: reduce verbosity of cpplint (Sakthipriyan Vairamani) [#5578](https://github.com/nodejs/node/pull/5578)
* [[`64d5752711`](https://github.com/nodejs/node/commit/64d5752711)] - **tools**: enable no-self-assign ESLint rule (Rich Trott) [#5552](https://github.com/nodejs/node/pull/5552)
* [[`131ed494e2`](https://github.com/nodejs/node/commit/131ed494e2)] - **tools**: enable no-extra-parens in ESLint (Rich Trott) [#5512](https://github.com/nodejs/node/pull/5512)
* [[`d4b9f02fdc`](https://github.com/nodejs/node/commit/d4b9f02fdc)] - **tools**: apply custom buffer lint rule to /lib only (Rich Trott) [#5371](https://github.com/nodejs/node/pull/5371)
* [[`6867bed4c4`](https://github.com/nodejs/node/commit/6867bed4c4)] - **tools**: enable additional lint rules (Rich Trott) [#5357](https://github.com/nodejs/node/pull/5357)
* [[`5e6b7605ee`](https://github.com/nodejs/node/commit/5e6b7605ee)] - **tools**: add Node.js-specific ESLint rules (Rich Trott) [#5320](https://github.com/nodejs/node/pull/5320)
* [[`6dc49ae203`](https://github.com/nodejs/node/commit/6dc49ae203)] - **tools,benchmark**: increase lint compliance (Rich Trott) [#5773](https://github.com/nodejs/node/pull/5773)
* [[`dff7091fce`](https://github.com/nodejs/node/commit/dff7091fce)] - **url**: group slashed protocols by protocol name (nettofarah) [#5380](https://github.com/nodejs/node/pull/5380)
* [[`0e97a3ea51`](https://github.com/nodejs/node/commit/0e97a3ea51)] - **win,build**: support Visual C++ Build Tools 2015 (João Reis) [#5627](https://github.com/nodejs/node/pull/5627)

<a id="4.4.0"></a>
## 2016-03-08, Version 4.4.0 'Argon' (LTS), @thealphanerd

In December we announced that we would be doing a minor release in order to
get a number of voted on SEMVER-MINOR changes into LTS. Our ability to release this
was delayed due to the unforeseen security release v4.3. We are quickly bumping to
v4.4 in order to bring you the features that we had committed to releasing.

This release also includes over 70 fixes to our docs and over 50 fixes to tests.

### Notable changes

The SEMVER-MINOR changes include:
* **deps**:
  - An update to v8 that introduces a new flag --perf_basic_prof_only_functions (Ali Ijaz Sheikh) [#3609](https://github.com/nodejs/node/pull/3609)
* **http**:
  - A new feature in http(s) agent that catches errors on *keep alived* connections (José F. Romaniello) [#4482](https://github.com/nodejs/node/pull/4482)
* **src**:
  - Better support for Big-Endian systems (Bryon Leung) [#3410](https://github.com/nodejs/node/pull/3410)
* **tls**:
  - A new feature that allows you to pass common SSL options to `tls.createSecurePair` (Коренберг Марк) [#2441](https://github.com/nodejs/node/pull/2441)
* **tools**:
  - a new flag `--prof-process` which will execute the tick processor on the provided isolate files (Matt Loring) [#4021](https://github.com/nodejs/node/pull/4021)

Notable semver patch changes include:

* **buld**:
  - Support python path that includes spaces. This should be of particular interest to our Windows users who may have python living in `c:/Program Files` (Felix Becker) [#4841](https://github.com/nodejs/node/pull/4841)
* **https**:
  - A potential fix for [#3692](https://github.com/nodejs/node/issues/3692) HTTP/HTTPS client requests throwing EPROTO (Fedor Indutny) [#4982](https://github.com/nodejs/node/pull/4982)
* **installer**:
  - More readable profiling information from isolate tick logs (Matt Loring) [#3032](https://github.com/nodejs/node/pull/3032)
* **npm**:
  - upgrade to npm 2.14.20 (Kat Marchán) [#5510](https://github.com/nodejs/node/pull/5510)
* **process**:
  - Add support for symbols in event emitters. Symbols didn't exist when it was written ¯\_(ツ)_/¯ (cjihrig) [#4798](https://github.com/nodejs/node/pull/4798)
* **querystring**:
  - querystring.parse() is now 13-22% faster! (Brian White) [#4675](https://github.com/nodejs/node/pull/4675)
* **streams**:
  - performance improvements for moving small buffers that shows a 5% throughput gain. IoT projects have been seen to be as much as 10% faster with this change! (Matteo Collina) [#4354](https://github.com/nodejs/node/pull/4354)
* **tools**:
  - eslint has been updated to version 2.1.0 (Rich Trott) [#5214](https://github.com/nodejs/node/pull/5214)

### Commits

* [[`360e04fd5a`](https://github.com/nodejs/node/commit/360e04fd5a)] - internal/child_process: call postSend on error (Fedor Indutny) [#4752](https://github.com/nodejs/node/pull/4752)
* [[`a29f501aa2`](https://github.com/nodejs/node/commit/a29f501aa2)] - **benchmark**: add a constant declaration for `net` (Minwoo Jung) [#3950](https://github.com/nodejs/node/pull/3950)
* [[`85e06a2e34`](https://github.com/nodejs/node/commit/85e06a2e34)] - **(SEMVER-MINOR)** **buffer**: allow encoding param to collapse (Trevor Norris) [#4803](https://github.com/nodejs/node/pull/4803)
* [[`fe893a8ebc`](https://github.com/nodejs/node/commit/fe893a8ebc)] - **(SEMVER-MINOR)** **buffer**: properly retrieve binary length of needle (Trevor Norris) [#4803](https://github.com/nodejs/node/pull/4803)
* [[`fae7c9db3f`](https://github.com/nodejs/node/commit/fae7c9db3f)] - **buffer**: refactor redeclared variables (Rich Trott) [#4886](https://github.com/nodejs/node/pull/4886)
* [[`4a6e2b26f7`](https://github.com/nodejs/node/commit/4a6e2b26f7)] - **build**: treat aarch64 as arm64 (Johan Bergström) [#5191](https://github.com/nodejs/node/pull/5191)
* [[`bc2536dfc6`](https://github.com/nodejs/node/commit/bc2536dfc6)] - **build**: add a help message and removed a TODO. (Ojas Shirekar) [#5080](https://github.com/nodejs/node/pull/5080)
* [[`f6416be5d2`](https://github.com/nodejs/node/commit/f6416be5d2)] - **build**: remove redundant TODO in configure (Ojas Shirekar) [#5080](https://github.com/nodejs/node/pull/5080)
* [[`6deb7a6eb8`](https://github.com/nodejs/node/commit/6deb7a6eb8)] - **build**: remove Makefile.build (Ojas Shirekar) [#5080](https://github.com/nodejs/node/pull/5080)
* [[`66d1115555`](https://github.com/nodejs/node/commit/66d1115555)] - **build**: fix build when python path contains spaces (Felix Becker) [#4841](https://github.com/nodejs/node/pull/4841)
* [[`29951cf36a`](https://github.com/nodejs/node/commit/29951cf36a)] - **child_process**: fix data loss with readable event (Brian White) [#5036](https://github.com/nodejs/node/pull/5036)
* [[`81d4127279`](https://github.com/nodejs/node/commit/81d4127279)] - **cluster**: dont rely on `this` in `fork` (Igor Klopov) [#5216](https://github.com/nodejs/node/pull/5216)
* [[`de4c07b29e`](https://github.com/nodejs/node/commit/de4c07b29e)] - **console**: apply null as `this` for util.format (Jackson Tian) [#5222](https://github.com/nodejs/node/pull/5222)
* [[`4e0755cab3`](https://github.com/nodejs/node/commit/4e0755cab3)] - **crypto**: have fixed NodeBIOs return EOF (Adam Langley) [#5105](https://github.com/nodejs/node/pull/5105)
* [[`a7955d5071`](https://github.com/nodejs/node/commit/a7955d5071)] - **crypto**: fix memory leak in LoadPKCS12 (Fedor Indutny) [#5109](https://github.com/nodejs/node/pull/5109)
* [[`5d9c1cf001`](https://github.com/nodejs/node/commit/5d9c1cf001)] - **crypto**: add `pfx` certs as CA certs too (Fedor Indutny) [#5109](https://github.com/nodejs/node/pull/5109)
* [[`ab5cb0539b`](https://github.com/nodejs/node/commit/ab5cb0539b)] - **crypto**: use SSL_CTX_clear_extra_chain_certs. (Adam Langley) [#4919](https://github.com/nodejs/node/pull/4919)
* [[`198928eb9f`](https://github.com/nodejs/node/commit/198928eb9f)] - **crypto**: fix build when OCSP-stapling not provided (Adam Langley) [#4914](https://github.com/nodejs/node/pull/4914)
* [[`b8e1089df0`](https://github.com/nodejs/node/commit/b8e1089df0)] - **crypto**: use a const SSL_CIPHER (Adam Langley) [#4913](https://github.com/nodejs/node/pull/4913)
* [[`139d6d9284`](https://github.com/nodejs/node/commit/139d6d9284)] - **debugger**: assert test before accessing this.binding (Prince J Wesley) [#5145](https://github.com/nodejs/node/pull/5145)
* [[`9c8f2ab546`](https://github.com/nodejs/node/commit/9c8f2ab546)] - **deps**: upgrade to npm 2.14.20 (Kat Marchán) [#5510](https://github.com/nodejs/node/pull/5510)
* [[`e591a0927f`](https://github.com/nodejs/node/commit/e591a0927f)] - **deps**: upgrade to npm 2.14.19 (Kat Marchán) [#5335](https://github.com/nodejs/node/pull/5335)
* [[`a5ce67a0aa`](https://github.com/nodejs/node/commit/a5ce67a0aa)] - **deps**: upgrade to npm 2.14.18 (Kat Marchán) [#5245](https://github.com/nodejs/node/pull/5245)
* [[`469db021f7`](https://github.com/nodejs/node/commit/469db021f7)] - **(SEMVER-MINOR)** **deps**: backport 9da3ab6 from V8 upstream (Ali Ijaz Sheikh) [#3609](https://github.com/nodejs/node/pull/3609)
* [[`3ca04a5de9`](https://github.com/nodejs/node/commit/3ca04a5de9)] - **deps**: backport 8d00c2c from v8 upstream (Gibson Fahnestock) [#5024](https://github.com/nodejs/node/pull/5024)
* [[`60e0bd4be9`](https://github.com/nodejs/node/commit/60e0bd4be9)] - **deps**: upgrade to npm 2.14.17 (Kat Marchán) [#5110](https://github.com/nodejs/node/pull/5110)
* [[`976b9a9ab3`](https://github.com/nodejs/node/commit/976b9a9ab3)] - **deps**: upgrade to npm 2.14.16 (Kat Marchán) [#4960](https://github.com/nodejs/node/pull/4960)
* [[`38b370abea`](https://github.com/nodejs/node/commit/38b370abea)] - **deps**: upgrade to npm 2.14.15 (Kat Marchán) [#4872](https://github.com/nodejs/node/pull/4872)
* [[`82f549ef81`](https://github.com/nodejs/node/commit/82f549ef81)] - **dgram**: scope redeclared variables (Rich Trott) [#4940](https://github.com/nodejs/node/pull/4940)
* [[`063e14b568`](https://github.com/nodejs/node/commit/063e14b568)] - **dns**: throw a TypeError in lookupService with invalid port (Evan Lucas) [#4839](https://github.com/nodejs/node/pull/4839)
* [[`a2613aefae`](https://github.com/nodejs/node/commit/a2613aefae)] - **doc**: remove out-of-date matter from internal docs (Rich Trott) [#5421](https://github.com/nodejs/node/pull/5421)
* [[`394743f4b3`](https://github.com/nodejs/node/commit/394743f4b3)] - **doc**: explicit about VS 2015 support in readme (Phillip Johnsen) [#5406](https://github.com/nodejs/node/pull/5406)
* [[`da6b26fbfb`](https://github.com/nodejs/node/commit/da6b26fbfb)] - **doc**: copyedit util doc (Rich Trott) [#5399](https://github.com/nodejs/node/pull/5399)
* [[`7070ad0cc0`](https://github.com/nodejs/node/commit/7070ad0cc0)] - **doc**: mention prototype check in deepStrictEqual() (cjihrig) [#5367](https://github.com/nodejs/node/pull/5367)
* [[`d4789fc5fd`](https://github.com/nodejs/node/commit/d4789fc5fd)] - **doc**: s/http/https in Myles Borins' GitHub link (Rod Vagg) [#5356](https://github.com/nodejs/node/pull/5356)
* [[`b86540d1eb`](https://github.com/nodejs/node/commit/b86540d1eb)] - **doc**: clarify error handling in net.createServer (Dirceu Pereira Tiegs) [#5353](https://github.com/nodejs/node/pull/5353)
* [[`3106297037`](https://github.com/nodejs/node/commit/3106297037)] - **doc**: `require` behavior on case-insensitive systems (Hugo Wood)
* [[`e0b45e4315`](https://github.com/nodejs/node/commit/e0b45e4315)] - **doc**: update repo docs to use 'CTC' (Alexis Campailla) [#5304](https://github.com/nodejs/node/pull/5304)
* [[`e355f13989`](https://github.com/nodejs/node/commit/e355f13989)] - **doc**: improvements to crypto.markdown copy (Alexander Makarenko) [#5230](https://github.com/nodejs/node/pull/5230)
* [[`a9035b5e1d`](https://github.com/nodejs/node/commit/a9035b5e1d)] - **doc**: link to man pages (dcposch@dcpos.ch) [#5073](https://github.com/nodejs/node/pull/5073)
* [[`2043e6a63c`](https://github.com/nodejs/node/commit/2043e6a63c)] - **doc**: clarify child_process.execFile{,Sync} file arg (Kevin Locke) [#5310](https://github.com/nodejs/node/pull/5310)
* [[`8c732ad1e1`](https://github.com/nodejs/node/commit/8c732ad1e1)] - **doc**: fix buf.length slice example (Chinedu Francis Nwafili) [#5259](https://github.com/nodejs/node/pull/5259)
* [[`6c27c78b8b`](https://github.com/nodejs/node/commit/6c27c78b8b)] - **doc**: fix buffer\[index\] example (Chinedu Francis Nwafili) [#5253](https://github.com/nodejs/node/pull/5253)
* [[`7765f99683`](https://github.com/nodejs/node/commit/7765f99683)] - **doc**: fix template string (Rafael Cepeda) [#5240](https://github.com/nodejs/node/pull/5240)
* [[`d15ef20162`](https://github.com/nodejs/node/commit/d15ef20162)] - **doc**: improvements to console.markdown copy (Alexander Makarenko) [#5225](https://github.com/nodejs/node/pull/5225)
* [[`593206a752`](https://github.com/nodejs/node/commit/593206a752)] - **doc**: fix net.createConnection() example (Brian White) [#5219](https://github.com/nodejs/node/pull/5219)
* [[`464636b5c5`](https://github.com/nodejs/node/commit/464636b5c5)] - **doc**: improve scrolling, various CSS tweaks (Roman Reiss) [#5198](https://github.com/nodejs/node/pull/5198)
* [[`f615cd5b0b`](https://github.com/nodejs/node/commit/f615cd5b0b)] - **doc**: console is asynchronous unless it's a file (Ben Noordhuis) [#5133](https://github.com/nodejs/node/pull/5133)
* [[`fbed0d11f1`](https://github.com/nodejs/node/commit/fbed0d11f1)] - **doc**: merging behavior of writeHead vs setHeader (Alejandro Oviedo) [#5081](https://github.com/nodejs/node/pull/5081)
* [[`b0bb42bd7d`](https://github.com/nodejs/node/commit/b0bb42bd7d)] - **doc**: fix reference to API `hash.final` (Minwoo Jung) [#5050](https://github.com/nodejs/node/pull/5050)
* [[`dee5045221`](https://github.com/nodejs/node/commit/dee5045221)] - **doc**: uppercase 'RSA-SHA256' in crypto.markdown (Rainer Oviir) [#5044](https://github.com/nodejs/node/pull/5044)
* [[`498052a017`](https://github.com/nodejs/node/commit/498052a017)] - **doc**: consistent styling for functions in TLS docs (Alexander Makarenko) [#5000](https://github.com/nodejs/node/pull/5000)
* [[`031277e6f8`](https://github.com/nodejs/node/commit/031277e6f8)] - **doc**: apply consistent styling for functions (Rich Trott) [#4974](https://github.com/nodejs/node/pull/4974)
* [[`808fe0ea48`](https://github.com/nodejs/node/commit/808fe0ea48)] - **doc**: fix `notDeepEqual` API (Minwoo Jung) [#4971](https://github.com/nodejs/node/pull/4971)
* [[`5b9025689f`](https://github.com/nodejs/node/commit/5b9025689f)] - **doc**: show links consistently in deprecations (Sakthipriyan Vairamani) [#4907](https://github.com/nodejs/node/pull/4907)
* [[`3a1865db5e`](https://github.com/nodejs/node/commit/3a1865db5e)] - **doc**: don't use "interface" as a variable name (ChALkeR) [#4900](https://github.com/nodejs/node/pull/4900)
* [[`90715c3d68`](https://github.com/nodejs/node/commit/90715c3d68)] - **doc**: keep the names in sorted order (Sakthipriyan Vairamani) [#4876](https://github.com/nodejs/node/pull/4876)
* [[`d8b3b25c9c`](https://github.com/nodejs/node/commit/d8b3b25c9c)] - **doc**: fix JSON generation for aliased methods (Timothy Gu) [#4871](https://github.com/nodejs/node/pull/4871)
* [[`7b763c8d25`](https://github.com/nodejs/node/commit/7b763c8d25)] - **doc**: fix code type of markdowns (Jackson Tian) [#4858](https://github.com/nodejs/node/pull/4858)
* [[`37d4e7afc2`](https://github.com/nodejs/node/commit/37d4e7afc2)] - **doc**: check for errors in 'listen' event (Benjamin Gruenbaum) [#4834](https://github.com/nodejs/node/pull/4834)
* [[`3f876b104c`](https://github.com/nodejs/node/commit/3f876b104c)] - **doc**: Examples work when data exceeds buffer size (Glen Arrowsmith) [#4811](https://github.com/nodejs/node/pull/4811)
* [[`e3e20422a7`](https://github.com/nodejs/node/commit/e3e20422a7)] - **doc**: harmonize $ node command line notation (Robert Jefe Lindstaedt) [#4806](https://github.com/nodejs/node/pull/4806)
* [[`73e0195cef`](https://github.com/nodejs/node/commit/73e0195cef)] - **doc**: fix type references for link gen, link css (Claudio Rodriguez) [#4741](https://github.com/nodejs/node/pull/4741)
* [[`0bdac429e1`](https://github.com/nodejs/node/commit/0bdac429e1)] - **doc**: multiple improvements in Stream docs (Alexander Makarenko) [#5009](https://github.com/nodejs/node/pull/5009)
* [[`693c16fb6b`](https://github.com/nodejs/node/commit/693c16fb6b)] - **doc**: fix anchor links from stream to http and events (piepmatz) [#5007](https://github.com/nodejs/node/pull/5007)
* [[`5fb533522c`](https://github.com/nodejs/node/commit/5fb533522c)] - **doc**: replace function expressions with arrows (Benjamin Gruenbaum) [#4832](https://github.com/nodejs/node/pull/4832)
* [[`e3572fb809`](https://github.com/nodejs/node/commit/e3572fb809)] - **doc**: fix links order in Buffer doc (Alexander Makarenko) [#5076](https://github.com/nodejs/node/pull/5076)
* [[`5c936ab765`](https://github.com/nodejs/node/commit/5c936ab765)] - **doc**: clarify optional arguments of Buffer methods (Michaël Zasso) [#5008](https://github.com/nodejs/node/pull/5008)
* [[`6df350c2b3`](https://github.com/nodejs/node/commit/6df350c2b3)] - **doc**: improve styling consistency in Buffer docs (Alexander Makarenko) [#5001](https://github.com/nodejs/node/pull/5001)
* [[`047f4a157f`](https://github.com/nodejs/node/commit/047f4a157f)] - **doc**: make buffer methods styles consistent (Timothy Gu) [#4873](https://github.com/nodejs/node/pull/4873)
* [[`4cfc017b90`](https://github.com/nodejs/node/commit/4cfc017b90)] - **doc**: fix nonsensical grammar in Buffer::write (Jimb Esser) [#4863](https://github.com/nodejs/node/pull/4863)
* [[`9087f6daca`](https://github.com/nodejs/node/commit/9087f6daca)] - **doc**: fix named anchors in addons.markdown and http.markdown (Michael Theriot) [#4708](https://github.com/nodejs/node/pull/4708)
* [[`4c8713ce58`](https://github.com/nodejs/node/commit/4c8713ce58)] - **doc**: add buf.indexOf encoding param with example (Karl Skomski) [#3373](https://github.com/nodejs/node/pull/3373)
* [[`1819d74491`](https://github.com/nodejs/node/commit/1819d74491)] - **doc**: fenced all code blocks, typo fixes (Robert Jefe Lindstaedt) [#4733](https://github.com/nodejs/node/pull/4733)
* [[`961735e645`](https://github.com/nodejs/node/commit/961735e645)] - **doc**: make references clickable (Roman Klauke) [#4654](https://github.com/nodejs/node/pull/4654)
* [[`7e80442483`](https://github.com/nodejs/node/commit/7e80442483)] - **doc**: improve child_process.execFile() code example (Ryan Sobol) [#4504](https://github.com/nodejs/node/pull/4504)
* [[`de9ad5b39d`](https://github.com/nodejs/node/commit/de9ad5b39d)] - **doc**: remove "above" and "below" references (Richard Sun) [#4499](https://github.com/nodejs/node/pull/4499)
* [[`c549ca3b69`](https://github.com/nodejs/node/commit/c549ca3b69)] - **doc**: fix heading level error in Buffer doc (Shigeki Ohtsu) [#4537](https://github.com/nodejs/node/pull/4537)
* [[`a613bae14c`](https://github.com/nodejs/node/commit/a613bae14c)] - **doc**: improvements to crypto.markdown copy (James M Snell) [#4435](https://github.com/nodejs/node/pull/4435)
* [[`18f580d0c1`](https://github.com/nodejs/node/commit/18f580d0c1)] - **doc**: improve child_process.markdown copy (James M Snell) [#4383](https://github.com/nodejs/node/pull/4383)
* [[`a929837311`](https://github.com/nodejs/node/commit/a929837311)] - **doc**: improvements to buffer.markdown copy (James M Snell) [#4370](https://github.com/nodejs/node/pull/4370)
* [[`a22f688407`](https://github.com/nodejs/node/commit/a22f688407)] - **doc**: improve addons.markdown copy (James M Snell) [#4320](https://github.com/nodejs/node/pull/4320)
* [[`94c2de47b1`](https://github.com/nodejs/node/commit/94c2de47b1)] - **doc**: update process.send() signature (cjihrig) [#5284](https://github.com/nodejs/node/pull/5284)
* [[`4e1926cb08`](https://github.com/nodejs/node/commit/4e1926cb08)] - **doc**: replace node-forward link in CONTRIBUTING.md (Ben Noordhuis) [#5227](https://github.com/nodejs/node/pull/5227)
* [[`e1713e81e5`](https://github.com/nodejs/node/commit/e1713e81e5)] - **doc**: fix minor inconsistencies in repl doc (Rich Trott) [#5193](https://github.com/nodejs/node/pull/5193)
* [[`b2e72c0d92`](https://github.com/nodejs/node/commit/b2e72c0d92)] - **doc**: clarify exceptions during uncaughtException (Noah Rose) [#5180](https://github.com/nodejs/node/pull/5180)
* [[`c3c549836a`](https://github.com/nodejs/node/commit/c3c549836a)] - **doc**: update DCO to v1.1 (Mikeal Rogers) [#5170](https://github.com/nodejs/node/pull/5170)
* [[`9dd35ad594`](https://github.com/nodejs/node/commit/9dd35ad594)] - **doc**: fix dgram doc indentation (Rich Trott) [#5118](https://github.com/nodejs/node/pull/5118)
* [[`eed830702c`](https://github.com/nodejs/node/commit/eed830702c)] - **doc**: fix typo in dgram doc (Rich Trott) [#5114](https://github.com/nodejs/node/pull/5114)
* [[`abfb2f5864`](https://github.com/nodejs/node/commit/abfb2f5864)] - **doc**: fix link in cluster documentation (Timothy Gu) [#5068](https://github.com/nodejs/node/pull/5068)
* [[`8b040b5bb2`](https://github.com/nodejs/node/commit/8b040b5bb2)] - **doc**: fix minor typo in process doc (Prayag Verma) [#5018](https://github.com/nodejs/node/pull/5018)
* [[`47eebe1d80`](https://github.com/nodejs/node/commit/47eebe1d80)] - **doc**: fix typo in Readme.md (Prayag Verma) [#5017](https://github.com/nodejs/node/pull/5017)
* [[`2b97ff89a6`](https://github.com/nodejs/node/commit/2b97ff89a6)] - **doc**: minor improvement in OS docs (Alexander Makarenko) [#5006](https://github.com/nodejs/node/pull/5006)
* [[`9a5d58b89e`](https://github.com/nodejs/node/commit/9a5d58b89e)] - **doc**: improve styling consistency in VM docs (Alexander Makarenko) [#5005](https://github.com/nodejs/node/pull/5005)
* [[`960e1bab98`](https://github.com/nodejs/node/commit/960e1bab98)] - **doc**: minor improvement to HTTPS doc (Alexander Makarenko) [#5002](https://github.com/nodejs/node/pull/5002)
* [[`6048b011e8`](https://github.com/nodejs/node/commit/6048b011e8)] - **doc**: spell writable consistently (Peter Lyons) [#4954](https://github.com/nodejs/node/pull/4954)
* [[`7b8f904167`](https://github.com/nodejs/node/commit/7b8f904167)] - **doc**: update eol handling in readline (Kári Tristan Helgason) [#4927](https://github.com/nodejs/node/pull/4927)
* [[`83efd0d4d1`](https://github.com/nodejs/node/commit/83efd0d4d1)] - **doc**: add more details to process.env (Evan Lucas) [#4924](https://github.com/nodejs/node/pull/4924)
* [[`b2d2c0b588`](https://github.com/nodejs/node/commit/b2d2c0b588)] - **doc**: undo move http.IncomingMessage.statusMessage (Jeff Harris) [#4822](https://github.com/nodejs/node/pull/4822)
* [[`b091c41b53`](https://github.com/nodejs/node/commit/b091c41b53)] - **doc**: proper markdown escaping -> \_\_, \*, \_ (Robert Jefe Lindstaedt) [#4805](https://github.com/nodejs/node/pull/4805)
* [[`0887208290`](https://github.com/nodejs/node/commit/0887208290)] - **doc**: remove unnecessary bind(this) (Dmitriy Lazarev) [#4797](https://github.com/nodejs/node/pull/4797)
* [[`f3e3c70bca`](https://github.com/nodejs/node/commit/f3e3c70bca)] - **doc**: Update small error in LICENSE for npm (Kat Marchán) [#4872](https://github.com/nodejs/node/pull/4872)
* [[`e703b180b3`](https://github.com/nodejs/node/commit/e703b180b3)] - **doc,tools,test**: lint doc-based addon tests (Rich Trott) [#5427](https://github.com/nodejs/node/pull/5427)
* [[`0f3b8ca192`](https://github.com/nodejs/node/commit/0f3b8ca192)] - **fs**: refactor redeclared variables (Rich Trott) [#4959](https://github.com/nodejs/node/pull/4959)
* [[`152c6b6b8d`](https://github.com/nodejs/node/commit/152c6b6b8d)] - **http**: remove reference to onParserExecute (Tom Atkinson) [#4773](https://github.com/nodejs/node/pull/4773)
* [[`6a0571cd72`](https://github.com/nodejs/node/commit/6a0571cd72)] - **http**: do not emit `upgrade` on advertisement (Fedor Indutny) [#4337](https://github.com/nodejs/node/pull/4337)
* [[`567ced9ef0`](https://github.com/nodejs/node/commit/567ced9ef0)] - **(SEMVER-MINOR)** **http**: handle errors on idle sockets (José F. Romaniello) [#4482](https://github.com/nodejs/node/pull/4482)
* [[`de5177ccb8`](https://github.com/nodejs/node/commit/de5177ccb8)] - **https**: evict cached sessions on error (Fedor Indutny) [#4982](https://github.com/nodejs/node/pull/4982)
* [[`77a6036264`](https://github.com/nodejs/node/commit/77a6036264)] - **installer**: install the tick processor (Matt Loring) [#3032](https://github.com/nodejs/node/pull/3032)
* [[`ea16d8d7c5`](https://github.com/nodejs/node/commit/ea16d8d7c5)] - **lib**: remove string_decoder.js var redeclarations (Rich Trott) [#4978](https://github.com/nodejs/node/pull/4978)
* [[`1389660ab3`](https://github.com/nodejs/node/commit/1389660ab3)] - **lib**: scope loop variables (Rich Trott) [#4965](https://github.com/nodejs/node/pull/4965)
* [[`59255d7218`](https://github.com/nodejs/node/commit/59255d7218)] - **lib**: use arrow functions instead of bind (Minwoo Jung) [#3622](https://github.com/nodejs/node/pull/3622)
* [[`fd26960aab`](https://github.com/nodejs/node/commit/fd26960aab)] - **lib,test**: remove extra semicolons (Michaël Zasso) [#2205](https://github.com/nodejs/node/pull/2205)
* [[`9646d26ffd`](https://github.com/nodejs/node/commit/9646d26ffd)] - **module**: refactor redeclared variable (Rich Trott) [#4962](https://github.com/nodejs/node/pull/4962)
* [[`09311128e8`](https://github.com/nodejs/node/commit/09311128e8)] - **net**: use `_server` for internal book-keeping (Fedor Indutny) [#5262](https://github.com/nodejs/node/pull/5262)
* [[`824c402174`](https://github.com/nodejs/node/commit/824c402174)] - **net**: refactor redeclared variables (Rich Trott) [#4963](https://github.com/nodejs/node/pull/4963)
* [[`96f306f3cf`](https://github.com/nodejs/node/commit/96f306f3cf)] - **net**: move isLegalPort to internal/net (Evan Lucas) [#4882](https://github.com/nodejs/node/pull/4882)
* [[`78d64889bd`](https://github.com/nodejs/node/commit/78d64889bd)] - **node**: set process._eventsCount to 0 on startup (Evan Lucas) [#5208](https://github.com/nodejs/node/pull/5208)
* [[`7a2e8f4356`](https://github.com/nodejs/node/commit/7a2e8f4356)] - **process**: support symbol events (cjihrig) [#4798](https://github.com/nodejs/node/pull/4798)
* [[`c9e2dce247`](https://github.com/nodejs/node/commit/c9e2dce247)] - **querystring**: improve parse() performance (Brian White) [#4675](https://github.com/nodejs/node/pull/4675)
* [[`18542c41fe`](https://github.com/nodejs/node/commit/18542c41fe)] - **repl**: remove variable redeclaration (Rich Trott) [#4977](https://github.com/nodejs/node/pull/4977)
* [[`10be8dc360`](https://github.com/nodejs/node/commit/10be8dc360)] - **src**: force line buffering for stderr (Rich Trott) [#3701](https://github.com/nodejs/node/pull/3701)
* [[`7958664e85`](https://github.com/nodejs/node/commit/7958664e85)] - **src**: clean up usage of __proto__ (Jackson Tian) [#5069](https://github.com/nodejs/node/pull/5069)
* [[`4e0a0d51b3`](https://github.com/nodejs/node/commit/4e0a0d51b3)] - **src**: remove no longer relevant comments (Chris911) [#4843](https://github.com/nodejs/node/pull/4843)
* [[`51c8bc8abc`](https://github.com/nodejs/node/commit/51c8bc8abc)] - **src**: remove __builtin_bswap16 call (Ben Noordhuis) [#4290](https://github.com/nodejs/node/pull/4290)
* [[`5e1976e37c`](https://github.com/nodejs/node/commit/5e1976e37c)] - **src**: remove unused BITS_PER_LONG macro (Ben Noordhuis) [#4290](https://github.com/nodejs/node/pull/4290)
* [[`c18ef54d88`](https://github.com/nodejs/node/commit/c18ef54d88)] - **(SEMVER-MINOR)** **src**: add BE support to StringBytes::Encode() (Bryon Leung) [#3410](https://github.com/nodejs/node/pull/3410)
* [[`be9e7610b5`](https://github.com/nodejs/node/commit/be9e7610b5)] - **src,test,tools**: modify for more stringent linting (Rich Trott) [#5214](https://github.com/nodejs/node/pull/5214)
* [[`538c4756a7`](https://github.com/nodejs/node/commit/538c4756a7)] - **stream**: refactor redeclared variables (Rich Trott) [#4816](https://github.com/nodejs/node/pull/4816)
* [[`4fa22e4126`](https://github.com/nodejs/node/commit/4fa22e4126)] - **streams**: 5% throughput gain when sending small chunks (Matteo Collina) [#4354](https://github.com/nodejs/node/pull/4354)
* [[`b6bd87495f`](https://github.com/nodejs/node/commit/b6bd87495f)] - **test**: remove flaky mark for test-debug-no-context (Rich Trott) [#5317](https://github.com/nodejs/node/pull/5317)
* [[`7705360e35`](https://github.com/nodejs/node/commit/7705360e35)] - **test**: add test for https server close event (Braydon Fuller) [#5106](https://github.com/nodejs/node/pull/5106)
* [[`9d6623e1d1`](https://github.com/nodejs/node/commit/9d6623e1d1)] - **test**: use String.prototype.repeat() for clarity (Rich Trott) [#5311](https://github.com/nodejs/node/pull/5311)
* [[`18e3987e2e`](https://github.com/nodejs/node/commit/18e3987e2e)] - **test**: mitigate flaky test-debug-no-context (Rich Trott) [#5269](https://github.com/nodejs/node/pull/5269)
* [[`058db07ce8`](https://github.com/nodejs/node/commit/058db07ce8)] - **test**: refactor test-dgram-send-callback-recursive (Santiago Gimeno) [#5079](https://github.com/nodejs/node/pull/5079)
* [[`1647113d7a`](https://github.com/nodejs/node/commit/1647113d7a)] - **test**: refactor test-http-destroyed-socket-write2 (Santiago Gimeno) [#4970](https://github.com/nodejs/node/pull/4970)
* [[`07dc2b50e2`](https://github.com/nodejs/node/commit/07dc2b50e2)] - **test**: shorten path for bogus socket (Rich Trott) [#4478](https://github.com/nodejs/node/pull/4478)
* [[`47e7c8c359`](https://github.com/nodejs/node/commit/47e7c8c359)] - **test**: mark test-http-regr-gh-2928 flaky (Rich Trott) [#5280](https://github.com/nodejs/node/pull/5280)
* [[`9dbd66f7ef`](https://github.com/nodejs/node/commit/9dbd66f7ef)] - **test**: mark test-http-agent flaky (Rich Trott) [#5209](https://github.com/nodejs/node/pull/5209)
* [[`98049876b5`](https://github.com/nodejs/node/commit/98049876b5)] - **test**: minimal repl eval option test (Rich Trott) [#5192](https://github.com/nodejs/node/pull/5192)
* [[`ae3185b8ac`](https://github.com/nodejs/node/commit/ae3185b8ac)] - **test**: disable fs watch tests for AIX (Michael Dawson) [#5187](https://github.com/nodejs/node/pull/5187)
* [[`b639c3345b`](https://github.com/nodejs/node/commit/b639c3345b)] - **test**: fix child-process-fork-regr-gh-2847 again (Santiago Gimeno) [#5179](https://github.com/nodejs/node/pull/5179)
* [[`8be3afc474`](https://github.com/nodejs/node/commit/8be3afc474)] - **test**: fix flaky test-http-regr-gh-2928 (Rich Trott) [#5154](https://github.com/nodejs/node/pull/5154)
* [[`46dc12bdcc`](https://github.com/nodejs/node/commit/46dc12bdcc)] - **test**: enable to work pkcs12 test in FIPS mode (Shigeki Ohtsu) [#5150](https://github.com/nodejs/node/pull/5150)
* [[`e19b8ea692`](https://github.com/nodejs/node/commit/e19b8ea692)] - **test**: remove unneeded common.indirectInstanceOf() (Rich Trott) [#5149](https://github.com/nodejs/node/pull/5149)
* [[`6072d2e15e`](https://github.com/nodejs/node/commit/6072d2e15e)] - **test**: disable gh-5100 test when in FIPS mode (Fedor Indutny) [#5144](https://github.com/nodejs/node/pull/5144)
* [[`a8417a2787`](https://github.com/nodejs/node/commit/a8417a2787)] - **test**: fix flaky test-dgram-pingpong (Rich Trott) [#5125](https://github.com/nodejs/node/pull/5125)
* [[`9db67a6a44`](https://github.com/nodejs/node/commit/9db67a6a44)] - **test**: fix child-process-fork-regr-gh-2847 (Santiago Gimeno) [#5121](https://github.com/nodejs/node/pull/5121)
* [[`69150caedc`](https://github.com/nodejs/node/commit/69150caedc)] - **test**: don't run test-tick-processor.js on Aix (Michael Dawson) [#5093](https://github.com/nodejs/node/pull/5093)
* [[`4a492b96b1`](https://github.com/nodejs/node/commit/4a492b96b1)] - **test**: mark flaky tests on Raspberry Pi (Rich Trott) [#5082](https://github.com/nodejs/node/pull/5082)
* [[`4301f2cdc2`](https://github.com/nodejs/node/commit/4301f2cdc2)] - **test**: fix inconsistent styling in test-url (Brian White) [#5014](https://github.com/nodejs/node/pull/5014)
* [[`865baaed60`](https://github.com/nodejs/node/commit/865baaed60)] - **test**: fix redeclared vars in sequential tests (Rich Trott) [#4999](https://github.com/nodejs/node/pull/4999)
* [[`663e852c1b`](https://github.com/nodejs/node/commit/663e852c1b)] - **test**: pummel test fixes (Rich Trott) [#4998](https://github.com/nodejs/node/pull/4998)
* [[`72d38a4a38`](https://github.com/nodejs/node/commit/72d38a4a38)] - **test**: fix redeclared vars in test-vm-* (Rich Trott) [#4997](https://github.com/nodejs/node/pull/4997)
* [[`97ddfa2b6e`](https://github.com/nodejs/node/commit/97ddfa2b6e)] - **test**: fix redeclared vars in test-url (Rich Trott) [#4993](https://github.com/nodejs/node/pull/4993)
* [[`43d4db4314`](https://github.com/nodejs/node/commit/43d4db4314)] - **test**: fix redeclared test-util-* vars (Rich Trott) [#4994](https://github.com/nodejs/node/pull/4994)
* [[`88fae38d0c`](https://github.com/nodejs/node/commit/88fae38d0c)] - **test**: fix variable redeclarations (Rich Trott) [#4992](https://github.com/nodejs/node/pull/4992)
* [[`58595f146a`](https://github.com/nodejs/node/commit/58595f146a)] - **test**: fix redeclared test-path vars (Rich Trott) [#4991](https://github.com/nodejs/node/pull/4991)
* [[`2b711d51fa`](https://github.com/nodejs/node/commit/2b711d51fa)] - **test**: fix var redeclarations in test-os (Rich Trott) [#4990](https://github.com/nodejs/node/pull/4990)
* [[`bd9e2c31d6`](https://github.com/nodejs/node/commit/bd9e2c31d6)] - **test**: fix test-net-* variable redeclarations (Rich Trott) [#4989](https://github.com/nodejs/node/pull/4989)
* [[`d67ab81882`](https://github.com/nodejs/node/commit/d67ab81882)] - **test**: fix redeclared test-intl var (Rich Trott) [#4988](https://github.com/nodejs/node/pull/4988)
* [[`d6dbb2fae7`](https://github.com/nodejs/node/commit/d6dbb2fae7)] - **test**: fix redeclared test-http-* vars (Rich Trott) [#4987](https://github.com/nodejs/node/pull/4987)
* [[`ecaa89a8cb`](https://github.com/nodejs/node/commit/ecaa89a8cb)] - **test**: fix redeclared test-event-emitter-* vars (Rich Trott) [#4985](https://github.com/nodejs/node/pull/4985)
* [[`299c729371`](https://github.com/nodejs/node/commit/299c729371)] - **test**: remove redeclared var in test-domain (Rich Trott) [#4984](https://github.com/nodejs/node/pull/4984)
* [[`35a4a203bf`](https://github.com/nodejs/node/commit/35a4a203bf)] - **test**: remove var redeclarations in test-crypto-* (Rich Trott) [#4981](https://github.com/nodejs/node/pull/4981)
* [[`1d56b74af0`](https://github.com/nodejs/node/commit/1d56b74af0)] - **test**: remove test-cluster-* var redeclarations (Rich Trott) [#4980](https://github.com/nodejs/node/pull/4980)
* [[`0ce12cc1ec`](https://github.com/nodejs/node/commit/0ce12cc1ec)] - **test**: fix test-http-extra-response flakiness (Santiago Gimeno) [#4979](https://github.com/nodejs/node/pull/4979)
* [[`c6b4bf138c`](https://github.com/nodejs/node/commit/c6b4bf138c)] - **test**: scope redeclared vars in test-child-process* (Rich Trott) [#4944](https://github.com/nodejs/node/pull/4944)
* [[`7654c171c7`](https://github.com/nodejs/node/commit/7654c171c7)] - **test**: refactor switch (Rich Trott) [#4870](https://github.com/nodejs/node/pull/4870)
* [[`226dfef690`](https://github.com/nodejs/node/commit/226dfef690)] - **test**: add common.platformTimeout() to dgram test (Rich Trott) [#4938](https://github.com/nodejs/node/pull/4938)
* [[`fb14bac662`](https://github.com/nodejs/node/commit/fb14bac662)] - **test**: fix flaky cluster test on Windows 10 (Rich Trott) [#4934](https://github.com/nodejs/node/pull/4934)
* [[`f5d29d7ac4`](https://github.com/nodejs/node/commit/f5d29d7ac4)] - **test**: Add assertion for TLS peer certificate fingerprint (Alan Cohen) [#4923](https://github.com/nodejs/node/pull/4923)
* [[`618427cea6`](https://github.com/nodejs/node/commit/618427cea6)] - **test**: fix test-tls-zero-clear-in flakiness (Santiago Gimeno) [#4888](https://github.com/nodejs/node/pull/4888)
* [[`8700c39c70`](https://github.com/nodejs/node/commit/8700c39c70)] - **test**: fix irregular whitespace issue (Roman Reiss) [#4864](https://github.com/nodejs/node/pull/4864)
* [[`2b026c9d5a`](https://github.com/nodejs/node/commit/2b026c9d5a)] - **test**: fs.link() test runs on same device (Drew Folta) [#4861](https://github.com/nodejs/node/pull/4861)
* [[`80a637ac4d`](https://github.com/nodejs/node/commit/80a637ac4d)] - **test**: scope redeclared variable (Rich Trott) [#4854](https://github.com/nodejs/node/pull/4854)
* [[`8c4903d4ef`](https://github.com/nodejs/node/commit/8c4903d4ef)] - **test**: update arrow function style (cjihrig) [#4813](https://github.com/nodejs/node/pull/4813)
* [[`0a44e6a447`](https://github.com/nodejs/node/commit/0a44e6a447)] - **test**: mark test-tick-processor flaky (Rich Trott) [#4809](https://github.com/nodejs/node/pull/4809)
* [[`363460616c`](https://github.com/nodejs/node/commit/363460616c)] - **test**: refactor test-net-settimeout (Rich Trott) [#4799](https://github.com/nodejs/node/pull/4799)
* [[`6841d82c22`](https://github.com/nodejs/node/commit/6841d82c22)] - **test**: remove race condition in http flood test (Rich Trott) [#4793](https://github.com/nodejs/node/pull/4793)
* [[`b5bae32847`](https://github.com/nodejs/node/commit/b5bae32847)] - **test**: remove test-http-exit-delay (Rich Trott) [#4786](https://github.com/nodejs/node/pull/4786)
* [[`60514f9521`](https://github.com/nodejs/node/commit/60514f9521)] - **test**: refactor test-fs-watch (Rich Trott) [#4776](https://github.com/nodejs/node/pull/4776)
* [[`2a3a431119`](https://github.com/nodejs/node/commit/2a3a431119)] - **test**: fix `net-socket-timeout-unref` flakiness (Santiago Gimeno) [#4772](https://github.com/nodejs/node/pull/4772)
* [[`9e6f3632a1`](https://github.com/nodejs/node/commit/9e6f3632a1)] - **test**: remove Object.observe from tests (Vladimir Kurchatkin) [#4769](https://github.com/nodejs/node/pull/4769)
* [[`f78daa67b8`](https://github.com/nodejs/node/commit/f78daa67b8)] - **test**: make npm tests work on prerelease node versions (Kat Marchán) [#4960](https://github.com/nodejs/node/pull/4960)
* [[`1c03191b6a`](https://github.com/nodejs/node/commit/1c03191b6a)] - **test**: make npm tests work on prerelease node versions (Kat Marchán) [#4872](https://github.com/nodejs/node/pull/4872)
* [[`d9c22cc896`](https://github.com/nodejs/node/commit/d9c22cc896)] - **test,buffer**: refactor redeclarations (Rich Trott) [#4893](https://github.com/nodejs/node/pull/4893)
* [[`5c4960468a`](https://github.com/nodejs/node/commit/5c4960468a)] - **tls**: nullify `.ssl` on handle close (Fedor Indutny) [#5168](https://github.com/nodejs/node/pull/5168)
* [[`c0f5f01c9c`](https://github.com/nodejs/node/commit/c0f5f01c9c)] - **tls**: scope loop vars with let (Rich Trott) [#4853](https://github.com/nodejs/node/pull/4853)
* [[`c86627e0d1`](https://github.com/nodejs/node/commit/c86627e0d1)] - **(SEMVER-MINOR)** **tls**: add `options` argument to createSecurePair (Коренберг Марк) [#2441](https://github.com/nodejs/node/pull/2441)
* [[`c908ff36f4`](https://github.com/nodejs/node/commit/c908ff36f4)] - **tls_wrap**: reach error reporting for UV_EPROTO (Fedor Indutny) [#4885](https://github.com/nodejs/node/pull/4885)
* [[`cebe3b95e3`](https://github.com/nodejs/node/commit/cebe3b95e3)] - **tools**: run tick processor without forking (Matt Loring) [#4224](https://github.com/nodejs/node/pull/4224)
* [[`70d8827714`](https://github.com/nodejs/node/commit/70d8827714)] - **(SEMVER-MINOR)** **tools**: add --prof-process flag to node binary (Matt Loring) [#4021](https://github.com/nodejs/node/pull/4021)
* [[`a43b9291c7`](https://github.com/nodejs/node/commit/a43b9291c7)] - **tools**: replace obsolete ESLint rules (Rich Trott) [#5214](https://github.com/nodejs/node/pull/5214)
* [[`a89c6f58f1`](https://github.com/nodejs/node/commit/a89c6f58f1)] - **tools**: update ESLint to version 2.1.0 (Rich Trott) [#5214](https://github.com/nodejs/node/pull/5214)
* [[`789f62196a`](https://github.com/nodejs/node/commit/789f62196a)] - **tools**: remove obsolete lint rules (Rich Trott) [#5214](https://github.com/nodejs/node/pull/5214)
* [[`154772cfa8`](https://github.com/nodejs/node/commit/154772cfa8)] - **tools**: parse types into links in doc html gen (Claudio Rodriguez) [#4741](https://github.com/nodejs/node/pull/4741)
* [[`9237b6e38a`](https://github.com/nodejs/node/commit/9237b6e38a)] - **tools**: fix warning in doc parsing (Shigeki Ohtsu) [#4537](https://github.com/nodejs/node/pull/4537)
* [[`c653cc0c03`](https://github.com/nodejs/node/commit/c653cc0c03)] - **tools**: add recommended ES6 lint rules (Rich Trott) [#5210](https://github.com/nodejs/node/pull/5210)
* [[`993d9b7df0`](https://github.com/nodejs/node/commit/993d9b7df0)] - **tools**: add recommended linting rules (Rich Trott) [#5188](https://github.com/nodejs/node/pull/5188)
* [[`8423125223`](https://github.com/nodejs/node/commit/8423125223)] - **tools**: remove excessive comments from .eslintrc (Rich Trott) [#5151](https://github.com/nodejs/node/pull/5151)
* [[`4c687c98e4`](https://github.com/nodejs/node/commit/4c687c98e4)] - **tools**: enable no-proto rule for linter (Jackson Tian) [#5140](https://github.com/nodejs/node/pull/5140)
* [[`28e4e6f312`](https://github.com/nodejs/node/commit/28e4e6f312)] - **tools**: disallow mixed spaces and tabs for indents (Rich Trott) [#5135](https://github.com/nodejs/node/pull/5135)
* [[`50c6fe8604`](https://github.com/nodejs/node/commit/50c6fe8604)] - **tools**: alphabetize eslint stylistic issues section (Rich Trott)
* [[`ee594f1ed7`](https://github.com/nodejs/node/commit/ee594f1ed7)] - **tools**: lint for empty character classes in regex (Rich Trott) [#5115](https://github.com/nodejs/node/pull/5115)
* [[`bf0e239e99`](https://github.com/nodejs/node/commit/bf0e239e99)] - **tools**: lint for spacing around unary operators (Rich Trott) [#5063](https://github.com/nodejs/node/pull/5063)
* [[`6345acb792`](https://github.com/nodejs/node/commit/6345acb792)] - **tools**: enable no-redeclare rule for linter (Rich Trott) [#5047](https://github.com/nodejs/node/pull/5047)
* [[`1dae175b62`](https://github.com/nodejs/node/commit/1dae175b62)] - **tools**: fix redeclared vars in doc/json.js (Rich Trott) [#5047](https://github.com/nodejs/node/pull/5047)
* [[`d1d220a1cf`](https://github.com/nodejs/node/commit/d1d220a1cf)] - **tools**: apply linting to doc tools (Rich Trott) [#4973](https://github.com/nodejs/node/pull/4973)
* [[`eddde1f60c`](https://github.com/nodejs/node/commit/eddde1f60c)] - **tools**: fix detecting constructor for JSON doc (Timothy Gu) [#4966](https://github.com/nodejs/node/pull/4966)
* [[`bcb327c8dd`](https://github.com/nodejs/node/commit/bcb327c8dd)] - **tools**: add property types in JSON documentation (Timothy Gu) [#4884](https://github.com/nodejs/node/pull/4884)
* [[`9a06a4c116`](https://github.com/nodejs/node/commit/9a06a4c116)] - **tools**: enable assorted ESLint error rules (Roman Reiss) [#4864](https://github.com/nodejs/node/pull/4864)
* [[`38474cfd49`](https://github.com/nodejs/node/commit/38474cfd49)] - **tools**: add arrow function rules to eslint (cjihrig) [#4813](https://github.com/nodejs/node/pull/4813)
* [[`f898abaa4f`](https://github.com/nodejs/node/commit/f898abaa4f)] - **tools**: fix setting path containing an ampersand (Brian White) [#4804](https://github.com/nodejs/node/pull/4804)
* [[`d10bee8e79`](https://github.com/nodejs/node/commit/d10bee8e79)] - **tools**: enable no-extra-semi rule in eslint (Michaël Zasso) [#2205](https://github.com/nodejs/node/pull/2205)
* [[`01006392cf`](https://github.com/nodejs/node/commit/01006392cf)] - **tools,doc**: fix linting errors (Rich Trott) [#5161](https://github.com/nodejs/node/pull/5161)
* [[`57a5f8731a`](https://github.com/nodejs/node/commit/57a5f8731a)] - **url**: change scoping of variables with let (Kári Tristan Helgason) [#4867](https://github.com/nodejs/node/pull/4867)

<a id="4.3.2"></a>
## 2016-03-02, Version 4.3.2 'Argon' (LTS), @thealphanerd

This is a security release with only a single commit, an update to openssl due to a recent security advisory. You can read more about the security advisory on [the Node.js website](https://nodejs.org/en/blog/vulnerability/openssl-march-2016/)

### Notable changes

* **openssl**: Upgrade from 1.0.2f to 1.0.2g (Ben Noordhuis) [#5507](https://github.com/nodejs/node/pull/5507)
  - Fix a double-free defect in parsing malformed DSA keys that may potentially be used for DoS or memory corruption attacks. It is likely to be very difficult to use this defect for a practical attack and is therefore considered low severity for Node.js users. More info is available at [CVE-2016-0705](https://www.openssl.org/news/vulnerabilities.html#2016-0705).
  - Fix a defect that can cause memory corruption in certain very rare cases relating to the internal `BN_hex2bn()` and `BN_dec2bn()` functions. It is believed that Node.js is not invoking the code paths that use these functions so practical attacks via Node.js using this defect are _unlikely_ to be possible. More info is available at [CVE-2016-0797](https://www.openssl.org/news/vulnerabilities.html#2016-0797).
  - Fix a defect that makes the _[CacheBleed Attack](https://ssrg.nicta.com.au/projects/TS/cachebleed/)_ possible. This defect enables attackers to execute side-channel attacks leading to the potential recovery of entire RSA private keys. It only affects the Intel Sandy Bridge (and possibly older) microarchitecture when using hyper-threading. Newer microarchitectures, including Haswell, are unaffected. More info is available at [CVE-2016-0702](https://www.openssl.org/news/vulnerabilities.html#2016-0702).

## Commits

* [[`c133797d09`](https://github.com/nodejs/node/commit/c133797d09)] - **deps**: upgrade openssl to 1.0.2g (Ben Noordhuis) [#5507](https://github.com/nodejs/node/pull/5507)

<a id="4.3.1"></a>
## 2016-02-16, Version 4.3.1 'Argon' (LTS), @thealphanerd

### Notable changes

* **buffer**
  * make byteLength work with Buffer correctly (Jackson Tian)
    - [#4738](https://github.com/nodejs/node/pull/4738)
* **debugger**
  * guard against call from non-node context (Ben Noordhuis)
    - [#4328](https://github.com/nodejs/node/pull/4328)
    - fixes segfaults in debugger
  * do not incept debug context (Myles Borins)
    - [#4819](https://github.com/nodejs/node/pull/4819)
    - fixes crash in debugger when using util methods
* **deps**
  * update to http-parser 2.5.2 (James Snell)
    - [#5238](https://github.com/nodejs/node/pull/5238)

### Commits

* [[`748d2b4de1`](https://github.com/nodejs/node/commit/748d2b4de1)] - **buffer**: make byteLength work with Buffer correctly (Jackson Tian) [#4738](https://github.com/nodejs/node/pull/4738)
* [[`fb615bdaf4`](https://github.com/nodejs/node/commit/fb615bdaf4)] - **buffer**: remove unnecessary TODO comments (Peter Geiss) [#4719](https://github.com/nodejs/node/pull/4719)
* [[`b8213ba7e1`](https://github.com/nodejs/node/commit/b8213ba7e1)] - **cluster**: ignore queryServer msgs on disconnection (Santiago Gimeno) [#4465](https://github.com/nodejs/node/pull/4465)
* [[`f8a676ed59`](https://github.com/nodejs/node/commit/f8a676ed59)] - **cluster**: fix race condition setting suicide prop (Santiago Gimeno) [#4349](https://github.com/nodejs/node/pull/4349)
* [[`9d4a226dad`](https://github.com/nodejs/node/commit/9d4a226dad)] - **crypto**: clear error stack in ECDH::Initialize (Fedor Indutny) [#4689](https://github.com/nodejs/node/pull/4689)
* [[`583f3347d8`](https://github.com/nodejs/node/commit/583f3347d8)] - **debugger**: remove variable redeclarations (Rich Trott) [#4633](https://github.com/nodejs/node/pull/4633)
* [[`667f7a7ab3`](https://github.com/nodejs/node/commit/667f7a7ab3)] - **debugger**: guard against call from non-node context (Ben Noordhuis) [#4328](https://github.com/nodejs/node/pull/4328)
* [[`188cff3c31`](https://github.com/nodejs/node/commit/188cff3c31)] - **deps**: update to http-parser 2.5.2 (James Snell) [#5238](https://github.com/nodejs/node/pull/5238)
* [[`6e829b44e3`](https://github.com/nodejs/node/commit/6e829b44e3)] - **dgram**: prevent disabled optimization of bind() (Brian White) [#4613](https://github.com/nodejs/node/pull/4613)
* [[`c3956d05b1`](https://github.com/nodejs/node/commit/c3956d05b1)] - **doc**: update list of personal traits in CoC (Kat Marchán) [#4801](https://github.com/nodejs/node/pull/4801)
* [[`39cb69ca21`](https://github.com/nodejs/node/commit/39cb69ca21)] - **doc**: style fixes for the TOC (Roman Reiss) [#4748](https://github.com/nodejs/node/pull/4748)
* [[`cb5986da81`](https://github.com/nodejs/node/commit/cb5986da81)] - **doc**: add `servername` parameter docs (Alexander Makarenko) [#4729](https://github.com/nodejs/node/pull/4729)
* [[`91066b5f34`](https://github.com/nodejs/node/commit/91066b5f34)] - **doc**: update branch-diff arguments in release doc (Rod Vagg) [#4691](https://github.com/nodejs/node/pull/4691)
* [[`9ca24de41d`](https://github.com/nodejs/node/commit/9ca24de41d)] - **doc**: add docs for more stream options (zoubin) [#4639](https://github.com/nodejs/node/pull/4639)
* [[`437d0e336d`](https://github.com/nodejs/node/commit/437d0e336d)] - **doc**: mention that http.Server inherits from net.Server (Ryan Sobol) [#4455](https://github.com/nodejs/node/pull/4455)
* [[`393e569160`](https://github.com/nodejs/node/commit/393e569160)] - **doc**: copyedit setTimeout() documentation (Rich Trott) [#4434](https://github.com/nodejs/node/pull/4434)
* [[`e2a682ecc3`](https://github.com/nodejs/node/commit/e2a682ecc3)] - **doc**: fix formatting in process.markdown (Rich Trott) [#4433](https://github.com/nodejs/node/pull/4433)
* [[`75b0ea85bd`](https://github.com/nodejs/node/commit/75b0ea85bd)] - **doc**: add path property to Write/ReadStream in fs.markdown (Claudio Rodriguez) [#4368](https://github.com/nodejs/node/pull/4368)
* [[`48c2783421`](https://github.com/nodejs/node/commit/48c2783421)] - **doc**: add docs working group (Bryan English) [#4244](https://github.com/nodejs/node/pull/4244)
* [[`c0432e9f56`](https://github.com/nodejs/node/commit/c0432e9f56)] - **doc**: restore ICU third-party software licenses (Richard Lau) [#4762](https://github.com/nodejs/node/pull/4762)
* [[`36a4159dab`](https://github.com/nodejs/node/commit/36a4159dab)] - **doc**: rebuild LICENSE using tools/license-builder.sh (Rod Vagg) [#4194](https://github.com/nodejs/node/pull/4194)
* [[`a2998a1bce`](https://github.com/nodejs/node/commit/a2998a1bce)] - **gitignore**: never ignore debug module (Michaël Zasso) [#2286](https://github.com/nodejs/node/pull/2286)
* [[`661b2557d9`](https://github.com/nodejs/node/commit/661b2557d9)] - **http**: remove variable redeclaration (Rich Trott) [#4612](https://github.com/nodejs/node/pull/4612)
* [[`1bb2967d48`](https://github.com/nodejs/node/commit/1bb2967d48)] - **http**: fix non-string header value concatenation (Brian White) [#4460](https://github.com/nodejs/node/pull/4460)
* [[`15ed64e34c`](https://github.com/nodejs/node/commit/15ed64e34c)] - **lib**: fix style issues after eslint update (Michaël Zasso) [nodejs/io.js#2286](https://github.com/nodejs/io.js/pull/2286)
* [[`2e92a1a6b4`](https://github.com/nodejs/node/commit/2e92a1a6b4)] - **module**: move unnecessary work for early return (Andres Suarez) [#3579](https://github.com/nodejs/node/pull/3579)
* [[`40c8e6d75d`](https://github.com/nodejs/node/commit/40c8e6d75d)] - **net**: remove hot path comment from connect (Evan Lucas) [#4648](https://github.com/nodejs/node/pull/4648)
* [[`8ed0c1c22c`](https://github.com/nodejs/node/commit/8ed0c1c22c)] - **net**: fix dns lookup for android (Josh Dague) [#4580](https://github.com/nodejs/node/pull/4580)
* [[`15fa555204`](https://github.com/nodejs/node/commit/15fa555204)] - **net, doc**: fix line wrapping lint in net.js (James M Snell) [#4588](https://github.com/nodejs/node/pull/4588)
* [[`1b070e48e0`](https://github.com/nodejs/node/commit/1b070e48e0)] - **node_contextify**: do not incept debug context (Myles Borins) [#4815](https://github.com/nodejs/node/issues/4815)
* [[`4fbcb47fe9`](https://github.com/nodejs/node/commit/4fbcb47fe9)] - **readline**: Remove XXX and output debuglog (Kohei TAKATA) [#4690](https://github.com/nodejs/node/pull/4690)
* [[`26f02405d0`](https://github.com/nodejs/node/commit/26f02405d0)] - **repl**: make sure historyPath is trimmed (Evan Lucas) [#4539](https://github.com/nodejs/node/pull/4539)
* [[`5990ba2a0a`](https://github.com/nodejs/node/commit/5990ba2a0a)] - **src**: remove redeclarations of variables (Rich Trott) [#4605](https://github.com/nodejs/node/pull/4605)
* [[`c41ed59dbc`](https://github.com/nodejs/node/commit/c41ed59dbc)] - **src**: don't check failure with ERR_peek_error() (Ben Noordhuis) [#4731](https://github.com/nodejs/node/pull/4731)
* [[`d71f9992f9`](https://github.com/nodejs/node/commit/d71f9992f9)] - **stream**: remove useless if test in transform (zoubin) [#4617](https://github.com/nodejs/node/pull/4617)
* [[`f205e9920e`](https://github.com/nodejs/node/commit/f205e9920e)] - **test**: fix tls-no-rsa-key flakiness (Santiago Gimeno) [#4043](https://github.com/nodejs/node/pull/4043)
* [[`447347cd62`](https://github.com/nodejs/node/commit/447347cd62)] - **test**: fix issues for space-in-parens ESLint rule (Roman Reiss) [#4753](https://github.com/nodejs/node/pull/4753)
* [[`be8274508c`](https://github.com/nodejs/node/commit/be8274508c)] - **test**: improve test-cluster-disconnect-suicide-race (Rich Trott) [#4739](https://github.com/nodejs/node/pull/4739)
* [[`0178001163`](https://github.com/nodejs/node/commit/0178001163)] - **test**: make test-cluster-disconnect-leak reliable (Rich Trott) [#4736](https://github.com/nodejs/node/pull/4736)
* [[`d615757da2`](https://github.com/nodejs/node/commit/d615757da2)] - **test**: fix flaky test-net-socket-local-address (cjihrig) [#4650](https://github.com/nodejs/node/pull/4650)
* [[`baa0a3dff5`](https://github.com/nodejs/node/commit/baa0a3dff5)] - **test**: fix race in test-net-server-pause-on-connect (Rich Trott) [#4637](https://github.com/nodejs/node/pull/4637)
* [[`909b5167cb`](https://github.com/nodejs/node/commit/909b5167cb)] - **test**: remove 1 second delay from test (Rich Trott) [#4616](https://github.com/nodejs/node/pull/4616)
* [[`8ea76608ed`](https://github.com/nodejs/node/commit/8ea76608ed)] - **test**: move resource intensive tests to sequential (Rich Trott) [#4615](https://github.com/nodejs/node/pull/4615)
* [[`7afcdd358e`](https://github.com/nodejs/node/commit/7afcdd358e)] - **test**: require common module only once (Rich Trott) [#4611](https://github.com/nodejs/node/pull/4611)
* [[`0e02eb0bbe`](https://github.com/nodejs/node/commit/0e02eb0bbe)] - **test**: only include http module once (Rich Trott) [#4606](https://github.com/nodejs/node/pull/4606)
* [[`34d9e48bb6`](https://github.com/nodejs/node/commit/34d9e48bb6)] - **test**: fix `http-upgrade-client` flakiness (Santiago Gimeno) [#4602](https://github.com/nodejs/node/pull/4602)
* [[`556703d531`](https://github.com/nodejs/node/commit/556703d531)] - **test**: fix flaky unrefed timers test (Rich Trott) [#4599](https://github.com/nodejs/node/pull/4599)
* [[`3d5bc69796`](https://github.com/nodejs/node/commit/3d5bc69796)] - **test**: fix `http-upgrade-agent` flakiness (Santiago Gimeno) [#4520](https://github.com/nodejs/node/pull/4520)
* [[`ec24d3767b`](https://github.com/nodejs/node/commit/ec24d3767b)] - **test**: fix flaky test-cluster-shared-leak (Rich Trott) [#4510](https://github.com/nodejs/node/pull/4510)
* [[`a256790327`](https://github.com/nodejs/node/commit/a256790327)] - **test**: fix flaky cluster-net-send (Brian White) [#4444](https://github.com/nodejs/node/pull/4444)
* [[`6809c2be1a`](https://github.com/nodejs/node/commit/6809c2be1a)] - **test**: fix flaky child-process-fork-regr-gh-2847 (Brian White) [#4442](https://github.com/nodejs/node/pull/4442)
* [[`e6448aa36b`](https://github.com/nodejs/node/commit/e6448aa36b)] - **test**: use addon.md block headings as test dir names (Rod Vagg) [#4412](https://github.com/nodejs/node/pull/4412)
* [[`305d340fca`](https://github.com/nodejs/node/commit/305d340fca)] - **test**: test each block in addon.md contains js & cc (Rod Vagg) [#4411](https://github.com/nodejs/node/pull/4411)
* [[`f213406575`](https://github.com/nodejs/node/commit/f213406575)] - **test**: fix tls-multi-key race condition (Santiago Gimeno) [#3966](https://github.com/nodejs/node/pull/3966)
* [[`607f545568`](https://github.com/nodejs/node/commit/607f545568)] - **test**: fix style issues after eslint update (Michaël Zasso) [nodejs/io.js#2286](https://github.com/nodejs/io.js/pull/2286)
* [[`aefb20a94f`](https://github.com/nodejs/node/commit/aefb20a94f)] - **tls**: copy client CAs and cert store on CertCb (Fedor Indutny) [#3537](https://github.com/nodejs/node/pull/3537)
* [[`7821b3e305`](https://github.com/nodejs/node/commit/7821b3e305)] - **tls_legacy**: do not read on OpenSSL's stack (Fedor Indutny) [#4624](https://github.com/nodejs/node/pull/4624)
* [[`b66db49f94`](https://github.com/nodejs/node/commit/b66db49f94)] - **tools**: add support for subkeys in release tools (Myles Borins) [#4807](https://github.com/nodejs/node/pull/4807)
* [[`837ebd1985`](https://github.com/nodejs/node/commit/837ebd1985)] - **tools**: enable space-in-parens ESLint rule (Roman Reiss) [#4753](https://github.com/nodejs/node/pull/4753)
* [[`066d5e7da2`](https://github.com/nodejs/node/commit/066d5e7da2)] - **tools**: fix style issue after eslint update (Michaël Zasso) [nodejs/io.js#2286](https://github.com/nodejs/io.js/pull/2286)
* [[`b20ea69f46`](https://github.com/nodejs/node/commit/b20ea69f46)] - **tools**: update eslint config (Michaël Zasso) [nodejs/io.js#2286](https://github.com/nodejs/io.js/pull/2286)
* [[`2e0352d50c`](https://github.com/nodejs/node/commit/2e0352d50c)] - **tools**: update eslint to v1.10.3 (Michaël Zasso) [nodejs/io.js#2286](https://github.com/nodejs/io.js/pull/2286)
* [[`c96800a432`](https://github.com/nodejs/node/commit/c96800a432)] - **tools**: fix license-builder.sh for ICU (Richard Lau) [#4762](https://github.com/nodejs/node/pull/4762)
* [[`720b03dca7`](https://github.com/nodejs/node/commit/720b03dca7)] - **tools**: add license-builder.sh to construct LICENSE (Rod Vagg) [#4194](https://github.com/nodejs/node/pull/4194)

<a id="4.3.0"></a>
## 2016-02-09, Version 4.3.0 'Argon' (LTS), @jasnell

This is an important security release. All Node.js users should consult the security release summary at nodejs.org for details on patched vulnerabilities.

Note that this release includes a non-backward compatible change to address a security issue. This change increases the version of the LTS v4.x line to v4.3.0. There will be *no further updates* to v4.2.x.

### Notable changes

* **http**: fix defects in HTTP header parsing for requests and responses that can allow request smuggling (CVE-2016-2086) or response splitting (CVE-2016-2216). HTTP header parsing now aligns more closely with the HTTP spec including restricting the acceptable characters.
* **http-parser**: upgrade from 2.5.0 to 2.5.1
* **openssl**: upgrade from 1.0.2e to 1.0.2f. To mitigate against the Logjam attack, TLS clients now reject Diffie-Hellman handshakes with parameters shorter than 1024-bits, up from the previous limit of 768-bits.
* **src**:
  - introduce new `--security-revert={cvenum}` command line flag for selective reversion of specific CVE fixes
  - allow the fix for CVE-2016-2216 to be selectively reverted using `--security-revert=CVE-2016-2216`

### Commits

* [[`d94f864abd`](https://github.com/nodejs/node/commit/d94f864abd)] - **deps**: add -no_rand_screen to openssl s_client (Shigeki Ohtsu) [#1836](https://github.com/nodejs/node/pull/1836)
* [[`136295e202`](https://github.com/nodejs/node/commit/136295e202)] - **deps**: upgrade openssl sources to 1.0.2f (Myles Borins) [#4961](https://github.com/nodejs/node/pull/4961)
* [[`0eae95eae3`](https://github.com/nodejs/node/commit/0eae95eae3)] - **(SEMVER-MINOR)** **deps**: update http-parser to version 2.5.1 (James M Snell)
* [[`cf2b714b02`](https://github.com/nodejs/node/commit/cf2b714b02)] - **(SEMVER-MINOR)** **http**: strictly forbid invalid characters from headers (James M Snell)
* [[`49ae2e0334`](https://github.com/nodejs/node/commit/49ae2e0334)] - **src**: avoid compiler warning in node_revert.cc (James M Snell)
* [[`da3750f981`](https://github.com/nodejs/node/commit/da3750f981)] - **(SEMVER-MAJOR)** **src**: add --security-revert command line flag (James M Snell)

<a id="4.2.6"></a>
## 2016-01-21, Version 4.2.6 'Argon' (LTS), @TheAlphaNerd

### Notable changes

* Fix regression in debugger and profiler functionality

### Known issues

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`1408f7abb1`](https://github.com/nodejs/node/commit/1408f7abb1)] - **module,src**: do not wrap modules with -1 lineOffset (cjihrig) [#4298](https://github.com/nodejs/node/pull/4298)
* [[`1f8e1472cc`](https://github.com/nodejs/node/commit/1f8e1472cc)] - **test**: add test for debugging one line files (cjihrig) [#4298](https://github.com/nodejs/node/pull/4298)

<a id="4.2.5"></a>
## 2016-01-20, Version 4.2.5 'Argon' (LTS), @TheAlphaNerd

Maintenance update.

### Notable changes

* **assert**
  * accommodate ES6 classes that extend Error (Rich Trott) [#4166](https://github.com/nodejs/node/pull/4166)
* **build**
  * add "--partly-static" build options (Super Zheng) [#4152](https://github.com/nodejs/node/pull/4152)
* **deps**
  * backport 066747e from upstream V8 (Ali Ijaz Sheikh) [#4655](https://github.com/nodejs/node/pull/4655)
  * backport 200315c from V8 upstream (Vladimir Kurchatkin) [#4128](https://github.com/nodejs/node/pull/4128)
  * upgrade libuv to 1.8.0 (Saúl Ibarra Corretgé)
* **docs**
  * various updates landed in 70 different commits!
* **repl**
  * attach location info to syntax errors (cjihrig) [#4013](https://github.com/nodejs/node/pull/4013)
  * display error message when loading directory (Prince J Wesley) [#4170](https://github.com/nodejs/node/pull/4170)
* **tests**
  * various updates landed in over 50 commits
* **tools**
  * add tap output to cpplint (Johan Bergström) [#3448](https://github.com/nodejs/node/pull/3448)
* **util**
  * allow lookup of hidden values (cjihrig) [#3988](https://github.com/nodejs/node/pull/3988)

### Known issues

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`87181cd74c`](https://github.com/nodejs/node/commit/87181cd74c)] - **assert**: accommodate ES6 classes that extend Error (Rich Trott) [#4166](https://github.com/nodejs/node/pull/4166)
* [[`901172a783`](https://github.com/nodejs/node/commit/901172a783)] - **assert**: typed array deepequal performance fix (Claudio Rodriguez) [#4330](https://github.com/nodejs/node/pull/4330)
* [[`55336810ee`](https://github.com/nodejs/node/commit/55336810ee)] - **async_wrap**: call callback in destructor (Trevor Norris) [#3461](https://github.com/nodejs/node/pull/3461)
* [[`a8b45e9e96`](https://github.com/nodejs/node/commit/a8b45e9e96)] - **async_wrap**: new instances get uid (Trevor Norris) [#3461](https://github.com/nodejs/node/pull/3461)
* [[`49f16d77c4`](https://github.com/nodejs/node/commit/49f16d77c4)] - **async_wrap**: allow some hooks to be optional (Trevor Norris) [#3461](https://github.com/nodejs/node/pull/3461)
* [[`44ee33f945`](https://github.com/nodejs/node/commit/44ee33f945)] - **buffer**: refactor create buffer (Jackson Tian) [#4340](https://github.com/nodejs/node/pull/4340)
* [[`138d004ac0`](https://github.com/nodejs/node/commit/138d004ac0)] - **buffer**: faster case for create Buffer from new Buffer(0) (Jackson Tian) [#4326](https://github.com/nodejs/node/pull/4326)
* [[`c6dc2a1609`](https://github.com/nodejs/node/commit/c6dc2a1609)] - **buffer**: Prevent Buffer constructor deopt (Bryce Baril) [#4158](https://github.com/nodejs/node/pull/4158)
* [[`a320045e68`](https://github.com/nodejs/node/commit/a320045e68)] - **buffer**: default to UTF8 in byteLength() (Tom Gallacher) [#4010](https://github.com/nodejs/node/pull/4010)
* [[`c5f71ac771`](https://github.com/nodejs/node/commit/c5f71ac771)] - **build**: add "--partly-static" build options (Super Zheng) [#4152](https://github.com/nodejs/node/pull/4152)
* [[`e6c25335ea`](https://github.com/nodejs/node/commit/e6c25335ea)] - **build**: omit -gline-tables-only for --enable-asan (Ben Noordhuis) [#3680](https://github.com/nodejs/node/pull/3680)
* [[`80b4ba286c`](https://github.com/nodejs/node/commit/80b4ba286c)] - **build**: Updates for AIX npm support - part 1 (Michael Dawson) [#3114](https://github.com/nodejs/node/pull/3114)
* [[`35e32985ca`](https://github.com/nodejs/node/commit/35e32985ca)] - **child_process**: guard against race condition (Rich Trott) [#4418](https://github.com/nodejs/node/pull/4418)
* [[`48564204f0`](https://github.com/nodejs/node/commit/48564204f0)] - **child_process**: flush consuming streams (Dave) [#4071](https://github.com/nodejs/node/pull/4071)
* [[`481d59a74c`](https://github.com/nodejs/node/commit/481d59a74c)] - **configure**: fix arm vfpv2 (Jörg Krause) [#4203](https://github.com/nodejs/node/pull/4203)
* [[`d19da6638d`](https://github.com/nodejs/node/commit/d19da6638d)] - **crypto**: load PFX chain the same way as regular one (Fedor Indutny) [#4165](https://github.com/nodejs/node/pull/4165)
* [[`b8e75de1f3`](https://github.com/nodejs/node/commit/b8e75de1f3)] - **crypto**: fix native module compilation with FIPS (Stefan Budeanu) [#4023](https://github.com/nodejs/node/pull/4023)
* [[`b7c3fb7f75`](https://github.com/nodejs/node/commit/b7c3fb7f75)] - **crypto**: disable crypto.createCipher in FIPS mode (Stefan Budeanu) [#3754](https://github.com/nodejs/node/pull/3754)
* [[`31b4091a1e`](https://github.com/nodejs/node/commit/31b4091a1e)] - **debugger**: also exit when the repl emits 'exit' (Felix Böhm) [#2369](https://github.com/nodejs/node/pull/2369)
* [[`9baa5618f5`](https://github.com/nodejs/node/commit/9baa5618f5)] - **deps**: backport 066747e from upstream V8 (Ali Ijaz Sheikh) [#4655](https://github.com/nodejs/node/pull/4655)
* [[`c3a9d8a62e`](https://github.com/nodejs/node/commit/c3a9d8a62e)] - **deps**: backport 200315c from V8 upstream (Vladimir Kurchatkin) [#4128](https://github.com/nodejs/node/pull/4128)
* [[`1ebb0c0fdf`](https://github.com/nodejs/node/commit/1ebb0c0fdf)] - **deps**: upgrade libuv to 1.8.0 (Saúl Ibarra Corretgé) [#4276](https://github.com/nodejs/node/pull/4276)
* [[`253fe3e7c8`](https://github.com/nodejs/node/commit/253fe3e7c8)] - **dns**: remove nonexistant exports.ADNAME (Roman Reiss) [#3051](https://github.com/nodejs/node/pull/3051)
* [[`8c2b65ad82`](https://github.com/nodejs/node/commit/8c2b65ad82)] - **doc**: clarify protocol default in http.request() (cjihrig) [#4714](https://github.com/nodejs/node/pull/4714)
* [[`33e72e135f`](https://github.com/nodejs/node/commit/33e72e135f)] - **doc**: update links to use https where possible (jpersson) [#4054](https://github.com/nodejs/node/pull/4054)
* [[`5f4aa79410`](https://github.com/nodejs/node/commit/5f4aa79410)] - **doc**: clarify explanation of first stream section (Vitor Cortez) [#4234](https://github.com/nodejs/node/pull/4234)
* [[`295ca5bfb2`](https://github.com/nodejs/node/commit/295ca5bfb2)] - **doc**: add branch-diff example to releases.md (Myles Borins) [#4636](https://github.com/nodejs/node/pull/4636)
* [[`18f5cd8710`](https://github.com/nodejs/node/commit/18f5cd8710)] - **doc**: update stylesheet to match frontpage (Roman Reiss) [#4621](https://github.com/nodejs/node/pull/4621)
* [[`2f40715f08`](https://github.com/nodejs/node/commit/2f40715f08)] - **doc**: adds usage of readline line-by-line parsing (Robert Jefe Lindstaedt) [#4609](https://github.com/nodejs/node/pull/4609)
* [[`5b45a464ee`](https://github.com/nodejs/node/commit/5b45a464ee)] - **doc**: document http's server.listen return value (Sequoia McDowell) [#4590](https://github.com/nodejs/node/pull/4590)
* [[`bd31740339`](https://github.com/nodejs/node/commit/bd31740339)] - **doc**: label http.IncomingMessage as a Class (Sequoia McDowell) [#4589](https://github.com/nodejs/node/pull/4589)
* [[`bcd2cbbb93`](https://github.com/nodejs/node/commit/bcd2cbbb93)] - **doc**: fix description about the latest-codename (Minwoo Jung) [#4583](https://github.com/nodejs/node/pull/4583)
* [[`0b12bcb35d`](https://github.com/nodejs/node/commit/0b12bcb35d)] - **doc**: add Evan Lucas to Release Team (Evan Lucas) [#4579](https://github.com/nodejs/node/pull/4579)
* [[`e20b1f6f10`](https://github.com/nodejs/node/commit/e20b1f6f10)] - **doc**: add Myles Borins to Release Team (Myles Borins) [#4578](https://github.com/nodejs/node/pull/4578)
* [[`54977e63eb`](https://github.com/nodejs/node/commit/54977e63eb)] - **doc**: add missing backtick for readline (Brian White) [#4549](https://github.com/nodejs/node/pull/4549)
* [[`5d6bed895c`](https://github.com/nodejs/node/commit/5d6bed895c)] - **doc**: bring releases.md up to date (cjihrig) [#4540](https://github.com/nodejs/node/pull/4540)
* [[`0cd2252e85`](https://github.com/nodejs/node/commit/0cd2252e85)] - **doc**: fix numbering in stream.markdown (Richard Sun) [#4538](https://github.com/nodejs/node/pull/4538)
* [[`8574d91f27`](https://github.com/nodejs/node/commit/8574d91f27)] - **doc**: stronger suggestion for userland assert (Wyatt Preul) [#4535](https://github.com/nodejs/node/pull/4535)
* [[`a7bcf8b84d`](https://github.com/nodejs/node/commit/a7bcf8b84d)] - **doc**: close backtick in process.title description (Dave) [#4534](https://github.com/nodejs/node/pull/4534)
* [[`0ceb3148b0`](https://github.com/nodejs/node/commit/0ceb3148b0)] - **doc**: improvements to events.markdown copy (James M Snell) [#4468](https://github.com/nodejs/node/pull/4468)
* [[`bf56d509b9`](https://github.com/nodejs/node/commit/bf56d509b9)] - **doc**: explain ClientRequest#setTimeout time unit (Ben Ripkens) [#4458](https://github.com/nodejs/node/pull/4458)
* [[`d927c51be3`](https://github.com/nodejs/node/commit/d927c51be3)] - **doc**: improvements to errors.markdown copy (James M Snell) [#4454](https://github.com/nodejs/node/pull/4454)
* [[`ceea6df581`](https://github.com/nodejs/node/commit/ceea6df581)] - **doc**: improvements to dns.markdown copy (James M Snell) [#4449](https://github.com/nodejs/node/pull/4449)
* [[`506f2f8ed1`](https://github.com/nodejs/node/commit/506f2f8ed1)] - **doc**: add anchors for _transform _flush _writev in stream.markdown (iamchenxin) [#4448](https://github.com/nodejs/node/pull/4448)
* [[`74bcad0b78`](https://github.com/nodejs/node/commit/74bcad0b78)] - **doc**: improvements to dgram.markdown copy (James M Snell) [#4437](https://github.com/nodejs/node/pull/4437)
* [[`e244d560c9`](https://github.com/nodejs/node/commit/e244d560c9)] - **doc**: improvements to debugger.markdown copy (James M Snell) [#4436](https://github.com/nodejs/node/pull/4436)
* [[`df7e1281a5`](https://github.com/nodejs/node/commit/df7e1281a5)] - **doc**: improvements to console.markdown copy (James M Snell) [#4428](https://github.com/nodejs/node/pull/4428)
* [[`abb17cc6c1`](https://github.com/nodejs/node/commit/abb17cc6c1)] - **doc**: fix spelling error in lib/url.js comment (Nik Nyby) [#4390](https://github.com/nodejs/node/pull/4390)
* [[`823269db2d`](https://github.com/nodejs/node/commit/823269db2d)] - **doc**: improve assert.markdown copy (James M Snell) [#4360](https://github.com/nodejs/node/pull/4360)
* [[`2b1804f6cb`](https://github.com/nodejs/node/commit/2b1804f6cb)] - **doc**: copyedit releases.md (Rich Trott) [#4384](https://github.com/nodejs/node/pull/4384)
* [[`2b142fd876`](https://github.com/nodejs/node/commit/2b142fd876)] - **doc**: catch the WORKING_GROUPS.md bootstrap docs up to date (James M Snell) [#4367](https://github.com/nodejs/node/pull/4367)
* [[`ed87873de3`](https://github.com/nodejs/node/commit/ed87873de3)] - **doc**: fix link in addons.markdown (Nicholas Young) [#4331](https://github.com/nodejs/node/pull/4331)
* [[`fe693b7a4f`](https://github.com/nodejs/node/commit/fe693b7a4f)] - **doc**: Typo in buffer.markdown referencing buf.write() (chrisjohn404) [#4324](https://github.com/nodejs/node/pull/4324)
* [[`764df2166e`](https://github.com/nodejs/node/commit/764df2166e)] - **doc**: document the cache parameter for fs.realpathSync (Jackson Tian) [#4285](https://github.com/nodejs/node/pull/4285)
* [[`61f91b2f29`](https://github.com/nodejs/node/commit/61f91b2f29)] - **doc**: fix, modernize examples in docs (James M Snell) [#4282](https://github.com/nodejs/node/pull/4282)
* [[`d87ad302ce`](https://github.com/nodejs/node/commit/d87ad302ce)] - **doc**: clarify error events in HTTP module documentation (Lenny Markus) [#4275](https://github.com/nodejs/node/pull/4275)
* [[`7983577e41`](https://github.com/nodejs/node/commit/7983577e41)] - **doc**: fix improper http.get sample code (Hideki Yamamura) [#4263](https://github.com/nodejs/node/pull/4263)
* [[`6c30d087e5`](https://github.com/nodejs/node/commit/6c30d087e5)] - **doc**: Fixing broken links to the v8 wiki (Tom Gallacher) [#4241](https://github.com/nodejs/node/pull/4241)
* [[`cf214e56e4`](https://github.com/nodejs/node/commit/cf214e56e4)] - **doc**: move description of 'equals' method to right place (janriemer) [#4227](https://github.com/nodejs/node/pull/4227)
* [[`fb8e8dbb92`](https://github.com/nodejs/node/commit/fb8e8dbb92)] - **doc**: copyedit console doc (Rich Trott) [#4225](https://github.com/nodejs/node/pull/4225)
* [[`4ccf04c229`](https://github.com/nodejs/node/commit/4ccf04c229)] - **doc**: add mcollina to collaborators (Matteo Collina) [#4220](https://github.com/nodejs/node/pull/4220)
* [[`59654c21d4`](https://github.com/nodejs/node/commit/59654c21d4)] - **doc**: add rmg to collaborators (Ryan Graham) [#4219](https://github.com/nodejs/node/pull/4219)
* [[`bfe1a6bd2b`](https://github.com/nodejs/node/commit/bfe1a6bd2b)] - **doc**: add calvinmetcalf to collaborators (Calvin Metcalf) [#4218](https://github.com/nodejs/node/pull/4218)
* [[`5140c404ae`](https://github.com/nodejs/node/commit/5140c404ae)] - **doc**: harmonize description of `ca` argument (Ben Noordhuis) [#4213](https://github.com/nodejs/node/pull/4213)
* [[`2e642051cf`](https://github.com/nodejs/node/commit/2e642051cf)] - **doc**: copyedit child_process doc (Rich Trott) [#4188](https://github.com/nodejs/node/pull/4188)
* [[`7920f8dbde`](https://github.com/nodejs/node/commit/7920f8dbde)] - **doc**: copyedit buffer doc (Rich Trott) [#4187](https://github.com/nodejs/node/pull/4187)
* [[`c35a409cbe`](https://github.com/nodejs/node/commit/c35a409cbe)] - **doc**: clarify assert.fail doc (Rich Trott) [#4186](https://github.com/nodejs/node/pull/4186)
* [[`6235fdf72e`](https://github.com/nodejs/node/commit/6235fdf72e)] - **doc**: copyedit addons doc (Rich Trott) [#4185](https://github.com/nodejs/node/pull/4185)
* [[`990e7ff93e`](https://github.com/nodejs/node/commit/990e7ff93e)] - **doc**: update AUTHORS list (Rod Vagg) [#4183](https://github.com/nodejs/node/pull/4183)
* [[`8d676ef55e`](https://github.com/nodejs/node/commit/8d676ef55e)] - **doc**: change references from node to Node.js (Roman Klauke) [#4177](https://github.com/nodejs/node/pull/4177)
* [[`1c34b139a2`](https://github.com/nodejs/node/commit/1c34b139a2)] - **doc**: add brief Node.js overview to README (wurde) [#4174](https://github.com/nodejs/node/pull/4174)
* [[`27b9b72ab0`](https://github.com/nodejs/node/commit/27b9b72ab0)] - **doc**: add iarna to collaborators (Rebecca Turner) [#4144](https://github.com/nodejs/node/pull/4144)
* [[`683d8dd564`](https://github.com/nodejs/node/commit/683d8dd564)] - **doc**: add JungMinu to collaborators (Minwoo Jung) [#4143](https://github.com/nodejs/node/pull/4143)
* [[`17b06dfa94`](https://github.com/nodejs/node/commit/17b06dfa94)] - **doc**: add zkat to collaborators (Kat Marchán) [#4142](https://github.com/nodejs/node/pull/4142)
* [[`39364c4c72`](https://github.com/nodejs/node/commit/39364c4c72)] - **doc**: improve child_process.markdown wording (yorkie) [#4138](https://github.com/nodejs/node/pull/4138)
* [[`abe452835f`](https://github.com/nodejs/node/commit/abe452835f)] - **doc**: url.format - true slash postfix behaviour (fansworld-claudio) [#4119](https://github.com/nodejs/node/pull/4119)
* [[`6dd375cfe2`](https://github.com/nodejs/node/commit/6dd375cfe2)] - **doc**: document backlog for server.listen() variants (Jan Schär) [#4025](https://github.com/nodejs/node/pull/4025)
* [[`b71a3b363a`](https://github.com/nodejs/node/commit/b71a3b363a)] - **doc**: fixup socket.remoteAddress (Arthur Gautier) [#4198](https://github.com/nodejs/node/pull/4198)
* [[`e2fe214857`](https://github.com/nodejs/node/commit/e2fe214857)] - **doc**: add links and backticks around names (jpersson) [#4054](https://github.com/nodejs/node/pull/4054)
* [[`bb158f8aed`](https://github.com/nodejs/node/commit/bb158f8aed)] - **doc**: s/node.js/Node.js in readme (Rod Vagg) [#3998](https://github.com/nodejs/node/pull/3998)
* [[`f55491ad47`](https://github.com/nodejs/node/commit/f55491ad47)] - **doc**: move fs.existsSync() deprecation message (Martin Forsberg) [#3942](https://github.com/nodejs/node/pull/3942)
* [[`8c5b847f5b`](https://github.com/nodejs/node/commit/8c5b847f5b)] - **doc**: Describe FIPSDIR environment variable (Stefan Budeanu) [#3752](https://github.com/nodejs/node/pull/3752)
* [[`70c95ea0e5`](https://github.com/nodejs/node/commit/70c95ea0e5)] - **doc**: add warning about Windows process groups (Roman Klauke) [#3681](https://github.com/nodejs/node/pull/3681)
* [[`46c59b7256`](https://github.com/nodejs/node/commit/46c59b7256)] - **doc**: add CTC meeting minutes 2015-10-28 (Rod Vagg) [#3661](https://github.com/nodejs/node/pull/3661)
* [[`7ffd299a1d`](https://github.com/nodejs/node/commit/7ffd299a1d)] - **doc**: add final full stop in CONTRIBUTING.md (Emily Aviva Kapor-Mater) [#3576](https://github.com/nodejs/node/pull/3576)
* [[`1f78bff7ce`](https://github.com/nodejs/node/commit/1f78bff7ce)] - **doc**: add TSC meeting minutes 2015-10-21 (Rod Vagg) [#3480](https://github.com/nodejs/node/pull/3480)
* [[`2e623ff024`](https://github.com/nodejs/node/commit/2e623ff024)] - **doc**: add TSC meeting minutes 2015-10-14 (Rod Vagg) [#3463](https://github.com/nodejs/node/pull/3463)
* [[`b9c69964bb`](https://github.com/nodejs/node/commit/b9c69964bb)] - **doc**: add TSC meeting minutes 2015-10-07 (Rod Vagg) [#3364](https://github.com/nodejs/node/pull/3364)
* [[`f31d23c724`](https://github.com/nodejs/node/commit/f31d23c724)] - **doc**: add TSC meeting minutes 2015-09-30 (Rod Vagg) [#3235](https://github.com/nodejs/node/pull/3235)
* [[`ae8e3af178`](https://github.com/nodejs/node/commit/ae8e3af178)] - **doc**: update irc channels: #node.js and #node-dev (Nelson Pecora) [#2743](https://github.com/nodejs/node/pull/2743)
* [[`830caeb1bd`](https://github.com/nodejs/node/commit/830caeb1bd)] - **doc, test**: symbols as event names (Bryan English) [#4151](https://github.com/nodejs/node/pull/4151)
* [[`82cbfcdcbe`](https://github.com/nodejs/node/commit/82cbfcdcbe)] - **docs**: update gpg key for Myles Borins (Myles Borins) [#4657](https://github.com/nodejs/node/pull/4657)
* [[`50b72aa5a3`](https://github.com/nodejs/node/commit/50b72aa5a3)] - **docs**: fix npm command in releases.md (Myles Borins) [#4656](https://github.com/nodejs/node/pull/4656)
* [[`5bf56882e1`](https://github.com/nodejs/node/commit/5bf56882e1)] - **fs,doc**: use `target` instead of `destination` (yorkie) [#3912](https://github.com/nodejs/node/pull/3912)
* [[`41fcda840c`](https://github.com/nodejs/node/commit/41fcda840c)] - **http**: use `self.keepAlive` instead of `self.options.keepAlive` (Damian Schenkelman) [#4407](https://github.com/nodejs/node/pull/4407)
* [[`3ff237333d`](https://github.com/nodejs/node/commit/3ff237333d)] - **http**: Remove an unnecessary assignment (Bo Borgerson) [#4323](https://github.com/nodejs/node/pull/4323)
* [[`39dc054572`](https://github.com/nodejs/node/commit/39dc054572)] - **http**: remove excess calls to removeSocket (Dave) [#4172](https://github.com/nodejs/node/pull/4172)
* [[`751fbd84dd`](https://github.com/nodejs/node/commit/751fbd84dd)] - **https**: use `servername` in agent key (Fedor Indutny) [#4389](https://github.com/nodejs/node/pull/4389)
* [[`7a1a0a0055`](https://github.com/nodejs/node/commit/7a1a0a0055)] - **lib**: remove unused modules (Rich Trott) [#4683](https://github.com/nodejs/node/pull/4683)
* [[`3d81ea99bb`](https://github.com/nodejs/node/commit/3d81ea99bb)] - **lib,test**: update let to const where applicable (Sakthipriyan Vairamani) [#3152](https://github.com/nodejs/node/pull/3152)
* [[`8a9869eeab`](https://github.com/nodejs/node/commit/8a9869eeab)] - **module**: fix column offsets in errors (Tristian Flanagan) [#2867](https://github.com/nodejs/node/pull/2867)
* [[`0ae90ecd3d`](https://github.com/nodejs/node/commit/0ae90ecd3d)] - **module,repl**: remove repl require() hack (Ben Noordhuis) [#4026](https://github.com/nodejs/node/pull/4026)
* [[`a7367fdc1e`](https://github.com/nodejs/node/commit/a7367fdc1e)] - **net**: small code cleanup (Jan Schär) [#3943](https://github.com/nodejs/node/pull/3943)
* [[`03e9495cc2`](https://github.com/nodejs/node/commit/03e9495cc2)] - **node**: remove unused variables in AppendExceptionLine (Yazhong Liu) [#4264](https://github.com/nodejs/node/pull/4264)
* [[`06113b8711`](https://github.com/nodejs/node/commit/06113b8711)] - **node**: s/doNTCallbackX/nextTickCallbackWithXArgs/ (Rod Vagg) [#4167](https://github.com/nodejs/node/pull/4167)
* [[`8ce6843fe4`](https://github.com/nodejs/node/commit/8ce6843fe4)] - **os**: fix crash in GetInterfaceAddresses (Martin Bark) [#4272](https://github.com/nodejs/node/pull/4272)
* [[`53dcbb6aa4`](https://github.com/nodejs/node/commit/53dcbb6aa4)] - **repl**: remove unused function (Rich Trott)
* [[`db0e906fc1`](https://github.com/nodejs/node/commit/db0e906fc1)] - **repl**: Fixed node repl history edge case. (Mudit Ameta) [#4108](https://github.com/nodejs/node/pull/4108)
* [[`9855fab05f`](https://github.com/nodejs/node/commit/9855fab05f)] - **repl**: use String#repeat instead of Array#join (Evan Lucas) [#3900](https://github.com/nodejs/node/pull/3900)
* [[`41882e4077`](https://github.com/nodejs/node/commit/41882e4077)] - **repl**: fix require('3rdparty') regression (Ben Noordhuis) [#4215](https://github.com/nodejs/node/pull/4215)
* [[`93afc39d4a`](https://github.com/nodejs/node/commit/93afc39d4a)] - **repl**: attach location info to syntax errors (cjihrig) [#4013](https://github.com/nodejs/node/pull/4013)
* [[`d4806675a6`](https://github.com/nodejs/node/commit/d4806675a6)] - **repl**: display error message when loading directory (Prince J Wesley) [#4170](https://github.com/nodejs/node/pull/4170)
* [[`3080bdc7d7`](https://github.com/nodejs/node/commit/3080bdc7d7)] - **src**: define Is* util functions with macros (cjihrig) [#4118](https://github.com/nodejs/node/pull/4118)
* [[`2b8a32a13b`](https://github.com/nodejs/node/commit/2b8a32a13b)] - **src**: refactor vcbuild configure args creation (Rod Vagg) [#3399](https://github.com/nodejs/node/pull/3399)
* [[`d47f6ba768`](https://github.com/nodejs/node/commit/d47f6ba768)] - **src**: fix deprecation message for ErrnoException (Martin von Gagern) [#4269](https://github.com/nodejs/node/pull/4269)
* [[`5ba08fbf76`](https://github.com/nodejs/node/commit/5ba08fbf76)] - **src**: fix line numbers on core errors (cjihrig) [#4254](https://github.com/nodejs/node/pull/4254)
* [[`70974e9362`](https://github.com/nodejs/node/commit/70974e9362)] - **src**: use GetCurrentProcessId() for process.pid (Ben Noordhuis) [#4163](https://github.com/nodejs/node/pull/4163)
* [[`c96eca164f`](https://github.com/nodejs/node/commit/c96eca164f)] - **src**: don't print garbage errors (cjihrig) [#4112](https://github.com/nodejs/node/pull/4112)
* [[`f61412c753`](https://github.com/nodejs/node/commit/f61412c753)] - **test**: mark test-debug-no-context is flaky (Rich Trott) [#4421](https://github.com/nodejs/node/pull/4421)
* [[`46d8c93ed2`](https://github.com/nodejs/node/commit/46d8c93ed2)] - **test**: don't use cwd for relative path (Johan Bergström) [#4477](https://github.com/nodejs/node/pull/4477)
* [[`b6124ea39c`](https://github.com/nodejs/node/commit/b6124ea39c)] - **test**: write to tmp dir rather than fixture dir (Rich Trott) [#4489](https://github.com/nodejs/node/pull/4489)
* [[`350fa664bb`](https://github.com/nodejs/node/commit/350fa664bb)] - **test**: don't assume a certain folder structure (Johan Bergström) [#3325](https://github.com/nodejs/node/pull/3325)
* [[`6b2ef0efac`](https://github.com/nodejs/node/commit/6b2ef0efac)] - **test**: make temp path customizable (Johan Bergström) [#3325](https://github.com/nodejs/node/pull/3325)
* [[`f1837703a9`](https://github.com/nodejs/node/commit/f1837703a9)] - **test**: remove unused vars from parallel tests (Rich Trott) [#4511](https://github.com/nodejs/node/pull/4511)
* [[`b4964b099a`](https://github.com/nodejs/node/commit/b4964b099a)] - **test**: remove unused variables form http tests (Rich Trott) [#4422](https://github.com/nodejs/node/pull/4422)
* [[`0d5a508dfb`](https://github.com/nodejs/node/commit/0d5a508dfb)] - **test**: extend timeout in Debug mode (Rich Trott) [#4431](https://github.com/nodejs/node/pull/4431)
* [[`6e4598d5da`](https://github.com/nodejs/node/commit/6e4598d5da)] - **test**: remove unused variables from TLS tests (Rich Trott) [#4424](https://github.com/nodejs/node/pull/4424)
* [[`7b1aa045a0`](https://github.com/nodejs/node/commit/7b1aa045a0)] - **test**: remove unused variables from HTTPS tests (Rich Trott) [#4426](https://github.com/nodejs/node/pull/4426)
* [[`da9e5c1b01`](https://github.com/nodejs/node/commit/da9e5c1b01)] - **test**: remove unused variables from net tests (Rich Trott) [#4430](https://github.com/nodejs/node/pull/4430)
* [[`13241bd24b`](https://github.com/nodejs/node/commit/13241bd24b)] - **test**: remove unused vars in ChildProcess tests (Rich Trott) [#4425](https://github.com/nodejs/node/pull/4425)
* [[`2f4538ddda`](https://github.com/nodejs/node/commit/2f4538ddda)] - **test**: remove unused vars (Rich Trott) [#4536](https://github.com/nodejs/node/pull/4536)
* [[`dffe83ccd6`](https://github.com/nodejs/node/commit/dffe83ccd6)] - **test**: remove unused modules (Rich Trott) [#4684](https://github.com/nodejs/node/pull/4684)
* [[`c4eeb88ba1`](https://github.com/nodejs/node/commit/c4eeb88ba1)] - **test**: fix flaky cluster-disconnect-race (Brian White) [#4457](https://github.com/nodejs/node/pull/4457)
* [[`7caf87bf6c`](https://github.com/nodejs/node/commit/7caf87bf6c)] - **test**: fix flaky test-http-agent-keepalive (Rich Trott) [#4524](https://github.com/nodejs/node/pull/4524)
* [[`25c41d084d`](https://github.com/nodejs/node/commit/25c41d084d)] - **test**: remove flaky designations for tests (Rich Trott) [#4519](https://github.com/nodejs/node/pull/4519)
* [[`b8f097ece2`](https://github.com/nodejs/node/commit/b8f097ece2)] - **test**: fix flaky streams test (Rich Trott) [#4516](https://github.com/nodejs/node/pull/4516)
* [[`c24fa1437c`](https://github.com/nodejs/node/commit/c24fa1437c)] - **test**: inherit JOBS from environment (Johan Bergström) [#4495](https://github.com/nodejs/node/pull/4495)
* [[`7dc90e9e7f`](https://github.com/nodejs/node/commit/7dc90e9e7f)] - **test**: remove time check (Rich Trott) [#4494](https://github.com/nodejs/node/pull/4494)
* [[`7ca3c6c388`](https://github.com/nodejs/node/commit/7ca3c6c388)] - **test**: refactor test-fs-empty-readStream (Rich Trott) [#4490](https://github.com/nodejs/node/pull/4490)
* [[`610727dea7`](https://github.com/nodejs/node/commit/610727dea7)] - **test**: clarify role of domains in test (Rich Trott) [#4474](https://github.com/nodejs/node/pull/4474)
* [[`1ae0e355b9`](https://github.com/nodejs/node/commit/1ae0e355b9)] - **test**: improve assert message (Rich Trott) [#4461](https://github.com/nodejs/node/pull/4461)
* [[`e70c88df56`](https://github.com/nodejs/node/commit/e70c88df56)] - **test**: remove unused assert module imports (Rich Trott) [#4438](https://github.com/nodejs/node/pull/4438)
* [[`c77fc71f9b`](https://github.com/nodejs/node/commit/c77fc71f9b)] - **test**: remove unused var from test-assert.js (Rich Trott) [#4405](https://github.com/nodejs/node/pull/4405)
* [[`f613b3033f`](https://github.com/nodejs/node/commit/f613b3033f)] - **test**: add test-domain-exit-dispose-again back (Julien Gilli) [#4256](https://github.com/nodejs/node/pull/4256)
* [[`f5bfacd858`](https://github.com/nodejs/node/commit/f5bfacd858)] - **test**: remove unused `util` imports (Rich Trott) [#4562](https://github.com/nodejs/node/pull/4562)
* [[`d795301025`](https://github.com/nodejs/node/commit/d795301025)] - **test**: remove unnecessary assignments (Rich Trott) [#4563](https://github.com/nodejs/node/pull/4563)
* [[`acc3d66934`](https://github.com/nodejs/node/commit/acc3d66934)] - **test**: move ArrayStream to common (cjihrig) [#4027](https://github.com/nodejs/node/pull/4027)
* [[`6c0021361c`](https://github.com/nodejs/node/commit/6c0021361c)] - **test**: refactor test-net-connect-options-ipv6 (Rich Trott) [#4395](https://github.com/nodejs/node/pull/4395)
* [[`29804e00ad`](https://github.com/nodejs/node/commit/29804e00ad)] - **test**: use platformTimeout() in more places (Brian White) [#4387](https://github.com/nodejs/node/pull/4387)
* [[`761af37d0e`](https://github.com/nodejs/node/commit/761af37d0e)] - **test**: fix race condition in test-http-client-onerror (Devin Nakamura) [#4346](https://github.com/nodejs/node/pull/4346)
* [[`980852165f`](https://github.com/nodejs/node/commit/980852165f)] - **test**: fix flaky test-net-error-twice (Brian White) [#4342](https://github.com/nodejs/node/pull/4342)
* [[`1bc44e79d3`](https://github.com/nodejs/node/commit/1bc44e79d3)] - **test**: try other ipv6 localhost alternatives (Brian White) [#4325](https://github.com/nodejs/node/pull/4325)
* [[`44dbe15640`](https://github.com/nodejs/node/commit/44dbe15640)] - **test**: fix debug-port-cluster flakiness (Ben Noordhuis) [#4310](https://github.com/nodejs/node/pull/4310)
* [[`73e781172b`](https://github.com/nodejs/node/commit/73e781172b)] - **test**: add test for tls.parseCertString (Evan Lucas) [#4283](https://github.com/nodejs/node/pull/4283)
* [[`15c295a21b`](https://github.com/nodejs/node/commit/15c295a21b)] - **test**: use regular timeout times for ARMv8 (Jeremiah Senkpiel) [#4248](https://github.com/nodejs/node/pull/4248)
* [[`fd250b8fab`](https://github.com/nodejs/node/commit/fd250b8fab)] - **test**: parallelize test-repl-persistent-history (Jeremiah Senkpiel) [#4247](https://github.com/nodejs/node/pull/4247)
* [[`9a0f156e5a`](https://github.com/nodejs/node/commit/9a0f156e5a)] - **test**: fix domain-top-level-error-handler-throw (Santiago Gimeno) [#4364](https://github.com/nodejs/node/pull/4364)
* [[`6bc1b1c259`](https://github.com/nodejs/node/commit/6bc1b1c259)] - **test**: don't assume openssl s_client supports -ssl3 (Ben Noordhuis) [#4204](https://github.com/nodejs/node/pull/4204)
* [[`d00b9fc66f`](https://github.com/nodejs/node/commit/d00b9fc66f)] - **test**: fix tls-inception flakiness (Santiago Gimeno) [#4195](https://github.com/nodejs/node/pull/4195)
* [[`c41b280a2b`](https://github.com/nodejs/node/commit/c41b280a2b)] - **test**: fix tls-inception (Santiago Gimeno) [#4195](https://github.com/nodejs/node/pull/4195)
* [[`6f4ab1d1ab`](https://github.com/nodejs/node/commit/6f4ab1d1ab)] - **test**: mark test-cluster-shared-leak flaky (Rich Trott) [#4162](https://github.com/nodejs/node/pull/4162)
* [[`90498e2a68`](https://github.com/nodejs/node/commit/90498e2a68)] - **test**: skip long path tests on non-Windows (Rafał Pocztarski) [#4116](https://github.com/nodejs/node/pull/4116)
* [[`c9100d78f3`](https://github.com/nodejs/node/commit/c9100d78f3)] - **test**: fix flaky test-net-socket-local-address (Rich Trott) [#4109](https://github.com/nodejs/node/pull/4109)
* [[`ac939d51d9`](https://github.com/nodejs/node/commit/ac939d51d9)] - **test**: improve cluster-disconnect-handles test (Brian White) [#4084](https://github.com/nodejs/node/pull/4084)
* [[`22ba1b4115`](https://github.com/nodejs/node/commit/22ba1b4115)] - **test**: eliminate multicast test FreeBSD flakiness (Rich Trott) [#4042](https://github.com/nodejs/node/pull/4042)
* [[`2ee7853bb7`](https://github.com/nodejs/node/commit/2ee7853bb7)] - **test**: fix http-many-ended-pipelines flakiness (Santiago Gimeno) [#4041](https://github.com/nodejs/node/pull/4041)
* [[`a77dcfec06`](https://github.com/nodejs/node/commit/a77dcfec06)] - **test**: use platform-based timeout for reliability (Rich Trott) [#4015](https://github.com/nodejs/node/pull/4015)
* [[`3f0ff879cf`](https://github.com/nodejs/node/commit/3f0ff879cf)] - **test**: fix time resolution constraint (Gireesh Punathil) [#3981](https://github.com/nodejs/node/pull/3981)
* [[`22b88e1c48`](https://github.com/nodejs/node/commit/22b88e1c48)] - **test**: add TAP diagnostic message for retried tests (Rich Trott) [#3960](https://github.com/nodejs/node/pull/3960)
* [[`22d2887b1c`](https://github.com/nodejs/node/commit/22d2887b1c)] - **test**: add OS X to module loading error test (Evan Lucas) [#3901](https://github.com/nodejs/node/pull/3901)
* [[`e2141cb75e`](https://github.com/nodejs/node/commit/e2141cb75e)] - **test**: skip instead of fail when mem constrained (Michael Cornacchia) [#3697](https://github.com/nodejs/node/pull/3697)
* [[`166523d0ed`](https://github.com/nodejs/node/commit/166523d0ed)] - **test**: fix race condition in unrefd interval test (Michael Cornacchia) [#3550](https://github.com/nodejs/node/pull/3550)
* [[`86b47e8dc0`](https://github.com/nodejs/node/commit/86b47e8dc0)] - **timers**: optimize callback call: bind -> arrow (Andrei Sedoi) [#4038](https://github.com/nodejs/node/pull/4038)
* [[`4d37472ea7`](https://github.com/nodejs/node/commit/4d37472ea7)] - **tls_wrap**: clear errors on return (Fedor Indutny) [#4709](https://github.com/nodejs/node/pull/4709)
* [[`5b695d0343`](https://github.com/nodejs/node/commit/5b695d0343)] - **tls_wrap**: inherit from the `AsyncWrap` first (Fedor Indutny) [#4268](https://github.com/nodejs/node/pull/4268)
* [[`0efc35e6d8`](https://github.com/nodejs/node/commit/0efc35e6d8)] - **tls_wrap**: slice buffer properly in `ClearOut` (Fedor Indutny) [#4184](https://github.com/nodejs/node/pull/4184)
* [[`628cb8657c`](https://github.com/nodejs/node/commit/628cb8657c)] - **tools**: add .editorconfig (ronkorving) [#2993](https://github.com/nodejs/node/pull/2993)
* [[`69fef19624`](https://github.com/nodejs/node/commit/69fef19624)] - **tools**: implement no-unused-vars for eslint (Rich Trott) [#4536](https://github.com/nodejs/node/pull/4536)
* [[`3ee16706f2`](https://github.com/nodejs/node/commit/3ee16706f2)] - **tools**: enforce `throw new Error()` with lint rule (Rich Trott) [#3714](https://github.com/nodejs/node/pull/3714)
* [[`32801de4ef`](https://github.com/nodejs/node/commit/32801de4ef)] - **tools**: Use `throw new Error()` consistently (Rich Trott) [#3714](https://github.com/nodejs/node/pull/3714)
* [[`f413fae0cd`](https://github.com/nodejs/node/commit/f413fae0cd)] - **tools**: add tap output to cpplint (Johan Bergström) [#3448](https://github.com/nodejs/node/pull/3448)
* [[`efa30dd2f0`](https://github.com/nodejs/node/commit/efa30dd2f0)] - **tools**: enable prefer-const eslint rule (Sakthipriyan Vairamani) [#3152](https://github.com/nodejs/node/pull/3152)
* [[`dd0c925896`](https://github.com/nodejs/node/commit/dd0c925896)] - **udp**: remove a needless instanceof Buffer check (ronkorving) [#4301](https://github.com/nodejs/node/pull/4301)
* [[`f4414102ed`](https://github.com/nodejs/node/commit/f4414102ed)] - **util**: faster arrayToHash (Jackson Tian)
* [[`b421119984`](https://github.com/nodejs/node/commit/b421119984)] - **util**: determine object types in C++ (cjihrig) [#4100](https://github.com/nodejs/node/pull/4100)
* [[`6a7c9d9293`](https://github.com/nodejs/node/commit/6a7c9d9293)] - **util**: move .decorateErrorStack to internal/util (Ben Noordhuis) [#4026](https://github.com/nodejs/node/pull/4026)
* [[`422a865d46`](https://github.com/nodejs/node/commit/422a865d46)] - **util**: add decorateErrorStack() (cjihrig) [#4013](https://github.com/nodejs/node/pull/4013)
* [[`2d5380ea25`](https://github.com/nodejs/node/commit/2d5380ea25)] - **util**: fix constructor/instanceof checks (Brian White) [#3385](https://github.com/nodejs/node/pull/3385)
* [[`1bf84b9d41`](https://github.com/nodejs/node/commit/1bf84b9d41)] - **util,src**: allow lookup of hidden values (cjihrig) [#3988](https://github.com/nodejs/node/pull/3988)

<a id="4.2.4"></a>
## 2015-12-23, Version 4.2.4 'Argon' (LTS), @jasnell

Maintenance update.

### Notable changes

* Roughly 78% of the commits are documentation and test improvements
* **domains**:
** Fix handling of uncaught exceptions (Julien Gilli) [#3884](https://github.com/nodejs/node/pull/3884)
* **deps**:
** Upgrade to npm 2.14.12 (Kat Marchán) [#4110](https://github.com/nodejs/node/pull/4110)
** Backport 819b40a from V8 upstream (Michaël Zasso) [#3938](https://github.com/nodejs/node/pull/3938)
** Updated node LICENSE file with new npm license (Kat Marchán) [#4110](https://github.com/nodejs/node/pull/4110)

### Known issues

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`907a13a07f`](https://github.com/nodejs/node/commit/907a13a07f)] - Add missing va_end before return (Ömer Fadıl Usta) [#3565](https://github.com/nodejs/node/pull/3565)
* [[`7ffc01756f`](https://github.com/nodejs/node/commit/7ffc01756f)] - **buffer**: fix writeInt{B,L}E for some neg values (Peter A. Bigot) [#3994](https://github.com/nodejs/node/pull/3994)
* [[`db0186e435`](https://github.com/nodejs/node/commit/db0186e435)] - **buffer**: let WriteFloatGeneric silently drop values (Minqi Pan)
* [[`5c6740865a`](https://github.com/nodejs/node/commit/5c6740865a)] - **build**: update signtool description, add url (Rod Vagg) [#4011](https://github.com/nodejs/node/pull/4011)
* [[`60dda70f89`](https://github.com/nodejs/node/commit/60dda70f89)] - **build**: fix --with-intl=system-icu for x-compile (Steven R. Loomis) [#3808](https://github.com/nodejs/node/pull/3808)
* [[`22208b067c`](https://github.com/nodejs/node/commit/22208b067c)] - **build**: fix configuring with prebuilt libraries (Markus Tzoe) [#3135](https://github.com/nodejs/node/pull/3135)
* [[`914caf9c69`](https://github.com/nodejs/node/commit/914caf9c69)] - **child_process**: add safety checks on stdio access (cjihrig) [#3799](https://github.com/nodejs/node/pull/3799)
* [[`236ad90a84`](https://github.com/nodejs/node/commit/236ad90a84)] - **child_process**: don't fork bomb ourselves from -e (Ben Noordhuis) [#3575](https://github.com/nodejs/node/pull/3575)
* [[`f28f69dac4`](https://github.com/nodejs/node/commit/f28f69dac4)] - **cluster**: remove handles when disconnecting worker (Ben Noordhuis) [#3677](https://github.com/nodejs/node/pull/3677)
* [[`f5c5e8bf91`](https://github.com/nodejs/node/commit/f5c5e8bf91)] - **cluster**: send suicide message on disconnect (cjihrig) [#3720](https://github.com/nodejs/node/pull/3720)
* [[`629d5d18d7`](https://github.com/nodejs/node/commit/629d5d18d7)] - **configure**: `v8_use_snapshot` should be `true` (Fedor Indutny) [#3962](https://github.com/nodejs/node/pull/3962)
* [[`3094464871`](https://github.com/nodejs/node/commit/3094464871)] - **configure**: use __ARM_ARCH to determine arm version (João Reis) [#4123](https://github.com/nodejs/node/pull/4123)
* [[`1e1173fc5c`](https://github.com/nodejs/node/commit/1e1173fc5c)] - **configure**: respect CC_host in host arch detection (João Reis) [#4117](https://github.com/nodejs/node/pull/4117)
* [[`2e9b886fbf`](https://github.com/nodejs/node/commit/2e9b886fbf)] - **crypto**: DSA parameter validation in FIPS mode (Stefan Budeanu) [#3756](https://github.com/nodejs/node/pull/3756)
* [[`00b77d9e84`](https://github.com/nodejs/node/commit/00b77d9e84)] - **crypto**: Improve error checking and reporting (Stefan Budeanu) [#3753](https://github.com/nodejs/node/pull/3753)
* [[`3dd90ddc73`](https://github.com/nodejs/node/commit/3dd90ddc73)] - **deps**: upgrade to npm 2.14.12 (Kat Marchán) [#4110](https://github.com/nodejs/node/pull/4110)
* [[`51ae8d10b3`](https://github.com/nodejs/node/commit/51ae8d10b3)] - **deps**: Updated node LICENSE file with new npm license (Kat Marchán) [#4110](https://github.com/nodejs/node/pull/4110)
* [[`9e1edead22`](https://github.com/nodejs/node/commit/9e1edead22)] - **deps**: backport 819b40a from V8 upstream (Michaël Zasso) [#3938](https://github.com/nodejs/node/pull/3938)
* [[`a2ce3843cc`](https://github.com/nodejs/node/commit/a2ce3843cc)] - **deps**: upgrade npm to 2.14.9 (Forrest L Norvell) [#3686](https://github.com/nodejs/node/pull/3686)
* [[`b140cb29f4`](https://github.com/nodejs/node/commit/b140cb29f4)] - **dns**: prevent undefined values in results (Junliang Yan) [#3696](https://github.com/nodejs/node/pull/3696)
* [[`8aafa2ecc0`](https://github.com/nodejs/node/commit/8aafa2ecc0)] - **doc**: standardize references to node.js in docs (Scott Buchanan) [#4136](https://github.com/nodejs/node/pull/4136)
* [[`72f43a263a`](https://github.com/nodejs/node/commit/72f43a263a)] - **doc**: fix internal link to child.send() (Luigi Pinca) [#4089](https://github.com/nodejs/node/pull/4089)
* [[`dcfdbac457`](https://github.com/nodejs/node/commit/dcfdbac457)] - **doc**: reword https.Agent example text (Jan Krems) [#4075](https://github.com/nodejs/node/pull/4075)
* [[`f93d268dec`](https://github.com/nodejs/node/commit/f93d268dec)] - **doc**: add HTTP working group (James M Snell) [#3919](https://github.com/nodejs/node/pull/3919)
* [[`beee0553ca`](https://github.com/nodejs/node/commit/beee0553ca)] - **doc**: update WORKING_GROUPS.md - add missing groups (Michael Dawson) [#3450](https://github.com/nodejs/node/pull/3450)
* [[`3327415fc4`](https://github.com/nodejs/node/commit/3327415fc4)] - **doc**: fix the exception description (yorkie) [#3658](https://github.com/nodejs/node/pull/3658)
* [[`da8d012c88`](https://github.com/nodejs/node/commit/da8d012c88)] - **doc**: clarify v4.2.3 notable items (Rod Vagg) [#4155](https://github.com/nodejs/node/pull/4155)
* [[`44a2d8ca24`](https://github.com/nodejs/node/commit/44a2d8ca24)] - **doc**: fix color of linked code blocks (jpersson) [#4068](https://github.com/nodejs/node/pull/4068)
* [[`bebde48ebc`](https://github.com/nodejs/node/commit/bebde48ebc)] - **doc**: fix typo in README (Rich Trott) [#4000](https://github.com/nodejs/node/pull/4000)
* [[`b48d5ec301`](https://github.com/nodejs/node/commit/b48d5ec301)] - **doc**: message.header duplication correction (Bryan English) [#3997](https://github.com/nodejs/node/pull/3997)
* [[`6ef3625456`](https://github.com/nodejs/node/commit/6ef3625456)] - **doc**: replace sane with reasonable (Lewis Cowper) [#3980](https://github.com/nodejs/node/pull/3980)
* [[`c5be3c63f0`](https://github.com/nodejs/node/commit/c5be3c63f0)] - **doc**: fix rare case of misaligned columns (Roman Reiss) [#3948](https://github.com/nodejs/node/pull/3948)
* [[`bd82fb06ff`](https://github.com/nodejs/node/commit/bd82fb06ff)] - **doc**: fix broken references (Alexander Gromnitsky) [#3944](https://github.com/nodejs/node/pull/3944)
* [[`8eb28c3d50`](https://github.com/nodejs/node/commit/8eb28c3d50)] - **doc**: add reference for buffer.inspect() (cjihrig) [#3921](https://github.com/nodejs/node/pull/3921)
* [[`4bc71e0078`](https://github.com/nodejs/node/commit/4bc71e0078)] - **doc**: clarify module loading behavior (cjihrig) [#3920](https://github.com/nodejs/node/pull/3920)
* [[`4c382e7aaa`](https://github.com/nodejs/node/commit/4c382e7aaa)] - **doc**: numeric flags to fs.open (Carl Lei) [#3641](https://github.com/nodejs/node/pull/3641)
* [[`5207099dc9`](https://github.com/nodejs/node/commit/5207099dc9)] - **doc**: clarify that fs streams expect blocking fd (Carl Lei) [#3641](https://github.com/nodejs/node/pull/3641)
* [[`753c5071ea`](https://github.com/nodejs/node/commit/753c5071ea)] - **doc**: Adding best practises for crypto.pbkdf2 (Tom Gallacher) [#3290](https://github.com/nodejs/node/pull/3290)
* [[`8f0291beba`](https://github.com/nodejs/node/commit/8f0291beba)] - **doc**: update WORKING_GROUPS.md to include Intl (Steven R. Loomis) [#3251](https://github.com/nodejs/node/pull/3251)
* [[`c31d472487`](https://github.com/nodejs/node/commit/c31d472487)] - **doc**: sort repl alphabetically (Tristian Flanagan) [#3859](https://github.com/nodejs/node/pull/3859)
* [[`6b172d9fe8`](https://github.com/nodejs/node/commit/6b172d9fe8)] - **doc**: consistent reference-style links (Bryan English) [#3845](https://github.com/nodejs/node/pull/3845)
* [[`ffd3335e29`](https://github.com/nodejs/node/commit/ffd3335e29)] - **doc**: address use of profanity in code of conduct (James M Snell) [#3827](https://github.com/nodejs/node/pull/3827)
* [[`a36a5b63cf`](https://github.com/nodejs/node/commit/a36a5b63cf)] - **doc**: reword message.headers to indicate they are not read-only (Tristian Flanagan) [#3814](https://github.com/nodejs/node/pull/3814)
* [[`6de77cd320`](https://github.com/nodejs/node/commit/6de77cd320)] - **doc**: clarify duplicate header handling (Bryan English) [#3810](https://github.com/nodejs/node/pull/3810)
* [[`b22973af81`](https://github.com/nodejs/node/commit/b22973af81)] - **doc**: replace head of readme with updated text (Rod Vagg) [#3482](https://github.com/nodejs/node/pull/3482)
* [[`eab0d56ea9`](https://github.com/nodejs/node/commit/eab0d56ea9)] - **doc**: repl: add defineComand and displayPrompt (Bryan English) [#3765](https://github.com/nodejs/node/pull/3765)
* [[`15fb02985f`](https://github.com/nodejs/node/commit/15fb02985f)] - **doc**: document release types in readme (Rod Vagg) [#3482](https://github.com/nodejs/node/pull/3482)
* [[`29f26b882f`](https://github.com/nodejs/node/commit/29f26b882f)] - **doc**: add link to \[customizing util.inspect colors\]. (Jesse McCarthy) [#3749](https://github.com/nodejs/node/pull/3749)
* [[`90fdb4f7b3`](https://github.com/nodejs/node/commit/90fdb4f7b3)] - **doc**: sort tls alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`39fa9fa85c`](https://github.com/nodejs/node/commit/39fa9fa85c)] - **doc**: sort stream alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`e98e8afb2b`](https://github.com/nodejs/node/commit/e98e8afb2b)] - **doc**: sort net alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`6de887483d`](https://github.com/nodejs/node/commit/6de887483d)] - **doc**: sort process alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`37033dcb71`](https://github.com/nodejs/node/commit/37033dcb71)] - **doc**: sort zlib alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`9878034567`](https://github.com/nodejs/node/commit/9878034567)] - **doc**: sort util alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`48fc765eb6`](https://github.com/nodejs/node/commit/48fc765eb6)] - **doc**: sort https alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`3546eb4f40`](https://github.com/nodejs/node/commit/3546eb4f40)] - **doc**: sort http alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`dedfb1156a`](https://github.com/nodejs/node/commit/dedfb1156a)] - **doc**: sort modules alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`71722fe1a1`](https://github.com/nodejs/node/commit/71722fe1a1)] - **doc**: sort readline alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`660062bf9e`](https://github.com/nodejs/node/commit/660062bf9e)] - **doc**: sort repl alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`34b8d28725`](https://github.com/nodejs/node/commit/34b8d28725)] - **doc**: sort string_decoder alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`3f3b9ed7d7`](https://github.com/nodejs/node/commit/3f3b9ed7d7)] - **doc**: sort timers alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`af876ddc64`](https://github.com/nodejs/node/commit/af876ddc64)] - **doc**: sort tty alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`3c2068704a`](https://github.com/nodejs/node/commit/3c2068704a)] - **doc**: sort url alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`363692fd0c`](https://github.com/nodejs/node/commit/363692fd0c)] - **doc**: sort vm alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`ca41b55166`](https://github.com/nodejs/node/commit/ca41b55166)] - **doc**: sort querystring alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`f37ff22b9f`](https://github.com/nodejs/node/commit/f37ff22b9f)] - **doc**: sort punycode alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`4d569607af`](https://github.com/nodejs/node/commit/4d569607af)] - **doc**: sort path alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`daa62447d1`](https://github.com/nodejs/node/commit/daa62447d1)] - **doc**: sort os alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`0906f9a8bb`](https://github.com/nodejs/node/commit/0906f9a8bb)] - **doc**: sort globals alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`6cd06c1319`](https://github.com/nodejs/node/commit/6cd06c1319)] - **doc**: sort fs alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`5b310f8d9e`](https://github.com/nodejs/node/commit/5b310f8d9e)] - **doc**: sort events alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`782cb7d15b`](https://github.com/nodejs/node/commit/782cb7d15b)] - **doc**: sort errors alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`c39eabbec4`](https://github.com/nodejs/node/commit/c39eabbec4)] - **doc**: sort dgram alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`261e0f3a21`](https://github.com/nodejs/node/commit/261e0f3a21)] - **doc**: sort crypto alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`0e6121d04d`](https://github.com/nodejs/node/commit/0e6121d04d)] - **doc**: sort dns alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`435ffb79f7`](https://github.com/nodejs/node/commit/435ffb79f7)] - **doc**: sort console alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`28935a10d6`](https://github.com/nodejs/node/commit/28935a10d6)] - **doc**: sort cluster alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`5e79dc4406`](https://github.com/nodejs/node/commit/5e79dc4406)] - **doc**: sort child_process alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`af0bf1a72c`](https://github.com/nodejs/node/commit/af0bf1a72c)] - **doc**: sort buffer alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`f43a0330aa`](https://github.com/nodejs/node/commit/f43a0330aa)] - **doc**: sort assert alphabetically (Tristian Flanagan) [#3662](https://github.com/nodejs/node/pull/3662)
* [[`1bbc3b3ff8`](https://github.com/nodejs/node/commit/1bbc3b3ff8)] - **doc**: add note on tls connection meta data methods (Tyler Henkel) [#3746](https://github.com/nodejs/node/pull/3746)
* [[`3c415bbb12`](https://github.com/nodejs/node/commit/3c415bbb12)] - **doc**: add note to util.isBuffer (Evan Lucas) [#3790](https://github.com/nodejs/node/pull/3790)
* [[`7b5e4574fd`](https://github.com/nodejs/node/commit/7b5e4574fd)] - **doc**: add romankl to collaborators (Roman Klauke) [#3725](https://github.com/nodejs/node/pull/3725)
* [[`4f7c638a7a`](https://github.com/nodejs/node/commit/4f7c638a7a)] - **doc**: add saghul as a collaborator (Saúl Ibarra Corretgé)
* [[`523251270a`](https://github.com/nodejs/node/commit/523251270a)] - **doc**: add thealphanerd to collaborators (Myles Borins) [#3723](https://github.com/nodejs/node/pull/3723)
* [[`488e74f27d`](https://github.com/nodejs/node/commit/488e74f27d)] - **doc**: update lts description in the collaborator guide (James M Snell) [#3668](https://github.com/nodejs/node/pull/3668)
* [[`fe3ae3cea4`](https://github.com/nodejs/node/commit/fe3ae3cea4)] - **doc**: add LTS info to COLLABORATOR_GUIDE.md (Myles Borins) [#3442](https://github.com/nodejs/node/pull/3442)
* [[`daa10a345e`](https://github.com/nodejs/node/commit/daa10a345e)] - **doc**: typo fix in readme.md (Sam P Gallagher-Bishop) [#3649](https://github.com/nodejs/node/pull/3649)
* [[`eca5720761`](https://github.com/nodejs/node/commit/eca5720761)] - **doc**: fix wrong date and known issue in changelog.md (James M Snell) [#3650](https://github.com/nodejs/node/pull/3650)
* [[`83494f8f3e`](https://github.com/nodejs/node/commit/83494f8f3e)] - **doc**: rename iojs-* groups to nodejs-* (Steven R. Loomis) [#3634](https://github.com/nodejs/node/pull/3634)
* [[`347fb65aee`](https://github.com/nodejs/node/commit/347fb65aee)] - **doc**: fix crypto spkac function descriptions (Jason Gerfen) [#3614](https://github.com/nodejs/node/pull/3614)
* [[`11d2050d63`](https://github.com/nodejs/node/commit/11d2050d63)] - **doc**: Updated streams simplified constructor API (Tom Gallacher) [#3602](https://github.com/nodejs/node/pull/3602)
* [[`6db4392bfb`](https://github.com/nodejs/node/commit/6db4392bfb)] - **doc**: made code spans more visible in the API docs (phijohns) [#3573](https://github.com/nodejs/node/pull/3573)
* [[`8a7dd73af1`](https://github.com/nodejs/node/commit/8a7dd73af1)] - **doc**: added what buf.copy returns (Manuel B) [#3555](https://github.com/nodejs/node/pull/3555)
* [[`cf4b65c2d6`](https://github.com/nodejs/node/commit/cf4b65c2d6)] - **doc**: fix function param order in assert doc (David Woods) [#3533](https://github.com/nodejs/node/pull/3533)
* [[`a2efe4c72b`](https://github.com/nodejs/node/commit/a2efe4c72b)] - **doc**: add note about timeout delay > TIMEOUT_MAX (Guilherme Souza) [#3512](https://github.com/nodejs/node/pull/3512)
* [[`d1b5833476`](https://github.com/nodejs/node/commit/d1b5833476)] - **doc**: add caveats of algs and key size in crypto (Shigeki Ohtsu) [#3479](https://github.com/nodejs/node/pull/3479)
* [[`12cdf6fcf3`](https://github.com/nodejs/node/commit/12cdf6fcf3)] - **doc**: add method links in events.markdown (Alejandro Oviedo) [#3187](https://github.com/nodejs/node/pull/3187)
* [[`f50f19e384`](https://github.com/nodejs/node/commit/f50f19e384)] - **doc**: stdout/stderr can block when directed to file (Ben Noordhuis) [#3170](https://github.com/nodejs/node/pull/3170)
* [[`b2cc1302e0`](https://github.com/nodejs/node/commit/b2cc1302e0)] - **docs**: improve discoverability of Code of Conduct (Ashley Williams) [#3774](https://github.com/nodejs/node/pull/3774)
* [[`fa1ab497f1`](https://github.com/nodejs/node/commit/fa1ab497f1)] - **docs**: fs - change links to buffer encoding to Buffer class anchor (fansworld-claudio) [#2796](https://github.com/nodejs/node/pull/2796)
* [[`34e64e5390`](https://github.com/nodejs/node/commit/34e64e5390)] - **domains**: fix handling of uncaught exceptions (Julien Gilli) [#3884](https://github.com/nodejs/node/pull/3884)
* [[`0311836e7a`](https://github.com/nodejs/node/commit/0311836e7a)] - **meta**: remove use of profanity in source (Myles Borins) [#4122](https://github.com/nodejs/node/pull/4122)
* [[`971762ada9`](https://github.com/nodejs/node/commit/971762ada9)] - **module**: cache regular expressions (Evan Lucas) [#3869](https://github.com/nodejs/node/pull/3869)
* [[`d80fa2c77c`](https://github.com/nodejs/node/commit/d80fa2c77c)] - **module**: remove unnecessary JSON.stringify (Andres Suarez) [#3578](https://github.com/nodejs/node/pull/3578)
* [[`aa85d62f09`](https://github.com/nodejs/node/commit/aa85d62f09)] - **net**: add local address/port for better errors (Jan Schär) [#3946](https://github.com/nodejs/node/pull/3946)
* [[`803a56de52`](https://github.com/nodejs/node/commit/803a56de52)] - **querystring**: Parse multiple separator characters (Yosuke Furukawa) [#3807](https://github.com/nodejs/node/pull/3807)
* [[`ff02b295fc`](https://github.com/nodejs/node/commit/ff02b295fc)] - **repl**: don't crash if cannot open history file (Evan Lucas) [#3630](https://github.com/nodejs/node/pull/3630)
* [[`329e88e545`](https://github.com/nodejs/node/commit/329e88e545)] - **repl**: To exit, press ^C again or type .exit. (Hemanth.HM) [#3368](https://github.com/nodejs/node/pull/3368)
* [[`9b05905361`](https://github.com/nodejs/node/commit/9b05905361)] - **src**: Revert "nix stdin _readableState.reading" (Roman Reiss) [#3490](https://github.com/nodejs/node/pull/3490)
* [[`957c1f2543`](https://github.com/nodejs/node/commit/957c1f2543)] - **stream_wrap**: error if stream has StringDecoder (Fedor Indutny) [#4031](https://github.com/nodejs/node/pull/4031)
* [[`43e3b69dae`](https://github.com/nodejs/node/commit/43e3b69dae)] - **test**: refactor test-http-exit-delay (Rich Trott) [#4055](https://github.com/nodejs/node/pull/4055)
* [[`541d0d21be`](https://github.com/nodejs/node/commit/541d0d21be)] - **test**: fix cluster-disconnect-handles flakiness (Santiago Gimeno) [#4009](https://github.com/nodejs/node/pull/4009)
* [[`5f66d66e84`](https://github.com/nodejs/node/commit/5f66d66e84)] - **test**: don't check the # of chunks in test-http-1.0 (Santiago Gimeno) [#3961](https://github.com/nodejs/node/pull/3961)
* [[`355edf585b`](https://github.com/nodejs/node/commit/355edf585b)] - **test**: fix cluster-worker-isdead (Santiago Gimeno) [#3954](https://github.com/nodejs/node/pull/3954)
* [[`4e46e04002`](https://github.com/nodejs/node/commit/4e46e04002)] - **test**: add test for repl.defineCommand() (Bryan English) [#3908](https://github.com/nodejs/node/pull/3908)
* [[`4ea1a69c53`](https://github.com/nodejs/node/commit/4ea1a69c53)] - **test**: mark test flaky on FreeBSD (Rich Trott) [#4016](https://github.com/nodejs/node/pull/4016)
* [[`05b64c11f5`](https://github.com/nodejs/node/commit/05b64c11f5)] - **test**: mark cluster-net-send test flaky on windows (Rich Trott) [#4006](https://github.com/nodejs/node/pull/4006)
* [[`695015579b`](https://github.com/nodejs/node/commit/695015579b)] - **test**: remove flaky designation from ls-no-sslv3 (Rich Trott) [#3620](https://github.com/nodejs/node/pull/3620)
* [[`abbd87b273`](https://github.com/nodejs/node/commit/abbd87b273)] - **test**: mark fork regression test flaky on windows (Rich Trott) [#4005](https://github.com/nodejs/node/pull/4005)
* [[`38ba152a7a`](https://github.com/nodejs/node/commit/38ba152a7a)] - **test**: skip test if in FreeBSD jail (Rich Trott) [#3995](https://github.com/nodejs/node/pull/3995)
* [[`cc24f0ea58`](https://github.com/nodejs/node/commit/cc24f0ea58)] - **test**: fix test-domain-exit-dispose-again (Julien Gilli) [#3990](https://github.com/nodejs/node/pull/3990)
* [[`b2f1014d26`](https://github.com/nodejs/node/commit/b2f1014d26)] - **test**: remove flaky status for cluster test (Rich Trott) [#3975](https://github.com/nodejs/node/pull/3975)
* [[`e66794fd30`](https://github.com/nodejs/node/commit/e66794fd30)] - **test**: address flaky test-http-client-timeout-event (Rich Trott) [#3968](https://github.com/nodejs/node/pull/3968)
* [[`5a2727421a`](https://github.com/nodejs/node/commit/5a2727421a)] - **test**: retry on smartos if ECONNREFUSED (Rich Trott) [#3941](https://github.com/nodejs/node/pull/3941)
* [[`dbc85a275c`](https://github.com/nodejs/node/commit/dbc85a275c)] - **test**: avoid test timeouts on rpi (Stefan Budeanu) [#3902](https://github.com/nodejs/node/pull/3902)
* [[`b9d7378d20`](https://github.com/nodejs/node/commit/b9d7378d20)] - **test**: fix flaky test-child-process-spawnsync-input (Rich Trott) [#3889](https://github.com/nodejs/node/pull/3889)
* [[`cca216a034`](https://github.com/nodejs/node/commit/cca216a034)] - **test**: move test-specific function out of common (Rich Trott) [#3871](https://github.com/nodejs/node/pull/3871)
* [[`fb8df8d6c2`](https://github.com/nodejs/node/commit/fb8df8d6c2)] - **test**: module loading error fix solaris #3798 (fansworld-claudio) [#3855](https://github.com/nodejs/node/pull/3855)
* [[`9ea6bc1e0f`](https://github.com/nodejs/node/commit/9ea6bc1e0f)] - **test**: skip test if FreeBSD jail will break it (Rich Trott) [#3839](https://github.com/nodejs/node/pull/3839)
* [[`150f126618`](https://github.com/nodejs/node/commit/150f126618)] - **test**: fix flaky SmartOS test (Rich Trott) [#3830](https://github.com/nodejs/node/pull/3830)
* [[`603a6f5405`](https://github.com/nodejs/node/commit/603a6f5405)] - **test**: run pipeline flood test in parallel (Rich Trott) [#3811](https://github.com/nodejs/node/pull/3811)
* [[`4a26f74ee3`](https://github.com/nodejs/node/commit/4a26f74ee3)] - **test**: skip/replace weak crypto tests in FIPS mode (Stefan Budeanu) [#3757](https://github.com/nodejs/node/pull/3757)
* [[`3f9562b6bd`](https://github.com/nodejs/node/commit/3f9562b6bd)] - **test**: stronger crypto in test fixtures (Stefan Budeanu) [#3759](https://github.com/nodejs/node/pull/3759)
* [[`1f83eebec5`](https://github.com/nodejs/node/commit/1f83eebec5)] - **test**: increase crypto strength for FIPS standard (Stefan Budeanu) [#3758](https://github.com/nodejs/node/pull/3758)
* [[`7c5fbf7850`](https://github.com/nodejs/node/commit/7c5fbf7850)] - **test**: add hasFipsCrypto to test/common.js (Stefan Budeanu) [#3756](https://github.com/nodejs/node/pull/3756)
* [[`f30214f135`](https://github.com/nodejs/node/commit/f30214f135)] - **test**: add test for invalid DSA key size (Stefan Budeanu) [#3756](https://github.com/nodejs/node/pull/3756)
* [[`9a6c9faafb`](https://github.com/nodejs/node/commit/9a6c9faafb)] - **test**: numeric flags to fs.open (Carl Lei) [#3641](https://github.com/nodejs/node/pull/3641)
* [[`93d1d3cfcd`](https://github.com/nodejs/node/commit/93d1d3cfcd)] - **test**: refactor test-http-pipeline-flood (Rich Trott) [#3636](https://github.com/nodejs/node/pull/3636)
* [[`6c23f67504`](https://github.com/nodejs/node/commit/6c23f67504)] - **test**: fix flaky test test-http-pipeline-flood (Devin Nakamura) [#3636](https://github.com/nodejs/node/pull/3636)
* [[`4e5cae4360`](https://github.com/nodejs/node/commit/4e5cae4360)] - **test**: use really invalid hostname (Sakthipriyan Vairamani) [#3711](https://github.com/nodejs/node/pull/3711)
* [[`da189f793b`](https://github.com/nodejs/node/commit/da189f793b)] - **test**: Fix test-cluster-worker-exit.js for AIX (Imran Iqbal) [#3666](https://github.com/nodejs/node/pull/3666)
* [[`7b4194a863`](https://github.com/nodejs/node/commit/7b4194a863)] - **test**: fix test-module-loading-error for musl (Hugues Malphettes) [#3657](https://github.com/nodejs/node/pull/3657)
* [[`3dc52e99df`](https://github.com/nodejs/node/commit/3dc52e99df)] - **test**: fix test-net-persistent-keepalive for AIX (Imran Iqbal) [#3646](https://github.com/nodejs/node/pull/3646)
* [[`0e8eb66a78`](https://github.com/nodejs/node/commit/0e8eb66a78)] - **test**: fix path to module for repl test on Windows (Michael Cornacchia) [#3608](https://github.com/nodejs/node/pull/3608)
* [[`3aecbc86d2`](https://github.com/nodejs/node/commit/3aecbc86d2)] - **test**: add test-zlib-flush-drain (Myles Borins) [#3534](https://github.com/nodejs/node/pull/3534)
* [[`542d05cbe1`](https://github.com/nodejs/node/commit/542d05cbe1)] - **test**: enhance fs-watch-recursive test (Sakthipriyan Vairamani) [#2599](https://github.com/nodejs/node/pull/2599)
* [[`0eb0119d64`](https://github.com/nodejs/node/commit/0eb0119d64)] - **tls**: Use SHA1 for sessionIdContext in FIPS mode (Stefan Budeanu) [#3755](https://github.com/nodejs/node/pull/3755)
* [[`c10c08604c`](https://github.com/nodejs/node/commit/c10c08604c)] - **tls**: remove util and calls to util.format (Myles Borins) [#3456](https://github.com/nodejs/node/pull/3456)
* [[`a558a570c0`](https://github.com/nodejs/node/commit/a558a570c0)] - **util**: use regexp instead of str.replace().join() (qinjia) [#3689](https://github.com/nodejs/node/pull/3689)
* [[`47bb94a0c3`](https://github.com/nodejs/node/commit/47bb94a0c3)] - **zlib**: only apply drain listener if given callback (Craig Cavalier) [#3534](https://github.com/nodejs/node/pull/3534)
* [[`4733a60158`](https://github.com/nodejs/node/commit/4733a60158)] - **zlib**: pass kind to recursive calls to flush (Myles Borins) [#3534](https://github.com/nodejs/node/pull/3534)

<a id="4.2.3"></a>
## 2015-12-04, Version 4.2.3 'Argon' (LTS), @rvagg

Security Update

### Notable changes

* **http**: Fix CVE-2015-8027, a bug whereby an HTTP socket may no longer have a parser associated with it but a pipelined request attempts to trigger a pause or resume on the non-existent parser, a potential denial-of-service vulnerability. (Fedor Indutny)
* **openssl**: Upgrade to 1.0.2e, containing fixes for:
  - CVE-2015-3193 "BN_mod_exp may produce incorrect results on x86_64", an attack may be possible against a Node.js TLS server using DHE key exchange. Details are available at <http://openssl.org/news/secadv/20151203.txt>.
  - CVE-2015-3194 "Certificate verify crash with missing PSS parameter", a potential denial-of-service vector for Node.js TLS servers using client certificate authentication; TLS clients are also impacted. Details are available at <http://openssl.org/news/secadv/20151203.txt>.
  (Shigeki Ohtsu) [#4134](https://github.com/nodejs/node/pull/4134)
* **v8**: Backport fix for CVE-2015-6764, a bug in `JSON.stringify()` that can result in out-of-bounds reads for arrays. (Ben Noordhuis)

### Known issues

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`49bbd563be`](https://github.com/nodejs/node/commit/49bbd563be)] - **deps**: upgrade openssl sources to 1.0.2e (Shigeki Ohtsu) [#4134](https://github.com/nodejs/node/pull/4134)
* [[`9a063fd492`](https://github.com/nodejs/node/commit/9a063fd492)] - **deps**: backport a7e50a5 from upstream v8 (Ben Noordhuis)
* [[`07233206e9`](https://github.com/nodejs/node/commit/07233206e9)] - **deps**: backport 6df9a1d from upstream v8 (Ben Noordhuis)
* [[`1c8e6de78e`](https://github.com/nodejs/node/commit/1c8e6de78e)] - **http**: fix pipeline regression (Fedor Indutny)

<a id="4.2.2"></a>
## 2015-11-03, Version 4.2.2 'Argon' (LTS), @jasnell

### Notable changes

This is an LTS maintenance release that addresses a number of issues:

* [[`1d0f2cbf87`](https://github.com/nodejs/node/commit/1d0f2cbf87)] - **buffer**: fix value check for writeUInt{B,L}E (Trevor Norris) [#3500](https://github.com/nodejs/node/pull/3500)
* [[`2a45b72b4a`](https://github.com/nodejs/node/commit/2a45b72b4a)] - **buffer**: don't CHECK on zero-sized realloc (Ben Noordhuis) [#3499](https://github.com/nodejs/node/pull/3499)
* [[`a6469e901a`](https://github.com/nodejs/node/commit/a6469e901a)] - **deps**: backport 010897c from V8 upstream (Ali Ijaz Sheikh) [#3520](https://github.com/nodejs/node/pull/3520)
* [[`cadee67c25`](https://github.com/nodejs/node/commit/cadee67c25)] - **deps**: backport 8d6a228 from the v8's upstream (Fedor Indutny) [#3549](https://github.com/nodejs/node/pull/3549)
* [[`46c8c94055`](https://github.com/nodejs/node/commit/46c8c94055)] - **fs**: reduced duplicate code in fs.write() (ronkorving) [#2947](https://github.com/nodejs/node/pull/2947)
* [[`0427cdf094`](https://github.com/nodejs/node/commit/0427cdf094)] - **http**: fix stalled pipeline bug (Fedor Indutny) [#3342](https://github.com/nodejs/node/pull/3342)
* [[`2109708186`](https://github.com/nodejs/node/commit/2109708186)] - **lib**: fix cluster handle leak (Rich Trott) [#3510](https://github.com/nodejs/node/pull/3510)
* [[`f49c7c6955`](https://github.com/nodejs/node/commit/f49c7c6955)] - **lib**: avoid REPL exit on completion error (Rich Trott) [#3358](https://github.com/nodejs/node/pull/3358)
* [[`8a2c4aeeaa`](https://github.com/nodejs/node/commit/8a2c4aeeaa)] - **repl**: handle comments properly (Sakthipriyan Vairamani) [#3515](https://github.com/nodejs/node/pull/3515)
* [[`a04408acce`](https://github.com/nodejs/node/commit/a04408acce)] - **repl**: limit persistent history correctly on load (Jeremiah Senkpiel) [#2356](https://github.com/nodejs/node/pull/2356)
* [[`3bafe1a59b`](https://github.com/nodejs/node/commit/3bafe1a59b)] - **src**: fix race condition in debug signal on exit (Ben Noordhuis) [#3528](https://github.com/nodejs/node/pull/3528)
* [[`fe01d0df7a`](https://github.com/nodejs/node/commit/fe01d0df7a)] - **src**: fix exception message encoding on Windows (Brian White) [#3288](https://github.com/nodejs/node/pull/3288)
* [[`4bac5d9ddf`](https://github.com/nodejs/node/commit/4bac5d9ddf)] - **stream**: avoid unnecessary concat of a single buffer. (Calvin Metcalf) [#3300](https://github.com/nodejs/node/pull/3300)
* [[`8d78d687d5`](https://github.com/nodejs/node/commit/8d78d687d5)] - **timers**: reuse timer in `setTimeout().unref()` (Fedor Indutny) [#3407](https://github.com/nodejs/node/pull/3407)
* [[`e69c869399`](https://github.com/nodejs/node/commit/e69c869399)] - **tls**: TLSSocket options default isServer false (Yuval Brik) [#2614](https://github.com/nodejs/node/pull/2614)

### Known issues

* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`1d0f2cbf87`](https://github.com/nodejs/node/commit/1d0f2cbf87)] - **buffer**: fix value check for writeUInt{B,L}E (Trevor Norris) [#3500](https://github.com/nodejs/node/pull/3500)
* [[`2a45b72b4a`](https://github.com/nodejs/node/commit/2a45b72b4a)] - **buffer**: don't CHECK on zero-sized realloc (Ben Noordhuis) [#3499](https://github.com/nodejs/node/pull/3499)
* [[`dc655e1dd2`](https://github.com/nodejs/node/commit/dc655e1dd2)] - **build**: rectify --link-module help text (Minqi Pan) [#3379](https://github.com/nodejs/node/pull/3379)
* [[`a6469e901a`](https://github.com/nodejs/node/commit/a6469e901a)] - **deps**: backport 010897c from V8 upstream (Ali Ijaz Sheikh) [#3520](https://github.com/nodejs/node/pull/3520)
* [[`cadee67c25`](https://github.com/nodejs/node/commit/cadee67c25)] - **deps**: backport 8d6a228 from the v8's upstream (Fedor Indutny) [#3549](https://github.com/nodejs/node/pull/3549)
* [[`1ebd35550b`](https://github.com/nodejs/node/commit/1ebd35550b)] - **doc**: fix typos in changelog (reggi) [#3291](https://github.com/nodejs/node/pull/3291)
* [[`fbd93d4c1c`](https://github.com/nodejs/node/commit/fbd93d4c1c)] - **doc**: more use-cases for promise events (Domenic Denicola) [#3438](https://github.com/nodejs/node/pull/3438)
* [[`6ceb9af407`](https://github.com/nodejs/node/commit/6ceb9af407)] - **doc**: remove old note, 'cluster' is marked stable (Balázs Galambosi) [#3314](https://github.com/nodejs/node/pull/3314)
* [[`a5f0d64ddc`](https://github.com/nodejs/node/commit/a5f0d64ddc)] - **doc**: createServer's key option can be an array (Sakthipriyan Vairamani) [#3123](https://github.com/nodejs/node/pull/3123)
* [[`317e0ec6b3`](https://github.com/nodejs/node/commit/317e0ec6b3)] - **doc**: binary encoding is not deprecated (Trevor Norris) [#3441](https://github.com/nodejs/node/pull/3441)
* [[`b422f6ee1a`](https://github.com/nodejs/node/commit/b422f6ee1a)] - **doc**: mention the behaviour if URL is invalid (Sakthipriyan Vairamani) [#2966](https://github.com/nodejs/node/pull/2966)
* [[`bc29aad22b`](https://github.com/nodejs/node/commit/bc29aad22b)] - **doc**: fix indent in tls resumption example (Roman Reiss) [#3372](https://github.com/nodejs/node/pull/3372)
* [[`313877bd8f`](https://github.com/nodejs/node/commit/313877bd8f)] - **doc**: fix typo in changelog (Timothy Gu) [#3353](https://github.com/nodejs/node/pull/3353)
* [[`4be432862a`](https://github.com/nodejs/node/commit/4be432862a)] - **doc**: show keylen in pbkdf2 as a byte length (calebboyd) [#3334](https://github.com/nodejs/node/pull/3334)
* [[`23a1140ddb`](https://github.com/nodejs/node/commit/23a1140ddb)] - **doc**: add information about Assert behavior and maintenance (Rich Trott) [#3330](https://github.com/nodejs/node/pull/3330)
* [[`e04cb1e1fc`](https://github.com/nodejs/node/commit/e04cb1e1fc)] - **doc**: clarify API buffer.concat (Martii) [#3255](https://github.com/nodejs/node/pull/3255)
* [[`eae714c370`](https://github.com/nodejs/node/commit/eae714c370)] - **doc**: clarify the use of `option.detached` (Kyle Smith) [#3250](https://github.com/nodejs/node/pull/3250)
* [[`b884899e67`](https://github.com/nodejs/node/commit/b884899e67)] - **doc**: label v4.2.1 as LTS in changelog heading (Phillip Johnsen) [#3360](https://github.com/nodejs/node/pull/3360)
* [[`9120a04981`](https://github.com/nodejs/node/commit/9120a04981)] - **docs**: add missing shell option to execSync (fansworld-claudio) [#3440](https://github.com/nodejs/node/pull/3440)
* [[`46c8c94055`](https://github.com/nodejs/node/commit/46c8c94055)] - **fs**: reduced duplicate code in fs.write() (ronkorving) [#2947](https://github.com/nodejs/node/pull/2947)
* [[`0427cdf094`](https://github.com/nodejs/node/commit/0427cdf094)] - **http**: fix stalled pipeline bug (Fedor Indutny) [#3342](https://github.com/nodejs/node/pull/3342)
* [[`2109708186`](https://github.com/nodejs/node/commit/2109708186)] - **lib**: fix cluster handle leak (Rich Trott) [#3510](https://github.com/nodejs/node/pull/3510)
* [[`f49c7c6955`](https://github.com/nodejs/node/commit/f49c7c6955)] - **lib**: avoid REPL exit on completion error (Rich Trott) [#3358](https://github.com/nodejs/node/pull/3358)
* [[`8a2c4aeeaa`](https://github.com/nodejs/node/commit/8a2c4aeeaa)] - **repl**: handle comments properly (Sakthipriyan Vairamani) [#3515](https://github.com/nodejs/node/pull/3515)
* [[`a04408acce`](https://github.com/nodejs/node/commit/a04408acce)] - **repl**: limit persistent history correctly on load (Jeremiah Senkpiel) [#2356](https://github.com/nodejs/node/pull/2356)
* [[`5d1f1c5fa8`](https://github.com/nodejs/node/commit/5d1f1c5fa8)] - **src**: wrap source before doing syntax check (Evan Lucas) [#3587](https://github.com/nodejs/node/pull/3587)
* [[`3bafe1a59b`](https://github.com/nodejs/node/commit/3bafe1a59b)] - **src**: fix race condition in debug signal on exit (Ben Noordhuis) [#3528](https://github.com/nodejs/node/pull/3528)
* [[`fe01d0df7a`](https://github.com/nodejs/node/commit/fe01d0df7a)] - **src**: fix exception message encoding on Windows (Brian White) [#3288](https://github.com/nodejs/node/pull/3288)
* [[`4bac5d9ddf`](https://github.com/nodejs/node/commit/4bac5d9ddf)] - **stream**: avoid unnecessary concat of a single buffer. (Calvin Metcalf) [#3300](https://github.com/nodejs/node/pull/3300)
* [[`117fb47a16`](https://github.com/nodejs/node/commit/117fb47a16)] - **stream**: fix signature of _write() in a comment (Fábio Santos) [#3248](https://github.com/nodejs/node/pull/3248)
* [[`c563a34427`](https://github.com/nodejs/node/commit/c563a34427)] - **test**: split independent tests into separate files (Rich Trott) [#3548](https://github.com/nodejs/node/pull/3548)
* [[`3f62952d42`](https://github.com/nodejs/node/commit/3f62952d42)] - **test**: add node::MakeCallback() test coverage (Ben Noordhuis) [#3478](https://github.com/nodejs/node/pull/3478)
* [[`6b75f10d8a`](https://github.com/nodejs/node/commit/6b75f10d8a)] - **test**: use port number from env in tls socket test (Stefan Budeanu) [#3557](https://github.com/nodejs/node/pull/3557)
* [[`39ff44e94f`](https://github.com/nodejs/node/commit/39ff44e94f)] - **test**: fix heap-profiler link error LNK1194 on win (Junliang Yan) [#3572](https://github.com/nodejs/node/pull/3572)
* [[`a2786dd408`](https://github.com/nodejs/node/commit/a2786dd408)] - **test**: fix missing unistd.h on windows (Junliang Yan) [#3532](https://github.com/nodejs/node/pull/3532)
* [[`5e6f7c9a23`](https://github.com/nodejs/node/commit/5e6f7c9a23)] - **test**: add regression test for --debug-brk -e 0 (Ben Noordhuis) [#3585](https://github.com/nodejs/node/pull/3585)
* [[`7cad182cb6`](https://github.com/nodejs/node/commit/7cad182cb6)] - **test**: port domains regression test from v0.10 (Jonas Dohse) [#3356](https://github.com/nodejs/node/pull/3356)
* [[`78d854c6ce`](https://github.com/nodejs/node/commit/78d854c6ce)] - **test**: remove util from common (Rich Trott) [#3324](https://github.com/nodejs/node/pull/3324)
* [[`c566c8b8c0`](https://github.com/nodejs/node/commit/c566c8b8c0)] - **test**: remove util properties from common (Rich Trott) [#3304](https://github.com/nodejs/node/pull/3304)
* [[`eb7c3fb2f4`](https://github.com/nodejs/node/commit/eb7c3fb2f4)] - **test**: split up buffer tests for reliability (Rich Trott) [#3323](https://github.com/nodejs/node/pull/3323)
* [[`b398a85e19`](https://github.com/nodejs/node/commit/b398a85e19)] - **test**: parallelize long-running test (Rich Trott) [#3287](https://github.com/nodejs/node/pull/3287)
* [[`b5f3b4956b`](https://github.com/nodejs/node/commit/b5f3b4956b)] - **test**: change call to deprecated util.isError() (Rich Trott) [#3084](https://github.com/nodejs/node/pull/3084)
* [[`32149cacb5`](https://github.com/nodejs/node/commit/32149cacb5)] - **test**: improve tests for util.inherits (Michaël Zasso) [#3507](https://github.com/nodejs/node/pull/3507)
* [[`5be686fab8`](https://github.com/nodejs/node/commit/5be686fab8)] - **test**: print helpful err msg on test-dns-ipv6.js (Junliang Yan) [#3501](https://github.com/nodejs/node/pull/3501)
* [[`0429131e32`](https://github.com/nodejs/node/commit/0429131e32)] - **test**: fix domain with abort-on-uncaught on PPC (Julien Gilli) [#3354](https://github.com/nodejs/node/pull/3354)
* [[`788106eee9`](https://github.com/nodejs/node/commit/788106eee9)] - **test**: cleanup, improve repl-persistent-history (Jeremiah Senkpiel) [#2356](https://github.com/nodejs/node/pull/2356)
* [[`ea58fa0bac`](https://github.com/nodejs/node/commit/ea58fa0bac)] - **test**: add Symbol test for assert.deepEqual() (Rich Trott) [#3327](https://github.com/nodejs/node/pull/3327)
* [[`d409ac473b`](https://github.com/nodejs/node/commit/d409ac473b)] - **test**: disable test-tick-processor - aix and be ppc (Michael Dawson) [#3491](https://github.com/nodejs/node/pull/3491)
* [[`c1623039dd`](https://github.com/nodejs/node/commit/c1623039dd)] - **test**: harden test-child-process-fork-regr-gh-2847 (Michael Dawson) [#3459](https://github.com/nodejs/node/pull/3459)
* [[`3bb4437abb`](https://github.com/nodejs/node/commit/3bb4437abb)] - **test**: fix test-net-keepalive for AIX (Imran Iqbal) [#3458](https://github.com/nodejs/node/pull/3458)
* [[`af55641a69`](https://github.com/nodejs/node/commit/af55641a69)] - **test**: wrap assert.fail when passed to callback (Myles Borins) [#3453](https://github.com/nodejs/node/pull/3453)
* [[`7c7ef01e65`](https://github.com/nodejs/node/commit/7c7ef01e65)] - **test**: skip test-dns-ipv6.js if ipv6 is unavailable (Junliang Yan) [#3444](https://github.com/nodejs/node/pull/3444)
* [[`a4d1510ba4`](https://github.com/nodejs/node/commit/a4d1510ba4)] - **test**: repl-persistent-history is no longer flaky (Jeremiah Senkpiel) [#3437](https://github.com/nodejs/node/pull/3437)
* [[`a5d968b8a2`](https://github.com/nodejs/node/commit/a5d968b8a2)] - **test**: fix flaky test-child-process-emfile (Rich Trott) [#3430](https://github.com/nodejs/node/pull/3430)
* [[`eac2acca76`](https://github.com/nodejs/node/commit/eac2acca76)] - **test**: remove flaky status from eval_messages test (Rich Trott) [#3420](https://github.com/nodejs/node/pull/3420)
* [[`155c778584`](https://github.com/nodejs/node/commit/155c778584)] - **test**: fix flaky test for symlinks (Rich Trott) [#3418](https://github.com/nodejs/node/pull/3418)
* [[`74eb632483`](https://github.com/nodejs/node/commit/74eb632483)] - **test**: apply correct assert.fail() arguments (Rich Trott) [#3378](https://github.com/nodejs/node/pull/3378)
* [[`0a4323dd82`](https://github.com/nodejs/node/commit/0a4323dd82)] - **test**: replace util with backtick strings (Myles Borins) [#3359](https://github.com/nodejs/node/pull/3359)
* [[`93847694ec`](https://github.com/nodejs/node/commit/93847694ec)] - **test**: add test-child-process-emfile fail message (Rich Trott) [#3335](https://github.com/nodejs/node/pull/3335)
* [[`8d78d687d5`](https://github.com/nodejs/node/commit/8d78d687d5)] - **timers**: reuse timer in `setTimeout().unref()` (Fedor Indutny) [#3407](https://github.com/nodejs/node/pull/3407)
* [[`e69c869399`](https://github.com/nodejs/node/commit/e69c869399)] - **tls**: TLSSocket options default isServer false (Yuval Brik) [#2614](https://github.com/nodejs/node/pull/2614)
* [[`0b32bbbf69`](https://github.com/nodejs/node/commit/0b32bbbf69)] - **v8**: pull fix for builtin code size on PPC (Michael Dawson) [#3474](https://github.com/nodejs/node/pull/3474)

<a id="4.2.1"></a>
## 2015-10-13, Version 4.2.1 'Argon' (LTS), @jasnell

### Notable changes

* Includes fixes for two regressions
  - Assertion error in WeakCallback  - see [#3329](https://github.com/nodejs/node/pull/3329)
  - Undefined timeout regression - see [#3331](https://github.com/nodejs/node/pull/3331)

### Known issues

* When a server queues a large amount of data to send to a client over a pipelined HTTP connection, the underlying socket may be destroyed. See [#3332](https://github.com/nodejs/node/issues/3332) and [#3342](https://github.com/nodejs/node/pull/3342).
* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`b3cbd13340`](https://github.com/nodejs/node/commit/b3cbd13340)] - **buffer**: fix assertion error in WeakCallback (Fedor Indutny) [#3329](https://github.com/nodejs/node/pull/3329)
* [[`102cb7288c`](https://github.com/nodejs/node/commit/102cb7288c)] - **doc**: label v4.2.0 as LTS in changelog heading (Rod Vagg) [#3343](https://github.com/nodejs/node/pull/3343)
* [[`c245a199a7`](https://github.com/nodejs/node/commit/c245a199a7)] - **lib**: fix undefined timeout regression (Ryan Graham) [#3331](https://github.com/nodejs/node/pull/3331)

<a id="4.2.0"></a>
## 2015-10-07, Version 4.2.0 'Argon' (LTS), @jasnell

### Notable changes

The first Node.js LTS release! See https://github.com/nodejs/LTS/ for details of the LTS process.

* **icu**: Updated to version 56 with significant performance improvements (Steven R. Loomis) [#3281](https://github.com/nodejs/node/pull/3281)
* **node**:
  - Added new `-c` (or `--check`) command line argument for checking script syntax without executing the code (Dave Eddy) [#2411](https://github.com/nodejs/node/pull/2411)
  - Added `process.versions.icu` to hold the current ICU library version (Evan Lucas) [#3102](https://github.com/nodejs/node/pull/3102)
  - Added `process.release.lts` to hold the current LTS codename when the binary is from an active LTS release line (Rod Vagg) [#3212](https://github.com/nodejs/node/pull/3212)
* **npm**: Upgraded to npm 2.14.7 from 2.14.4, see [release notes](https://github.com/npm/npm/releases/tag/v2.14.7) for full details (Kat Marchán) [#3299](https://github.com/nodejs/node/pull/3299)

### Known issues

See https://github.com/nodejs/node/labels/confirmed-bug for complete and current list of known issues.

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`8383c4fe00`](https://github.com/nodejs/node/commit/8383c4fe00)] - **assert**: support arrow functions in .throws() (Ben Noordhuis) [#3276](https://github.com/nodejs/node/pull/3276)
* [[`3eaa593a32`](https://github.com/nodejs/node/commit/3eaa593a32)] - **async_wrap**: correctly pass parent to init callback (Trevor Norris) [#3216](https://github.com/nodejs/node/pull/3216)
* [[`54795620f6`](https://github.com/nodejs/node/commit/54795620f6)] - **buffer**: don't abort on prototype getters (Trevor Norris) [#3302](https://github.com/nodejs/node/pull/3302)
* [[`660f7591c8`](https://github.com/nodejs/node/commit/660f7591c8)] - **buffer**: FreeCallback should be tied to ArrayBuffer (Fedor Indutny) [#3198](https://github.com/nodejs/node/pull/3198)
* [[`651a5b51eb`](https://github.com/nodejs/node/commit/651a5b51eb)] - **buffer**: only check if instance is Uint8Array (Trevor Norris) [#3080](https://github.com/nodejs/node/pull/3080)
* [[`d5a1b1ad7c`](https://github.com/nodejs/node/commit/d5a1b1ad7c)] - **buffer**: clean up usage of __proto__ (Trevor Norris) [#3080](https://github.com/nodejs/node/pull/3080)
* [[`af24376e18`](https://github.com/nodejs/node/commit/af24376e18)] - **build**: Intl: deps: bump ICU to 56.1 (GA) (Steven R. Loomis) [#3281](https://github.com/nodejs/node/pull/3281)
* [[`9136359d57`](https://github.com/nodejs/node/commit/9136359d57)] - **build**: make icu download path customizable (Johan Bergström) [#3200](https://github.com/nodejs/node/pull/3200)
* [[`b3c5ad10a8`](https://github.com/nodejs/node/commit/b3c5ad10a8)] - **build**: add --with-arm-fpu option (Jérémy Lal) [#3228](https://github.com/nodejs/node/pull/3228)
* [[`f00f3268e4`](https://github.com/nodejs/node/commit/f00f3268e4)] - **build**: intl: avoid 'duplicate main()' on ICU 56 (Steven R. Loomis) [#3066](https://github.com/nodejs/node/pull/3066)
* [[`071c72a6a3`](https://github.com/nodejs/node/commit/071c72a6a3)] - **deps**: upgrade to npm 2.14.7 (Kat Marchán) [#3299](https://github.com/nodejs/node/pull/3299)
* [[`8b50e95f06`](https://github.com/nodejs/node/commit/8b50e95f06)] - **(SEMVER-MINOR)** **deps**: backport 1ee712a from V8 upstream (Julien Gilli) [#3036](https://github.com/nodejs/node/pull/3036)
* [[`747271372f`](https://github.com/nodejs/node/commit/747271372f)] - **doc**: update the assert module summary (David Boivin) [#2799](https://github.com/nodejs/node/pull/2799)
* [[`0d506556b0`](https://github.com/nodejs/node/commit/0d506556b0)] - **doc**: replace node-gyp link with nodejs/node-gyp (Roman Klauke) [#3320](https://github.com/nodejs/node/pull/3320)
* [[`40a159e4f4`](https://github.com/nodejs/node/commit/40a159e4f4)] - **doc**: Amend capitalization of word JavaScript (Dave Hodder) [#3285](https://github.com/nodejs/node/pull/3285)
* [[`6dd34761fd`](https://github.com/nodejs/node/commit/6dd34761fd)] - **doc**: add method links in dns.markdown (Alejandro Oviedo) [#3196](https://github.com/nodejs/node/pull/3196)
* [[`333e8336be`](https://github.com/nodejs/node/commit/333e8336be)] - **doc**: add method links in child_process.markdown (Alejandro Oviedo) [#3186](https://github.com/nodejs/node/pull/3186)
* [[`0cfc6d39ca`](https://github.com/nodejs/node/commit/0cfc6d39ca)] - **doc**: recommend Infinity on emitter.setMaxListeners (Jason Karns) [#2559](https://github.com/nodejs/node/pull/2559)
* [[`d4fc6d93ef`](https://github.com/nodejs/node/commit/d4fc6d93ef)] - **doc**: add help repo link to CONTRIBUTING.md (Doug Shamoo) [#3233](https://github.com/nodejs/node/pull/3233)
* [[`28aac7f19d`](https://github.com/nodejs/node/commit/28aac7f19d)] - **doc**: add TLS session resumption example (Roman Reiss) [#3147](https://github.com/nodejs/node/pull/3147)
* [[`365cf22cce`](https://github.com/nodejs/node/commit/365cf22cce)] - **doc**: update AUTHORS list (Rod Vagg) [#3211](https://github.com/nodejs/node/pull/3211)
* [[`d4399613b7`](https://github.com/nodejs/node/commit/d4399613b7)] - **doc**: standardize references to userland (Martial) [#3192](https://github.com/nodejs/node/pull/3192)
* [[`75de258376`](https://github.com/nodejs/node/commit/75de258376)] - **doc**: fix spelling in Buffer documentation (Rod Machen) [#3226](https://github.com/nodejs/node/pull/3226)
* [[`725c7276dd`](https://github.com/nodejs/node/commit/725c7276dd)] - **doc**: fix README.md link to joyent/node intl wiki (Steven R. Loomis) [#3067](https://github.com/nodejs/node/pull/3067)
* [[`4a35ba4966`](https://github.com/nodejs/node/commit/4a35ba4966)] - **(SEMVER-MINOR)** **fs**: include filename in watch errors (charlierudolph) [#2748](https://github.com/nodejs/node/pull/2748)
* [[`2ddbbfd164`](https://github.com/nodejs/node/commit/2ddbbfd164)] - **http**: cork/uncork before flushing pipelined res (Fedor Indutny) [#3172](https://github.com/nodejs/node/pull/3172)
* [[`f638402e2f`](https://github.com/nodejs/node/commit/f638402e2f)] - **http**: add comment about `outputSize` in res/server (Fedor Indutny) [#3128](https://github.com/nodejs/node/pull/3128)
* [[`1850879b0e`](https://github.com/nodejs/node/commit/1850879b0e)] - **js_stream**: prevent abort if isalive doesn't exist (Trevor Norris) [#3282](https://github.com/nodejs/node/pull/3282)
* [[`63644dd1cd`](https://github.com/nodejs/node/commit/63644dd1cd)] - **lib**: remove redundant code, add tests in timers.js (Rich Trott) [#3143](https://github.com/nodejs/node/pull/3143)
* [[`74f443583c`](https://github.com/nodejs/node/commit/74f443583c)] - **module**: use UNC paths when loading native addons (Justin Chase) [#2965](https://github.com/nodejs/node/pull/2965)
* [[`01cb3fc36b`](https://github.com/nodejs/node/commit/01cb3fc36b)] - **net**: don't throw on bytesWritten access (Trevor Norris) [#3305](https://github.com/nodejs/node/pull/3305)
* [[`9d65528b01`](https://github.com/nodejs/node/commit/9d65528b01)] - **(SEMVER-MINOR)** **node**: add -c|--check CLI arg to syntax check script (Dave Eddy) [#2411](https://github.com/nodejs/node/pull/2411)
* [[`42b936e78d`](https://github.com/nodejs/node/commit/42b936e78d)] - **(SEMVER-MINOR)** **src**: add process.release.lts property (Rod Vagg) [#3212](https://github.com/nodejs/node/pull/3212)
* [[`589287b2e3`](https://github.com/nodejs/node/commit/589287b2e3)] - **src**: convert BE-utf16-string to LE before search (Karl Skomski) [#3295](https://github.com/nodejs/node/pull/3295)
* [[`2314378f06`](https://github.com/nodejs/node/commit/2314378f06)] - **src**: fix u-a-free if uv returns err in ASYNC_CALL (Karl Skomski) [#3049](https://github.com/nodejs/node/pull/3049)
* [[`d99336a391`](https://github.com/nodejs/node/commit/d99336a391)] - **(SEMVER-MINOR)** **src**: replace naive search in Buffer::IndexOf (Karl Skomski) [#2539](https://github.com/nodejs/node/pull/2539)
* [[`546e8333ba`](https://github.com/nodejs/node/commit/546e8333ba)] - **(SEMVER-MINOR)** **src**: fix --abort-on-uncaught-exception (Jeremy Whitlock) [#3036](https://github.com/nodejs/node/pull/3036)
* [[`7271cb047c`](https://github.com/nodejs/node/commit/7271cb047c)] - **(SEMVER-MINOR)** **src**: add process.versions.icu (Evan Lucas) [#3102](https://github.com/nodejs/node/pull/3102)
* [[`7b9f78acb2`](https://github.com/nodejs/node/commit/7b9f78acb2)] - **stream**: avoid pause with unpipe in buffered write (Brian White) [#2325](https://github.com/nodejs/node/pull/2325)
* [[`f0f8afd879`](https://github.com/nodejs/node/commit/f0f8afd879)] - **test**: remove common.inspect() (Rich Trott) [#3257](https://github.com/nodejs/node/pull/3257)
* [[`5ca4f6f8bd`](https://github.com/nodejs/node/commit/5ca4f6f8bd)] - **test**: test `util` rather than `common` (Rich Trott) [#3256](https://github.com/nodejs/node/pull/3256)
* [[`7a5ae34345`](https://github.com/nodejs/node/commit/7a5ae34345)] - **test**: refresh temp directory when using pipe (Rich Trott) [#3231](https://github.com/nodejs/node/pull/3231)
* [[`7c85557ef0`](https://github.com/nodejs/node/commit/7c85557ef0)] - **test**: Fix test-fs-read-stream-fd-leak race cond (Junliang Yan) [#3218](https://github.com/nodejs/node/pull/3218)
* [[`26a7ec6960`](https://github.com/nodejs/node/commit/26a7ec6960)] - **test**: fix losing original env vars issue (Junliang Yan) [#3190](https://github.com/nodejs/node/pull/3190)
* [[`e922716192`](https://github.com/nodejs/node/commit/e922716192)] - **test**: remove deprecated error logging (Rich Trott) [#3079](https://github.com/nodejs/node/pull/3079)
* [[`8f29d95a8c`](https://github.com/nodejs/node/commit/8f29d95a8c)] - **test**: report timeout in TapReporter (Karl Skomski) [#2647](https://github.com/nodejs/node/pull/2647)
* [[`2d0fe4c657`](https://github.com/nodejs/node/commit/2d0fe4c657)] - **test**: linting for buffer-free-callback test (Rich Trott) [#3230](https://github.com/nodejs/node/pull/3230)
* [[`70c9e4337e`](https://github.com/nodejs/node/commit/70c9e4337e)] - **test**: make common.js mandatory via linting rule (Rich Trott) [#3157](https://github.com/nodejs/node/pull/3157)
* [[`b7179562aa`](https://github.com/nodejs/node/commit/b7179562aa)] - **test**: load common.js in all tests (Rich Trott) [#3157](https://github.com/nodejs/node/pull/3157)
* [[`bab555a1c1`](https://github.com/nodejs/node/commit/bab555a1c1)] - **test**: speed up stringbytes-external test (Evan Lucas) [#3005](https://github.com/nodejs/node/pull/3005)
* [[`ddf258376d`](https://github.com/nodejs/node/commit/ddf258376d)] - **test**: use normalize() for unicode paths (Roman Reiss) [#3007](https://github.com/nodejs/node/pull/3007)
* [[`46876d519c`](https://github.com/nodejs/node/commit/46876d519c)] - **test**: remove arguments.callee usage (Roman Reiss) [#3167](https://github.com/nodejs/node/pull/3167)
* [[`af10df6108`](https://github.com/nodejs/node/commit/af10df6108)] - **tls**: use parent handle's close callback (Fedor Indutny) [#2991](https://github.com/nodejs/node/pull/2991)
* [[`9c2748bad1`](https://github.com/nodejs/node/commit/9c2748bad1)] - **tools**: remove leftover license boilerplate (Nathan Rajlich) [#3225](https://github.com/nodejs/node/pull/3225)
* [[`5d9f83ff2a`](https://github.com/nodejs/node/commit/5d9f83ff2a)] - **tools**: apply linting to custom rules code (Rich Trott) [#3195](https://github.com/nodejs/node/pull/3195)
* [[`18a8b2ec73`](https://github.com/nodejs/node/commit/18a8b2ec73)] - **tools**: remove unused gflags module (Ben Noordhuis) [#3220](https://github.com/nodejs/node/pull/3220)
* [[`e0fffca836`](https://github.com/nodejs/node/commit/e0fffca836)] - **util**: fix for inspecting promises (Evan Lucas) [#3221](https://github.com/nodejs/node/pull/3221)
* [[`8dfdee3733`](https://github.com/nodejs/node/commit/8dfdee3733)] - **util**: correctly inspect Map/Set Iterators (Evan Lucas) [#3119](https://github.com/nodejs/node/pull/3119)
* [[`b5c51fdba0`](https://github.com/nodejs/node/commit/b5c51fdba0)] - **util**: fix check for Array constructor (Evan Lucas) [#3119](https://github.com/nodejs/node/pull/3119)

<a id="4.1.2"></a>
## 2015-10-05, Version 4.1.2 (Stable), @rvagg

### Notable changes

* **http**:
  - Fix out-of-order 'finish' event bug in pipelining that can abort execution, fixes DoS vulnerability [CVE-2015-7384](https://github.com/nodejs/node/issues/3138) (Fedor Indutny) [#3128](https://github.com/nodejs/node/pull/3128)
  - Account for pending response data instead of just the data on the current request to decide whether pause the socket or not (Fedor Indutny) [#3128](https://github.com/nodejs/node/pull/3128)
* **libuv**: Upgraded from v1.7.4 to v1.7.5, see [release notes](https://github.com/libuv/libuv/releases/tag/v1.7.5) for details (Saúl Ibarra Corretgé) [#3010](https://github.com/nodejs/node/pull/3010)
  - A better rwlock implementation for all Windows versions
  - Improved AIX support
* **v8**:
  - Upgraded from v4.5.103.33 to v4.5.103.35 (Ali Ijaz Sheikh) [#3117](https://github.com/nodejs/node/pull/3117)
  - Backported [f782159](https://codereview.chromium.org/1367123003) from v8's upstream to help speed up Promise introspection (Ben Noordhuis) [#3130](https://github.com/nodejs/node/pull/3130)
  - Backported [c281c15](https://codereview.chromium.org/1363683002) from v8's upstream to add JSTypedArray length in post-mortem metadata (Julien Gilli) [#3031](https://github.com/nodejs/node/pull/3031)

### Known issues

See https://github.com/nodejs/node/labels/confirmed-bug for complete and current list of known issues.

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`39b8730e8b`](https://github.com/nodejs/node/commit/39b8730e8b)] - **async_wrap**: ensure all objects have internal field (Trevor Norris) [#3139](https://github.com/nodejs/node/pull/3139)
* [[`99e66074d7`](https://github.com/nodejs/node/commit/99e66074d7)] - **async_wrap**: update providers and add test (Trevor Norris) [#3139](https://github.com/nodejs/node/pull/3139)
* [[`7a58157d4e`](https://github.com/nodejs/node/commit/7a58157d4e)] - **benchmark**: update comment in common.js (Minwoo Jung) [#2399](https://github.com/nodejs/node/pull/2399)
* [[`9e9bfa4dc0`](https://github.com/nodejs/node/commit/9e9bfa4dc0)] - **build**: iojs -> nodejs of release-urlbase (Minqi Pan) [#3015](https://github.com/nodejs/node/pull/3015)
* [[`8335ec7191`](https://github.com/nodejs/node/commit/8335ec7191)] - **build**: fix some typos inside the configure script (Minqi Pan) [#3016](https://github.com/nodejs/node/pull/3016)
* [[`d6ac547d5d`](https://github.com/nodejs/node/commit/d6ac547d5d)] - **build,win**: fix node.exe resource version (João Reis) [#3053](https://github.com/nodejs/node/pull/3053)
* [[`798dad24f4`](https://github.com/nodejs/node/commit/798dad24f4)] - **child_process**: `null` channel handle on close (Fedor Indutny) [#3041](https://github.com/nodejs/node/pull/3041)
* [[`e5615854ea`](https://github.com/nodejs/node/commit/e5615854ea)] - **contextify**: use CHECK instead of `if` (Oguz Bastemur) [#3125](https://github.com/nodejs/node/pull/3125)
* [[`f055a66a38`](https://github.com/nodejs/node/commit/f055a66a38)] - **crypto**: enable FIPS only when configured with it (Fedor Indutny) [#3153](https://github.com/nodejs/node/pull/3153)
* [[`4c8d96bc30`](https://github.com/nodejs/node/commit/4c8d96bc30)] - **crypto**: add more keylen sanity checks in pbkdf2 (Johann) [#3029](https://github.com/nodejs/node/pull/3029)
* [[`4c5940776c`](https://github.com/nodejs/node/commit/4c5940776c)] - **deps**: upgrade libuv to 1.7.5 (Saúl Ibarra Corretgé) [#3010](https://github.com/nodejs/node/pull/3010)
* [[`5a9e795577`](https://github.com/nodejs/node/commit/5a9e795577)] - **deps**: upgrade V8 to 4.5.103.35 (Ali Ijaz Sheikh) [#3117](https://github.com/nodejs/node/pull/3117)
* [[`925b29f959`](https://github.com/nodejs/node/commit/925b29f959)] - **deps**: backport f782159 from v8's upstream (Ben Noordhuis) [#3130](https://github.com/nodejs/node/pull/3130)
* [[`039f73fa83`](https://github.com/nodejs/node/commit/039f73fa83)] - **deps**: remove and gitignore .bin directory (Ben Noordhuis) [#3004](https://github.com/nodejs/node/pull/3004)
* [[`5fbb24812d`](https://github.com/nodejs/node/commit/5fbb24812d)] - **deps**: backport c281c15 from V8's upstream (Julien Gilli) [#3031](https://github.com/nodejs/node/pull/3031)
* [[`6ee5d0f69f`](https://github.com/nodejs/node/commit/6ee5d0f69f)] - **dns**: add missing exports.BADNAME (Roman Reiss) [#3051](https://github.com/nodejs/node/pull/3051)
* [[`f92aee7170`](https://github.com/nodejs/node/commit/f92aee7170)] - **doc**: fix outdated 'try/catch' statement in sync (Minwoo Jung) [#3087](https://github.com/nodejs/node/pull/3087)
* [[`c7161f39e8`](https://github.com/nodejs/node/commit/c7161f39e8)] - **doc**: add TSC meeting minutes 2015-09-16 (Rod Vagg) [#3023](https://github.com/nodejs/node/pull/3023)
* [[`928166c4a8`](https://github.com/nodejs/node/commit/928166c4a8)] - **doc**: copyedit fs.watch() information (Rich Trott) [#3097](https://github.com/nodejs/node/pull/3097)
* [[`75d5dcea76`](https://github.com/nodejs/node/commit/75d5dcea76)] - **doc**: jenkins-iojs.nodesource.com -> ci.nodejs.org (Michał Gołębiowski) [#2886](https://github.com/nodejs/node/pull/2886)
* [[`5c3f50b21d`](https://github.com/nodejs/node/commit/5c3f50b21d)] - **doc**: rearrange execSync and execFileSync (Laurent Fortin) [#2940](https://github.com/nodejs/node/pull/2940)
* [[`4fc33ac11a`](https://github.com/nodejs/node/commit/4fc33ac11a)] - **doc**: make execFileSync in line with execFile (Laurent Fortin) [#2940](https://github.com/nodejs/node/pull/2940)
* [[`a366e84b17`](https://github.com/nodejs/node/commit/a366e84b17)] - **doc**: fix typos in cluster & errors (reggi) [#3011](https://github.com/nodejs/node/pull/3011)
* [[`52031e1bf1`](https://github.com/nodejs/node/commit/52031e1bf1)] - **doc**: switch LICENSE from closure-linter to eslint (Minqi Pan) [#3018](https://github.com/nodejs/node/pull/3018)
* [[`b28f6a53bc`](https://github.com/nodejs/node/commit/b28f6a53bc)] - **docs**: Clarify assert.doesNotThrow behavior (Fabio Oliveira) [#2807](https://github.com/nodejs/node/pull/2807)
* [[`99943e189d`](https://github.com/nodejs/node/commit/99943e189d)] - **http**: fix out-of-order 'finish' bug in pipelining (Fedor Indutny) [#3128](https://github.com/nodejs/node/pull/3128)
* [[`fb7a491d1c`](https://github.com/nodejs/node/commit/fb7a491d1c)] - **http_server**: pause socket properly (Fedor Indutny) [#3128](https://github.com/nodejs/node/pull/3128)
* [[`a0b35bfcf3`](https://github.com/nodejs/node/commit/a0b35bfcf3)] - **i18n**: add caller to removal list for bidi in ICU55 (Michael Dawson) [#3115](https://github.com/nodejs/node/pull/3115)
* [[`ac2bce0b0c`](https://github.com/nodejs/node/commit/ac2bce0b0c)] - **path**: improve posixSplitPath performance (Evan Lucas) [#3034](https://github.com/nodejs/node/pull/3034)
* [[`37cdeafa2f`](https://github.com/nodejs/node/commit/37cdeafa2f)] - **smalloc**: remove module (Brendan Ashworth) [#3099](https://github.com/nodejs/node/pull/3099)
* [[`5ec5d0aa8b`](https://github.com/nodejs/node/commit/5ec5d0aa8b)] - **src**: internalize binding function property names (Ben Noordhuis) [#3060](https://github.com/nodejs/node/pull/3060)
* [[`c8175fc2af`](https://github.com/nodejs/node/commit/c8175fc2af)] - **src**: internalize per-isolate string properties (Ben Noordhuis) [#3060](https://github.com/nodejs/node/pull/3060)
* [[`9a593abc47`](https://github.com/nodejs/node/commit/9a593abc47)] - **src**: include signal.h in util.h (Cheng Zhao) [#3058](https://github.com/nodejs/node/pull/3058)
* [[`fde0c6f321`](https://github.com/nodejs/node/commit/fde0c6f321)] - **src**: fix function and variable names in comments (Sakthipriyan Vairamani) [#3039](https://github.com/nodejs/node/pull/3039)
* [[`1cc7b41ba4`](https://github.com/nodejs/node/commit/1cc7b41ba4)] - **stream_wrap**: support empty `TryWrite`s (Fedor Indutny) [#3128](https://github.com/nodejs/node/pull/3128)
* [[`9faf4c6fcf`](https://github.com/nodejs/node/commit/9faf4c6fcf)] - **test**: load common.js to test for global leaks (Rich Trott) [#3095](https://github.com/nodejs/node/pull/3095)
* [[`0858c86374`](https://github.com/nodejs/node/commit/0858c86374)] - **test**: fix invalid variable name (Sakthipriyan Vairamani) [#3150](https://github.com/nodejs/node/pull/3150)
* [[`1167171004`](https://github.com/nodejs/node/commit/1167171004)] - **test**: change calls to deprecated util.print() (Rich Trott) [#3083](https://github.com/nodejs/node/pull/3083)
* [[`5ada45bf28`](https://github.com/nodejs/node/commit/5ada45bf28)] - **test**: replace deprecated util.debug() calls (Rich Trott) [#3082](https://github.com/nodejs/node/pull/3082)
* [[`d8ab4e185d`](https://github.com/nodejs/node/commit/d8ab4e185d)] - **util**: optimize promise introspection (Ben Noordhuis) [#3130](https://github.com/nodejs/node/pull/3130)

<a id="4.1.1"></a>
## 2015-09-22, Version 4.1.1 (Stable), @rvagg

### Notable changes

* **buffer**: Fixed a bug introduced in v4.1.0 where allocating a new zero-length buffer can result in the _next_ allocation of a TypedArray in JavaScript not being zero-filled. In certain circumstances this could result in data leakage via reuse of memory space in TypedArrays, breaking the normally safe assumption that TypedArrays should be always zero-filled. (Trevor Norris) [#2931](https://github.com/nodejs/node/pull/2931).
* **http**: Guard against response-splitting of HTTP trailing headers added via [`response.addTrailers()`](https://nodejs.org/api/http.html#http_response_addtrailers_headers) by removing new-line (`[\r\n]`) characters from values. Note that standard header values are already stripped of new-line characters. The expected security impact is low because trailing headers are rarely used. (Ben Noordhuis) [#2945](https://github.com/nodejs/node/pull/2945).
* **npm**: Upgrade to npm 2.14.4 from 2.14.3, see [release notes](https://github.com/npm/npm/releases/tag/v2.14.4) for full details (Kat Marchán) [#2958](https://github.com/nodejs/node/pull/2958)
  - Upgrades `graceful-fs` on multiple dependencies to no longer rely on monkey-patching `fs`
  - Fix `npm link` for pre-release / RC builds of Node
* **v8**: Update post-mortem metadata to allow post-mortem debugging tools to find and inspect:
  - JavaScript objects that use dictionary properties (Julien Gilli) [#2959](https://github.com/nodejs/node/pull/2959)
  - ScopeInfo and thus closures (Julien Gilli) [#2974](https://github.com/nodejs/node/pull/2974)

### Known issues

See https://github.com/nodejs/node/labels/confirmed-bug for complete and current list of known issues.

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`d63e02e08d`](https://github.com/nodejs/node/commit/d63e02e08d)] - **buffer**: don't set zero fill for zero-length buffer (Trevor Norris) [#2931](https://github.com/nodejs/node/pull/2931)
* [[`5905b14bff`](https://github.com/nodejs/node/commit/5905b14bff)] - **build**: fix icutrim when building small-icu on BE (Stewart Addison) [#2602](https://github.com/nodejs/node/pull/2602)
* [[`f010cb5d96`](https://github.com/nodejs/node/commit/f010cb5d96)] - **configure**: detect mipsel host (Jérémy Lal) [#2971](https://github.com/nodejs/node/pull/2971)
* [[`b93ad5abbd`](https://github.com/nodejs/node/commit/b93ad5abbd)] - **deps**: backport 357e6b9 from V8's upstream (Julien Gilli) [#2974](https://github.com/nodejs/node/pull/2974)
* [[`8da3da4d41`](https://github.com/nodejs/node/commit/8da3da4d41)] - **deps**: backport ff7d70b from V8's upstream (Julien Gilli) [#2959](https://github.com/nodejs/node/pull/2959)
* [[`2600fb8ae6`](https://github.com/nodejs/node/commit/2600fb8ae6)] - **deps**: upgraded to node-gyp@3.0.3 in npm (Kat Marchán) [#2958](https://github.com/nodejs/node/pull/2958)
* [[`793aad2d7a`](https://github.com/nodejs/node/commit/793aad2d7a)] - **deps**: upgrade to npm 2.14.4 (Kat Marchán) [#2958](https://github.com/nodejs/node/pull/2958)
* [[`43e2b7f836`](https://github.com/nodejs/node/commit/43e2b7f836)] - **doc**: remove usage of events.EventEmitter (Sakthipriyan Vairamani) [#2921](https://github.com/nodejs/node/pull/2921)
* [[`9c59d2f16a`](https://github.com/nodejs/node/commit/9c59d2f16a)] - **doc**: remove extra using v8::HandleScope statement (Christopher J. Brody) [#2983](https://github.com/nodejs/node/pull/2983)
* [[`f7edbab367`](https://github.com/nodejs/node/commit/f7edbab367)] - **doc**: clarify description of assert.ifError() (Rich Trott) [#2941](https://github.com/nodejs/node/pull/2941)
* [[`b2ddf0f9a2`](https://github.com/nodejs/node/commit/b2ddf0f9a2)] - **doc**: refine process.kill() and exit explanations (Rich Trott) [#2918](https://github.com/nodejs/node/pull/2918)
* [[`f68fed2e6f`](https://github.com/nodejs/node/commit/f68fed2e6f)] - **http**: remove redundant code in _deferToConnect (Malcolm Ahoy) [#2769](https://github.com/nodejs/node/pull/2769)
* [[`f542e74c93`](https://github.com/nodejs/node/commit/f542e74c93)] - **http**: guard against response splitting in trailers (Ben Noordhuis) [#2945](https://github.com/nodejs/node/pull/2945)
* [[`bc9f629387`](https://github.com/nodejs/node/commit/bc9f629387)] - **http_parser**: do not dealloc during kOnExecute (Fedor Indutny) [#2956](https://github.com/nodejs/node/pull/2956)
* [[`1860e0cebd`](https://github.com/nodejs/node/commit/1860e0cebd)] - **lib,src**: remove usage of events.EventEmitter (Sakthipriyan Vairamani) [#2921](https://github.com/nodejs/node/pull/2921)
* [[`d4cd5ac407`](https://github.com/nodejs/node/commit/d4cd5ac407)] - **readline**: fix tab completion bug (Matt Harrison) [#2816](https://github.com/nodejs/node/pull/2816)
* [[`9760e04839`](https://github.com/nodejs/node/commit/9760e04839)] - **repl**: don't use tty control codes when $TERM is set to "dumb" (Salman Aljammaz) [#2712](https://github.com/nodejs/node/pull/2712)
* [[`cb971cc97d`](https://github.com/nodejs/node/commit/cb971cc97d)] - **repl**: backslash bug fix (Sakthipriyan Vairamani) [#2968](https://github.com/nodejs/node/pull/2968)
* [[`2034f68668`](https://github.com/nodejs/node/commit/2034f68668)] - **src**: honor --abort_on_uncaught_exception flag (Evan Lucas) [#2776](https://github.com/nodejs/node/pull/2776)
* [[`0b1ca4a9ef`](https://github.com/nodejs/node/commit/0b1ca4a9ef)] - **src**: Add ABORT macro (Evan Lucas) [#2776](https://github.com/nodejs/node/pull/2776)
* [[`4519dd00f9`](https://github.com/nodejs/node/commit/4519dd00f9)] - **test**: test sync version of mkdir & rmdir (Sakthipriyan Vairamani) [#2588](https://github.com/nodejs/node/pull/2588)
* [[`816f609c8b`](https://github.com/nodejs/node/commit/816f609c8b)] - **test**: use tmpDir instead of fixtures in readdir (Sakthipriyan Vairamani) [#2587](https://github.com/nodejs/node/pull/2587)
* [[`2084f52585`](https://github.com/nodejs/node/commit/2084f52585)] - **test**: test more http response splitting scenarios (Ben Noordhuis) [#2945](https://github.com/nodejs/node/pull/2945)
* [[`fa08d1d8a1`](https://github.com/nodejs/node/commit/fa08d1d8a1)] - **test**: add test-spawn-cmd-named-pipe (Alexis Campailla) [#2770](https://github.com/nodejs/node/pull/2770)
* [[`71b5d80682`](https://github.com/nodejs/node/commit/71b5d80682)] - **test**: make cluster tests more time tolerant (Michael Dawson) [#2891](https://github.com/nodejs/node/pull/2891)
* [[`3e09dcfc32`](https://github.com/nodejs/node/commit/3e09dcfc32)] - **test**: update cwd-enoent tests for AIX (Imran Iqbal) [#2909](https://github.com/nodejs/node/pull/2909)
* [[`6ea8ec1c59`](https://github.com/nodejs/node/commit/6ea8ec1c59)] - **tools**: single, cross-platform tick processor (Matt Loring) [#2868](https://github.com/nodejs/node/pull/2868)

<a id="4.1.0"></a>
## 2015-09-17, Version 4.1.0 (Stable), @Fishrock123

### Notable changes

* **buffer**:
  - Buffers are now created in JavaScript, rather than C++. This increases the speed of buffer creation (Trevor Norris) [#2866](https://github.com/nodejs/node/pull/2866).
  - `Buffer#slice()` now uses `Uint8Array#subarray()` internally, increasing `slice()` performance (Karl Skomski) [#2777](https://github.com/nodejs/node/pull/2777).
* **fs**:
  - `fs.utimes()` now properly converts numeric strings, `NaN`, and `Infinity` (Yazhong Liu) [#2387](https://github.com/nodejs/node/pull/2387).
  - `fs.WriteStream` now implements `_writev`, allowing for super-fast bulk writes (Ron Korving) [#2167](https://github.com/nodejs/node/pull/2167).
* **http**: Fixed an issue with certain `write()` sizes causing errors when using `http.request()` (Fedor Indutny) [#2824](https://github.com/nodejs/node/pull/2824).
* **npm**: Upgrade to version 2.14.3, see https://github.com/npm/npm/releases/tag/v2.14.3 for more details (Kat Marchán) [#2822](https://github.com/nodejs/node/pull/2822).
* **src**: V8 cpu profiling no longer erroneously shows idle time (Oleksandr Chekhovskyi) [#2324](https://github.com/nodejs/node/pull/2324).
* **timers**: `#ref()` and `#unref()` now return the timer they belong to (Sam Roberts) [#2905](https://github.com/nodejs/node/pull/2905).
* **v8**: Lateral upgrade to 4.5.103.33 from 4.5.103.30, contains minor fixes (Ali Ijaz Sheikh) [#2870](https://github.com/nodejs/node/pull/2870).
  - This fixes a previously known bug where some computed object shorthand properties did not work correctly ([#2507](https://github.com/nodejs/node/issues/2507)).

### Known issues

See https://github.com/nodejs/node/labels/confirmed-bug for complete and current list of known issues.

* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`b1abe812cd`](https://github.com/nodejs/node/commit/b1abe812cd)] - Working on 4.0.1 (Rod Vagg)
* [[`f9f8378853`](https://github.com/nodejs/node/commit/f9f8378853)] - 2015-09-08, Version 4.0.0 (Stable) Release (Rod Vagg)
* [[`9683e5df51`](https://github.com/nodejs/node/commit/9683e5df51)] - **bindings**: close after reading module struct (Fedor Indutny) [#2792](https://github.com/nodejs/node/pull/2792)
* [[`4b4cfa2d44`](https://github.com/nodejs/node/commit/4b4cfa2d44)] - **buffer**: always allocate typed arrays outside heap (Trevor Norris) [#2893](https://github.com/nodejs/node/pull/2893)
* [[`7df018a29b`](https://github.com/nodejs/node/commit/7df018a29b)] - **buffer**: construct Uint8Array in JS (Trevor Norris) [#2866](https://github.com/nodejs/node/pull/2866)
* [[`43397b204e`](https://github.com/nodejs/node/commit/43397b204e)] - **(SEMVER-MINOR)** **build**: Updates to enable AIX support (Michael Dawson) [#2364](https://github.com/nodejs/node/pull/2364)
* [[`e35b1fd610`](https://github.com/nodejs/node/commit/e35b1fd610)] - **build**: clean up the generated tap file (Sakthipriyan Vairamani) [#2837](https://github.com/nodejs/node/pull/2837)
* [[`96670ebe37`](https://github.com/nodejs/node/commit/96670ebe37)] - **deps**: backport 6d32be2 from v8's upstream (Michaël Zasso) [#2916](https://github.com/nodejs/node/pull/2916)
* [[`94972d5b13`](https://github.com/nodejs/node/commit/94972d5b13)] - **deps**: backport 0d01728 from v8's upstream (Fedor Indutny) [#2912](https://github.com/nodejs/node/pull/2912)
* [[`7ebd881c29`](https://github.com/nodejs/node/commit/7ebd881c29)] - **deps**: upgrade V8 to 4.5.103.33 (Ali Ijaz Sheikh) [#2870](https://github.com/nodejs/node/pull/2870)
* [[`ed47ab6e44`](https://github.com/nodejs/node/commit/ed47ab6e44)] - **deps**: upgraded to node-gyp@3.0.3 in npm (Kat Marchán) [#2822](https://github.com/nodejs/node/pull/2822)
* [[`f4641ae875`](https://github.com/nodejs/node/commit/f4641ae875)] - **deps**: upgrade to npm 2.14.3 (Kat Marchán) [#2822](https://github.com/nodejs/node/pull/2822)
* [[`8119693a3d`](https://github.com/nodejs/node/commit/8119693a3d)] - **deps**: update libuv to version 1.7.4 (Saúl Ibarra Corretgé) [#2817](https://github.com/nodejs/node/pull/2817)
* [[`6098504685`](https://github.com/nodejs/node/commit/6098504685)] - **deps**: cherry-pick 6da51b4 from v8's upstream (Fedor Indutny) [#2801](https://github.com/nodejs/node/pull/2801)
* [[`bf42cc8dba`](https://github.com/nodejs/node/commit/bf42cc8dba)] - **doc**: process exit event is not guaranteed to fire (Rich Trott) [#2861](https://github.com/nodejs/node/pull/2861)
* [[`bb0f869f67`](https://github.com/nodejs/node/commit/bb0f869f67)] - **doc**: remove incorrect reference to TCP in net docs (Sam Roberts) [#2903](https://github.com/nodejs/node/pull/2903)
* [[`302d59dce8`](https://github.com/nodejs/node/commit/302d59dce8)] - **doc**: correct buffer.slice arg syntax (Sam Roberts) [#2903](https://github.com/nodejs/node/pull/2903)
* [[`74db9637b7`](https://github.com/nodejs/node/commit/74db9637b7)] - **doc**: describe spawn option.detached (Sam Roberts) [#2903](https://github.com/nodejs/node/pull/2903)
* [[`a7bd897273`](https://github.com/nodejs/node/commit/a7bd897273)] - **doc**: rename from iojs(1) to node(1) in benchmarks (Dmitry Vasilyev) [#2884](https://github.com/nodejs/node/pull/2884)
* [[`cd643d7c37`](https://github.com/nodejs/node/commit/cd643d7c37)] - **doc**: add missing backtick in buffer.markdown (Sven Slootweg) [#2881](https://github.com/nodejs/node/pull/2881)
* [[`e8a206e802`](https://github.com/nodejs/node/commit/e8a206e802)] - **doc**: fix broken link in repl.markdown (Danny Nemer) [#2827](https://github.com/nodejs/node/pull/2827)
* [[`7ee36d61f7`](https://github.com/nodejs/node/commit/7ee36d61f7)] - **doc**: fix typos in README (Ionică Bizău) [#2852](https://github.com/nodejs/node/pull/2852)
* [[`4d1ae26196`](https://github.com/nodejs/node/commit/4d1ae26196)] - **doc**: add tunniclm as a collaborator (Mike Tunnicliffe) [#2826](https://github.com/nodejs/node/pull/2826)
* [[`2d77d03643`](https://github.com/nodejs/node/commit/2d77d03643)] - **doc**: fix two doc errors in stream and process (Jeremiah Senkpiel) [#2549](https://github.com/nodejs/node/pull/2549)
* [[`55ac24f721`](https://github.com/nodejs/node/commit/55ac24f721)] - **doc**: fixed io.js references in process.markdown (Tristian Flanagan) [#2846](https://github.com/nodejs/node/pull/2846)
* [[`cd1297fb57`](https://github.com/nodejs/node/commit/cd1297fb57)] - **doc**: use "Calls" over "Executes" for consistency (Minwoo Jung) [#2800](https://github.com/nodejs/node/pull/2800)
* [[`d664b95581`](https://github.com/nodejs/node/commit/d664b95581)] - **doc**: use US English for consistency (Anne-Gaelle Colom) [#2784](https://github.com/nodejs/node/pull/2784)
* [[`82ba1839fb`](https://github.com/nodejs/node/commit/82ba1839fb)] - **doc**: use 3rd person singular for consistency (Anne-Gaelle Colom) [#2765](https://github.com/nodejs/node/pull/2765)
* [[`432cce6e95`](https://github.com/nodejs/node/commit/432cce6e95)] - **doc**: describe process API for IPC (Sam Roberts) [#1978](https://github.com/nodejs/node/pull/1978)
* [[`1d75012b9d`](https://github.com/nodejs/node/commit/1d75012b9d)] - **doc**: fix comma splice in Assertion Testing doc (Rich Trott) [#2728](https://github.com/nodejs/node/pull/2728)
* [[`6108ea9bb4`](https://github.com/nodejs/node/commit/6108ea9bb4)] - **fs**: consider NaN/Infinity in toUnixTimestamp (Yazhong Liu) [#2387](https://github.com/nodejs/node/pull/2387)
* [[`2b6aa9415f`](https://github.com/nodejs/node/commit/2b6aa9415f)] - **(SEMVER-MINOR)** **fs**: implemented WriteStream#writev (Ron Korving) [#2167](https://github.com/nodejs/node/pull/2167)
* [[`431bf74c55`](https://github.com/nodejs/node/commit/431bf74c55)] - **http**: default Agent.getName to 'localhost' (Malcolm Ahoy) [#2825](https://github.com/nodejs/node/pull/2825)
* [[`ea15d71c16`](https://github.com/nodejs/node/commit/ea15d71c16)] - **http_server**: fix resume after socket close (Fedor Indutny) [#2824](https://github.com/nodejs/node/pull/2824)
* [[`8e5843405b`](https://github.com/nodejs/node/commit/8e5843405b)] - **src**: null env_ field from constructor (Trevor Norris) [#2913](https://github.com/nodejs/node/pull/2913)
* [[`0a5f80a11f`](https://github.com/nodejs/node/commit/0a5f80a11f)] - **src**: use subarray() in Buffer#slice() for speedup (Karl Skomski) [#2777](https://github.com/nodejs/node/pull/2777)
* [[`57707e2490`](https://github.com/nodejs/node/commit/57707e2490)] - **src**: use ZCtxt as a source for v8::Isolates (Roman Klauke) [#2547](https://github.com/nodejs/node/pull/2547)
* [[`b0df2273ab`](https://github.com/nodejs/node/commit/b0df2273ab)] - **src**: fix v8::CpuProfiler idle sampling (Oleksandr Chekhovskyi) [#2324](https://github.com/nodejs/node/pull/2324)
* [[`eaa8e60b91`](https://github.com/nodejs/node/commit/eaa8e60b91)] - **streams**: refactor LazyTransform to internal/ (Brendan Ashworth) [#2566](https://github.com/nodejs/node/pull/2566)
* [[`648c003e14`](https://github.com/nodejs/node/commit/648c003e14)] - **test**: use tmp directory in chdir test (Sakthipriyan Vairamani) [#2589](https://github.com/nodejs/node/pull/2589)
* [[`079a2173d4`](https://github.com/nodejs/node/commit/079a2173d4)] - **test**: fix Buffer OOM error message (Trevor Norris) [#2915](https://github.com/nodejs/node/pull/2915)
* [[`52019a1b21`](https://github.com/nodejs/node/commit/52019a1b21)] - **test**: fix default value for additional param (Sakthipriyan Vairamani) [#2553](https://github.com/nodejs/node/pull/2553)
* [[`5df5d0423a`](https://github.com/nodejs/node/commit/5df5d0423a)] - **test**: remove disabled test (Rich Trott) [#2841](https://github.com/nodejs/node/pull/2841)
* [[`9e5f0995bd`](https://github.com/nodejs/node/commit/9e5f0995bd)] - **test**: split up internet dns tests (Rich Trott) [#2802](https://github.com/nodejs/node/pull/2802)
* [[`41f2dde51a`](https://github.com/nodejs/node/commit/41f2dde51a)] - **test**: increase dgram timeout for armv6 (Rich Trott) [#2808](https://github.com/nodejs/node/pull/2808)
* [[`6e2fe1c21a`](https://github.com/nodejs/node/commit/6e2fe1c21a)] - **test**: remove valid hostname check in test-dns.js (Rich Trott) [#2785](https://github.com/nodejs/node/pull/2785)
* [[`779e14f1a7`](https://github.com/nodejs/node/commit/779e14f1a7)] - **test**: expect error for test_lookup_ipv6_hint on FreeBSD (Rich Trott) [#2724](https://github.com/nodejs/node/pull/2724)
* [[`f931b9dd95`](https://github.com/nodejs/node/commit/f931b9dd95)] - **(SEMVER-MINOR)** **timer**: ref/unref return self (Sam Roberts) [#2905](https://github.com/nodejs/node/pull/2905)
* [[`59d03738cc`](https://github.com/nodejs/node/commit/59d03738cc)] - **tools**: enable arrow functions in .eslintrc (Sakthipriyan Vairamani) [#2840](https://github.com/nodejs/node/pull/2840)
* [[`69e7b875a2`](https://github.com/nodejs/node/commit/69e7b875a2)] - **tools**: open `test.tap` file in write-binary mode (Sakthipriyan Vairamani) [#2837](https://github.com/nodejs/node/pull/2837)
* [[`ff6d30d784`](https://github.com/nodejs/node/commit/ff6d30d784)] - **tools**: add missing tick processor polyfill (Matt Loring) [#2694](https://github.com/nodejs/node/pull/2694)
* [[`519caba021`](https://github.com/nodejs/node/commit/519caba021)] - **tools**: fix flakiness in test-tick-processor (Matt Loring) [#2694](https://github.com/nodejs/node/pull/2694)
* [[`ac004b8555`](https://github.com/nodejs/node/commit/ac004b8555)] - **tools**: remove hyphen in TAP result (Sakthipriyan Vairamani) [#2718](https://github.com/nodejs/node/pull/2718)
* [[`ba47511976`](https://github.com/nodejs/node/commit/ba47511976)] - **tsc**: adjust TSC membership for IBM+StrongLoop (James M Snell) [#2858](https://github.com/nodejs/node/pull/2858)
* [[`e035266805`](https://github.com/nodejs/node/commit/e035266805)] - **win,msi**: fix documentation shortcut url (Brian White) [#2781](https://github.com/nodejs/node/pull/2781)

<a id="4.0.0"></a>
## 2015-09-08, Version 4.0.0 (Stable), @rvagg

### Notable changes

This list of changes is relative to the last io.js v3.x branch release, v3.3.0. Please see the list of notable changes in the v3.x, v2.x and v1.x releases for a more complete list of changes from 0.12.x. Note, that some changes in the v3.x series as well as major breaking changes in this release constitute changes required for full convergence of the Node.js and io.js projects.

* **child_process**: `ChildProcess.prototype.send()` and `process.send()` operate asynchronously across all platforms so an optional callback parameter has been introduced that will be invoked once the message has been sent, i.e. `.send(message[, sendHandle][, callback])` (Ben Noordhuis) [#2620](https://github.com/nodejs/node/pull/2620).
* **node**: Rename "io.js" code to "Node.js" (cjihrig) [#2367](https://github.com/nodejs/node/pull/2367).
* **node-gyp**: This release bundles an updated version of node-gyp that works with all versions of Node.js and io.js including nightly and release candidate builds. From io.js v3 and Node.js v4 onward, it will only download a headers tarball when building addons rather than the entire source. (Rod Vagg) [#2700](https://github.com/nodejs/node/pull/2700)
* **npm**: Upgrade to version 2.14.2 from 2.13.3, includes a security update, see https://github.com/npm/npm/releases/tag/v2.14.2 for more details, (Kat Marchán) [#2696](https://github.com/nodejs/node/pull/2696).
* **timers**: Improved timer performance from porting the 0.12 implementation, plus minor fixes (Jeremiah Senkpiel) [#2540](https://github.com/nodejs/node/pull/2540), (Julien Gilli) [nodejs/node-v0.x-archive#8751](https://github.com/nodejs/node-v0.x-archive/pull/8751) [nodejs/node-v0.x-archive#8905](https://github.com/nodejs/node-v0.x-archive/pull/8905)
* **util**: The `util.is*()` functions have been deprecated, beginning with deprecation warnings in the documentation for this release, users are encouraged to seek more robust alternatives in the npm registry, (Sakthipriyan Vairamani) [#2447](https://github.com/nodejs/node/pull/2447).
* **v8**: Upgrade to version 4.5.103.30 from 4.4.63.30 (Ali Ijaz Sheikh) [#2632](https://github.com/nodejs/node/pull/2632).
  - Implement new `TypedArray` prototype methods: `copyWithin()`, `every()`, `fill()`, `filter()`, `find()`, `findIndex()`, `forEach()`, `indexOf()`, `join()`, `lastIndexOf()`, `map()`, `reduce()`, `reduceRight()`, `reverse()`, `slice()`, `some()`, `sort()`. See https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray for further information.
  - Implement new `TypedArray.from()` and `TypedArray.of()` functions. See https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray for further information.
  - Implement arrow functions, see https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions for further information.
  - Full ChangeLog available at https://github.com/v8/v8-git-mirror/blob/4.5.103/ChangeLog

### Known issues

See https://github.com/nodejs/node/labels/confirmed-bug for complete and current list of known issues.

* Some uses of computed object shorthand properties are not handled correctly by the current version of V8. e.g. `[{ [prop]: val }]` evaluates to `[{}]`. [#2507](https://github.com/nodejs/node/issues/2507)
* Some problems with unreferenced timers running during `beforeExit` are still to be resolved. See [#1264](https://github.com/nodejs/node/issues/1264).
* Surrogate pair in REPL can freeze terminal. [#690](https://github.com/nodejs/node/issues/690)
* Calling `dns.setServers()` while a DNS query is in progress can cause the process to crash on a failed assertion. [#894](https://github.com/nodejs/node/issues/894)
* `url.resolve` may transfer the auth portion of the url when resolving between two full hosts, see [#1435](https://github.com/nodejs/node/issues/1435).

### Commits

* [[`4f50d3fb90`](https://github.com/nodejs/node/commit/4f50d3fb90)] - **(SEMVER-MAJOR)** This commit sets the value of process.release.name to "node". (cjihrig) [#2367](https://github.com/nodejs/node/pull/2367)
* [[`d3178d8b1b`](https://github.com/nodejs/node/commit/d3178d8b1b)] - **buffer**: SlowBuffer only accept valid numeric values (Michaël Zasso) [#2635](https://github.com/nodejs/node/pull/2635)
* [[`0cb0f4a6e4`](https://github.com/nodejs/node/commit/0cb0f4a6e4)] - **build**: fix v8_enable_handle_zapping override (Karl Skomski) [#2731](https://github.com/nodejs/node/pull/2731)
* [[`a7596d7efc`](https://github.com/nodejs/node/commit/a7596d7efc)] - **build**: remote commands on staging in single session (Rod Vagg) [#2717](https://github.com/nodejs/node/pull/2717)
* [[`be427e9efa`](https://github.com/nodejs/node/commit/be427e9efa)] - **build**: make .msi install to "nodejs", not "node" (Rod Vagg) [#2701](https://github.com/nodejs/node/pull/2701)
* [[`5652ce0dbc`](https://github.com/nodejs/node/commit/5652ce0dbc)] - **build**: fix .pkg creation tooling (Rod Vagg) [#2687](https://github.com/nodejs/node/pull/2687)
* [[`101db80111`](https://github.com/nodejs/node/commit/101db80111)] - **build**: add --enable-asan with builtin leakcheck (Karl Skomski) [#2376](https://github.com/nodejs/node/pull/2376)
* [[`2c3939c9c0`](https://github.com/nodejs/node/commit/2c3939c9c0)] - **child_process**: use stdio.fd even if it is 0 (Evan Lucas) [#2727](https://github.com/nodejs/node/pull/2727)
* [[`609db5a1dd`](https://github.com/nodejs/node/commit/609db5a1dd)] - **child_process**: check execFile and fork args (James M Snell) [#2667](https://github.com/nodejs/node/pull/2667)
* [[`d010568c23`](https://github.com/nodejs/node/commit/d010568c23)] - **(SEMVER-MAJOR)** **child_process**: add callback parameter to .send() (Ben Noordhuis) [#2620](https://github.com/nodejs/node/pull/2620)
* [[`c60857a81a`](https://github.com/nodejs/node/commit/c60857a81a)] - **cluster**: allow shared reused dgram sockets (Fedor Indutny) [#2548](https://github.com/nodejs/node/pull/2548)
* [[`b2ecbb6191`](https://github.com/nodejs/node/commit/b2ecbb6191)] - **contextify**: ignore getters during initialization (Fedor Indutny) [#2091](https://github.com/nodejs/node/pull/2091)
* [[`3711934095`](https://github.com/nodejs/node/commit/3711934095)] - **cpplint**: make it possible to run outside git repo (Ben Noordhuis) [#2710](https://github.com/nodejs/node/pull/2710)
* [[`03f900ab25`](https://github.com/nodejs/node/commit/03f900ab25)] - **crypto**: replace rwlocks with simple mutexes (Ben Noordhuis) [#2723](https://github.com/nodejs/node/pull/2723)
* [[`847459c29b`](https://github.com/nodejs/node/commit/847459c29b)] - **(SEMVER-MAJOR)** **crypto**: show exponent in decimal and hex (Chad Johnston) [#2320](https://github.com/nodejs/node/pull/2320)
* [[`e1c976184d`](https://github.com/nodejs/node/commit/e1c976184d)] - **deps**: improve ArrayBuffer performance in v8 (Fedor Indutny) [#2732](https://github.com/nodejs/node/pull/2732)
* [[`cc0ab17a23`](https://github.com/nodejs/node/commit/cc0ab17a23)] - **deps**: float node-gyp v3.0.0 (Rod Vagg) [#2700](https://github.com/nodejs/node/pull/2700)
* [[`b2c3c6d727`](https://github.com/nodejs/node/commit/b2c3c6d727)] - **deps**: create .npmrc during npm tests (Kat Marchán) [#2696](https://github.com/nodejs/node/pull/2696)
* [[`babdbfdbd5`](https://github.com/nodejs/node/commit/babdbfdbd5)] - **deps**: upgrade to npm 2.14.2 (Kat Marchán) [#2696](https://github.com/nodejs/node/pull/2696)
* [[`155783d876`](https://github.com/nodejs/node/commit/155783d876)] - **deps**: backport 75e43a6 from v8 upstream (again) (saper) [#2692](https://github.com/nodejs/node/pull/2692)
* [[`5424d6fcf0`](https://github.com/nodejs/node/commit/5424d6fcf0)] - **deps**: upgrade V8 to 4.5.103.30 (Ali Ijaz Sheikh) [#2632](https://github.com/nodejs/node/pull/2632)
* [[`c43172578e`](https://github.com/nodejs/node/commit/c43172578e)] - **(SEMVER-MAJOR)** **deps**: upgrade V8 to 4.5.103.24 (Ali Ijaz Sheikh) [#2509](https://github.com/nodejs/node/pull/2509)
* [[`714e96e8b9`](https://github.com/nodejs/node/commit/714e96e8b9)] - **deps**: backport 75e43a6 from v8 upstream (saper) [#2636](https://github.com/nodejs/node/pull/2636)
* [[`8637755cbf`](https://github.com/nodejs/node/commit/8637755cbf)] - **doc**: add TSC meeting minutes 2015-09-02 (Rod Vagg) [#2674](https://github.com/nodejs/node/pull/2674)
* [[`d3d5b93214`](https://github.com/nodejs/node/commit/d3d5b93214)] - **doc**: update environment vars in manpage and --help (Roman Reiss) [#2690](https://github.com/nodejs/node/pull/2690)
* [[`29f586ac0a`](https://github.com/nodejs/node/commit/29f586ac0a)] - **doc**: update url doc to account for escaping (Jeremiah Senkpiel) [#2605](https://github.com/nodejs/node/pull/2605)
* [[`ba50cfebef`](https://github.com/nodejs/node/commit/ba50cfebef)] - **doc**: reorder collaborators by their usernames (Johan Bergström) [#2322](https://github.com/nodejs/node/pull/2322)
* [[`8a9a3bf798`](https://github.com/nodejs/node/commit/8a9a3bf798)] - **doc**: update changelog for io.js v3.3.0 (Rod Vagg) [#2653](https://github.com/nodejs/node/pull/2653)
* [[`6cd0e2664b`](https://github.com/nodejs/node/commit/6cd0e2664b)] - **doc**: update io.js reference (Ben Noordhuis) [#2580](https://github.com/nodejs/node/pull/2580)
* [[`f9539c19e8`](https://github.com/nodejs/node/commit/f9539c19e8)] - **doc**: update changelog for io.js v3.2.0 (Rod Vagg) [#2512](https://github.com/nodejs/node/pull/2512)
* [[`cded6e7993`](https://github.com/nodejs/node/commit/cded6e7993)] - **doc**: fix CHANGELOG.md on master (Roman Reiss) [#2513](https://github.com/nodejs/node/pull/2513)
* [[`93e2830686`](https://github.com/nodejs/node/commit/93e2830686)] - **(SEMVER-MINOR)** **doc**: document deprecation of util.is* functions (Sakthipriyan Vairamani) [#2447](https://github.com/nodejs/node/pull/2447)
* [[`7038388558`](https://github.com/nodejs/node/commit/7038388558)] - **doc,test**: enable recursive file watching in Windows (Sakthipriyan Vairamani) [#2649](https://github.com/nodejs/node/pull/2649)
* [[`f3696f64a1`](https://github.com/nodejs/node/commit/f3696f64a1)] - **events,lib**: don't require EE#listenerCount() (Jeremiah Senkpiel) [#2661](https://github.com/nodejs/node/pull/2661)
* [[`45a2046f5d`](https://github.com/nodejs/node/commit/45a2046f5d)] - **(SEMVER-MAJOR)** **installer**: fix installers for node.js rename (Frederic Hemberger) [#2367](https://github.com/nodejs/node/pull/2367)
* [[`7a999a1376`](https://github.com/nodejs/node/commit/7a999a1376)] - **(SEMVER-MAJOR)** **lib**: add net.Socket#localFamily property (Ben Noordhuis) [#956](https://github.com/nodejs/node/pull/956)
* [[`de88255b0f`](https://github.com/nodejs/node/commit/de88255b0f)] - ***Revert*** "**lib,src**: add unix socket getsockname/getpeername" (Ben Noordhuis) [#2584](https://github.com/nodejs/node/pull/2584)
* [[`f337595441`](https://github.com/nodejs/node/commit/f337595441)] - **(SEMVER-MAJOR)** **lib,src**: add unix socket getsockname/getpeername (Ben Noordhuis) [#956](https://github.com/nodejs/node/pull/956)
* [[`3b602527d1`](https://github.com/nodejs/node/commit/3b602527d1)] - **(SEMVER-MAJOR)** **node**: additional cleanup for node rename (cjihrig) [#2367](https://github.com/nodejs/node/pull/2367)
* [[`a69ab27ab4`](https://github.com/nodejs/node/commit/a69ab27ab4)] - **(SEMVER-MAJOR)** **node**: rename from io.js to node (cjihrig) [#2367](https://github.com/nodejs/node/pull/2367)
* [[`9358eee9dd`](https://github.com/nodejs/node/commit/9358eee9dd)] - **node-gyp**: float 3.0.1, minor fix for download url (Rod Vagg) [#2737](https://github.com/nodejs/node/pull/2737)
* [[`d2d981252b`](https://github.com/nodejs/node/commit/d2d981252b)] - **src**: s/ia32/x86 for process.release.libUrl for win (Rod Vagg) [#2699](https://github.com/nodejs/node/pull/2699)
* [[`eba3d3dccd`](https://github.com/nodejs/node/commit/eba3d3dccd)] - **src**: use standard conform snprintf on windows (Karl Skomski) [#2404](https://github.com/nodejs/node/pull/2404)
* [[`cddbec231f`](https://github.com/nodejs/node/commit/cddbec231f)] - **src**: fix buffer overflow for long exception lines (Karl Skomski) [#2404](https://github.com/nodejs/node/pull/2404)
* [[`dd3f3417c7`](https://github.com/nodejs/node/commit/dd3f3417c7)] - **src**: re-enable fast math on arm (Michaël Zasso) [#2592](https://github.com/nodejs/node/pull/2592)
* [[`e137c1177c`](https://github.com/nodejs/node/commit/e137c1177c)] - **(SEMVER-MAJOR)** **src**: enable vector ics on arm again (Ali Ijaz Sheikh) [#2509](https://github.com/nodejs/node/pull/2509)
* [[`7ce749d722`](https://github.com/nodejs/node/commit/7ce749d722)] - **src**: replace usage of v8::Handle with v8::Local (Michaël Zasso) [#2202](https://github.com/nodejs/node/pull/2202)
* [[`b1a2d9509f`](https://github.com/nodejs/node/commit/b1a2d9509f)] - **src**: enable v8 deprecation warnings and fix them (Ben Noordhuis) [#2091](https://github.com/nodejs/node/pull/2091)
* [[`808de0da03`](https://github.com/nodejs/node/commit/808de0da03)] - **(SEMVER-MAJOR)** **src**: apply debug force load fixups from 41e63fb (Ali Ijaz Sheikh) [#2509](https://github.com/nodejs/node/pull/2509)
* [[`5201cb0ff1`](https://github.com/nodejs/node/commit/5201cb0ff1)] - **src**: fix memory leak in ExternString (Karl Skomski) [#2402](https://github.com/nodejs/node/pull/2402)
* [[`2308a27c0a`](https://github.com/nodejs/node/commit/2308a27c0a)] - **src**: only set v8 flags if argc > 1 (Evan Lucas) [#2646](https://github.com/nodejs/node/pull/2646)
* [[`384effed20`](https://github.com/nodejs/node/commit/384effed20)] - **test**: fix use of `common` before required (Rod Vagg) [#2685](https://github.com/nodejs/node/pull/2685)
* [[`f146f686b7`](https://github.com/nodejs/node/commit/f146f686b7)] - **(SEMVER-MAJOR)** **test**: fix test-repl-tab-complete.js for V8 4.5 (Ali Ijaz Sheikh) [#2509](https://github.com/nodejs/node/pull/2509)
* [[`fe4b309fd3`](https://github.com/nodejs/node/commit/fe4b309fd3)] - **test**: refactor to eliminate flaky test (Rich Trott) [#2609](https://github.com/nodejs/node/pull/2609)
* [[`619721e6b8`](https://github.com/nodejs/node/commit/619721e6b8)] - **test**: mark eval_messages as flaky (Alexis Campailla) [#2648](https://github.com/nodejs/node/pull/2648)
* [[`93ba585b66`](https://github.com/nodejs/node/commit/93ba585b66)] - **test**: mark test-vm-syntax-error-stderr as flaky (João Reis) [#2662](https://github.com/nodejs/node/pull/2662)
* [[`367140bca0`](https://github.com/nodejs/node/commit/367140bca0)] - **test**: mark test-repl-persistent-history as flaky (João Reis) [#2659](https://github.com/nodejs/node/pull/2659)
* [[`f6b093343d`](https://github.com/nodejs/node/commit/f6b093343d)] - **timers**: minor `_unrefActive` fixes and improvements (Jeremiah Senkpiel) [#2540](https://github.com/nodejs/node/pull/2540)
* [[`403d7ee7d1`](https://github.com/nodejs/node/commit/403d7ee7d1)] - **timers**: don't mutate unref list while iterating it (Julien Gilli) [#2540](https://github.com/nodejs/node/pull/2540)
* [[`7a8c3e08c3`](https://github.com/nodejs/node/commit/7a8c3e08c3)] - **timers**: Avoid linear scan in `_unrefActive`. (Julien Gilli) [#2540](https://github.com/nodejs/node/pull/2540)
* [[`b630ebaf43`](https://github.com/nodejs/node/commit/b630ebaf43)] - **win,msi**: Upgrade from old upgrade code (João Reis) [#2439](https://github.com/nodejs/node/pull/2439)
