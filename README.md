<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts after **repository update** is done succesfully.
- Nightly images are build once per day, at 5:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a href=""><b>Board name</b></a></td><td align="left"><b>Started</b></td><td align=right><b>Kernel version</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td></tr><tr><td align="left"><a href="https://paste.armbian.com/huherefuse">Orange Pi Win</a></td><td align="left">2023-08-19&nbsp;19:10:35</td><td align=right>6.1.45-current-sunxi64</td><td align=right>881</td><td align=right>2880</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qajiqakide">Orange Pi Win</a></td><td align="left">2023-08-19&nbsp;19:22:32</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>783</td><td align=right>2856</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-19&nbsp;19:01:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-19&nbsp;19:01:37</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/obuteyawik">Espressobin</a></td><td align="left">2023-08-19&nbsp;19:20:08</td><td align=right>5.15.127-current-mvebu64</td><td align=right>633</td><td align=right>1025</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ozobadoboq">Espressobin</a></td><td align="left">2023-08-19&nbsp;19:38:12</td><td align=right>6.1.46-edge-mvebu64</td><td align=right>840</td><td align=right>1046</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ocodavayok">Pine H64</a></td><td align="left">2023-08-19&nbsp;19:07:49</td><td align=right>6.1.45-current-sunxi64</td><td align=right>929</td><td align=right>3784</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sinilojipe">Pine H64</a></td><td align="left">2023-08-19&nbsp;19:16:11</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>875</td><td align=right>3634</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">UEFI x86</a></td><td align="left">2023-08-19&nbsp;19:17:25</td><td align=right>5.15.127-legacy-x86</td><td align=right>830</td><td align=right>4746</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">UEFI x86</a></td><td align="left">2023-08-19&nbsp;19:24:47</td><td align=right>6.1.46-current-x86</td><td align=right>873</td><td align=right>4553</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">UEFI x86</a></td><td align="left">2023-08-19&nbsp;19:32:42</td><td align=right>6.4.11-edge-x86</td><td align=right>548</td><td align=right>4507</td></tr><tr><td align="left"><a href="https://paste.armbian.com/kisewexaze">RockPro 64</a></td><td align="left">2023-08-19&nbsp;19:08:43</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6540</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nuhinalugi">RockPro 64</a></td><td align="left">2023-08-19&nbsp;19:15:20</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>834</td><td align=right>6402</td></tr><tr><td align="left"><a href="https://paste.armbian.com/hakefemoga">Rockpi E</a></td><td align="left">2023-08-19&nbsp;19:11:33</td><td align=right>6.1.46-current-rockchip64</td><td align=right>90</td><td align=right>3343</td></tr><tr><td align="left"><a href="https://paste.armbian.com/napijawuhu">Rockpi E</a></td><td align="left">2023-08-19&nbsp;19:25:07</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>89</td><td align=right>3232</td></tr><tr><td align="left"><a href="https://paste.armbian.com/evekocenus">Odroid C2</a></td><td align="left">2023-08-19&nbsp;19:09:16</td><td align=right>6.1.46-current-meson64</td><td align=right>882</td><td align=right>3927</td></tr><tr><td align="left"><a href="https://paste.armbian.com/emivecawal">Odroid C2</a></td><td align="left">2023-08-19&nbsp;19:18:04</td><td align=right>6.4.11-edge-meson64</td><td align=right>640</td><td align=right>4029</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ubirikisem">NanoPi R6S</a></td><td align="left">2023-08-19&nbsp;19:01:07</td><td align=right>5.10.160-legacy-rk35xx</td><td align=right>2250</td><td align=right>15819</td></tr><tr><td align="left"><a href="https://paste.armbian.com/yodokevawu">Orange Pi 3 LTS</a></td><td align="left">2023-08-19&nbsp;19:06:36</td><td align=right>6.1.45-current-sunxi64</td><td align=right>916</td><td align=right>3884</td></tr><tr><td align="left"><a href="https://paste.armbian.com/feresosono">Orange Pi 3 LTS</a></td><td align="left">2023-08-19&nbsp;19:15:41</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>912</td><td align=right>3837</td></tr><tr><td align="left"><a href="https://paste.armbian.com/agedewicex">Odroid C4</a></td><td align="left">2023-08-19&nbsp;19:06:04</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>5633</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iwowuhesiw">Odroid C4</a></td><td align="left">2023-08-19&nbsp;19:12:59</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>5657</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qugiyajidu">Rockpi 4B</a></td><td align="left">2023-08-19&nbsp;19:04:35</td><td align=right>6.1.46-current-rockchip64</td><td align=right>781</td><td align=right>6442</td></tr><tr><td align="left"><a href="https://paste.armbian.com/enegixuquj">Rockpi 4B</a></td><td align="left">2023-08-19&nbsp;19:11:54</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>6125</td></tr><tr><td align="left"><a href="https://paste.armbian.com/tovameyobi">NanoPi M4</a></td><td align="left">2023-08-19&nbsp;19:04:18</td><td align=right>6.1.46-current-rockchip64</td><td align=right>970</td><td align=right>6660</td></tr><tr><td align="left"><a href="https://paste.armbian.com/gebeqivozu">NanoPi M4</a></td><td align="left">2023-08-19&nbsp;19:11:33</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>6699</td></tr><tr><td align="left"><a href="https://paste.armbian.com/owituyarek">Banana Pi Pro</a></td><td align="left">2023-08-19&nbsp;19:11:48</td><td align=right>6.1.45-current-sunxi</td><td align=right>410</td><td align=right>1015</td></tr><tr><td align="left"><a href="https://paste.armbian.com/yazorezela">Banana Pi Pro</a></td><td align="left">2023-08-19&nbsp;19:25:58</td><td align=right>6.4.10-edge-sunxi</td><td align=right>351</td><td align=right>1014</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wexuhejoqa">ZeroPi</a></td><td align="left">2023-08-19&nbsp;19:16:17</td><td align=right>5.15.126-legacy-sunxi</td><td align=right>536</td><td align=right>2642</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bucawotazo">ZeroPi</a></td><td align="left">2023-08-19&nbsp;19:26:13</td><td align=right>6.1.45-current-sunxi</td><td align=right>608</td><td align=right>2663</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nutasewitu">ZeroPi</a></td><td align="left">2023-08-19&nbsp;19:36:28</td><td align=right>6.4.10-edge-sunxi</td><td align=right>519</td><td align=right>2639</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uhikomojuv">Cubietruck</a></td><td align="left">2023-08-19&nbsp;19:26:29</td><td align=right>6.1.45-current-sunxi</td><td align=right>353</td><td align=right>986</td></tr><tr><td align="left"><a href="https://paste.armbian.com/amarejufid">Cubietruck</a></td><td align="left">2023-08-19&nbsp;19:43:55</td><td align=right>6.4.10-edge-sunxi</td><td align=right>319</td><td align=right>987</td></tr><tr><td align="left"><a href="https://paste.armbian.com/hemomaniri">NanoPi R4S</a></td><td align="left">2023-08-19&nbsp;19:05:49</td><td align=right>6.1.46-current-rockchip64</td><td align=right>910</td><td align=right>6399</td></tr><tr><td align="left"><a href="https://paste.armbian.com/puvavuceti">NanoPi R4S</a></td><td align="left">2023-08-19&nbsp;19:12:59</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>6476</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zekocotalo">Odroid N2</a></td><td align="left">2023-08-19&nbsp;19:02:15</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>8853</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wefenakuka">Odroid N2</a></td><td align="left">2023-08-19&nbsp;19:07:21</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>8859</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ifuwozolad">Orange Pi 3</a></td><td align="left">2023-08-19&nbsp;19:04:35</td><td align=right>6.1.45-current-sunxi64</td><td align=right>954</td><td align=right>4215</td></tr><tr><td align="left"><a href="https://paste.armbian.com/etahivowek">Orange Pi 3</a></td><td align="left">2023-08-19&nbsp;19:11:57</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>872</td><td align=right>3924</td></tr><tr><td align="left"><a href="https://paste.armbian.com/fuvefubibi">NanoPi Neo 3</a></td><td align="left">2023-08-19&nbsp;19:05:44</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>3461</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ucogacihiq">NanoPi Neo 3</a></td><td align="left">2023-08-19&nbsp;19:14:49</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>2670</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jafuhufoxu">Orange Pi Zero</a></td><td align="left">2023-08-19&nbsp;19:15:32</td><td align=right>5.15.126-legacy-sunxi</td><td align=right>90</td><td align=right>2082</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ehiconociv">Orange Pi Zero</a></td><td align="left">2023-08-19&nbsp;19:26:20</td><td align=right>6.1.45-current-sunxi</td><td align=right>91</td><td align=right>2112</td></tr><tr><td align="left"><a href="https://paste.armbian.com/seyelutese">Orange Pi Zero</a></td><td align="left">2023-08-19&nbsp;19:37:18</td><td align=right>6.4.10-edge-sunxi</td><td align=right>90</td><td align=right>1991</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jimupibijo">Orange Pi Zero Plus</a></td><td align="left">2023-08-19&nbsp;19:12:25</td><td align=right>6.1.45-current-sunxi64</td><td align=right>842</td><td align=right>2520</td></tr><tr><td align="left"><a href="https://paste.armbian.com/irikezixev">Orange Pi Zero Plus</a></td><td align="left">2023-08-19&nbsp;19:23:06</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>784</td><td align=right>2501</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nodedopema">Orange Pi Zero2</a></td><td align="left">2023-08-19&nbsp;19:10:50</td><td align=right>6.1.45-current-sunxi64</td><td align=right>833</td><td align=right>2689</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ujetapibem">Orange Pi Zero2</a></td><td align="left">2023-08-19&nbsp;19:22:56</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>826</td><td align=right>2540</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-19&nbsp;19:08:06</td><td align=right>6.1.46-current-mvebu</td><td align=right>750</td><td align=right>2177</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-19&nbsp;19:14:43</td><td align=right>6.2.16-edge-mvebu</td><td align=right>882</td><td align=right>2188</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qaqepovupo">ODROID M1</a></td><td align="left">2023-08-19&nbsp;19:07:25</td><td align=right>6.3.13-edge-rk3568-odroid</td><td align=right>890</td><td align=right>5312</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eraresemas">Tinker Board 2</a></td><td align="left">2023-08-19&nbsp;19:16:06</td><td align=right>6.1.46-current-rockchip64</td><td align=right>901</td><td align=right>6864</td></tr><tr><td align="left"><a href="https://paste.armbian.com/anumurutez">Tinker Board 2</a></td><td align="left">2023-08-19&nbsp;19:23:05</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>731</td><td align=right>6741</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jofejituye">Orange Pi 4 LTS</a></td><td align="left">2023-08-19&nbsp;19:05:41</td><td align=right>6.1.46-current-rockchip64</td><td align=right>900</td><td align=right>5325</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vuxazuboni">Orange Pi 4 LTS</a></td><td align="left">2023-08-19&nbsp;19:13:19</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>898</td><td align=right>4838</td></tr><tr><td align="left"><a href="https://paste.armbian.com/arihuyayex">Le potato</a></td><td align="left">2023-08-19&nbsp;19:11:42</td><td align=right>6.1.46-current-meson64</td><td align=right>93</td><td align=right>3713</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ekusuyugav">Le potato</a></td><td align="left">2023-08-19&nbsp;19:22:56</td><td align=right>6.4.11-edge-meson64</td><td align=right>88</td><td align=right>3740</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-19&nbsp;18:57:13</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uturoruyog">Banana Pi CM4IO</a></td><td align="left">2023-08-19&nbsp;19:01:17</td><td align=right>6.1.46-current-meson64</td><td align=right>880</td><td align=right>8837</td></tr><tr><td align="left"><a href="https://paste.armbian.com/dimedahosi">Banana Pi CM4IO</a></td><td align="left">2023-08-19&nbsp;19:05:20</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>8451</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oyopicosoz">Banana Pi M5</a></td><td align="left">2023-08-19&nbsp;19:02:58</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>5602</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bucifejewi">Banana Pi M5</a></td><td align="left">2023-08-19&nbsp;19:08:38</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>5566</td></tr><tr><td align="left"><a href="https://paste.armbian.com/imotutuxaz">Khadas VIM2</a></td><td align="left">2023-08-19&nbsp;19:08:11</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>6096</td></tr><tr><td align="left"><a href="https://paste.armbian.com/cucomobequ">Khadas VIM2</a></td><td align="left">2023-08-19&nbsp;19:19:07</td><td align=right>6.4.11-edge-meson64</td><td align=right>600</td><td align=right>6065</td></tr><tr><td align="left"><a href="https://paste.armbian.com/rusamowoco">Khadas VIM1</a></td><td align="left">2023-08-19&nbsp;19:06:33</td><td align=right>6.1.46-current-meson64</td><td align=right>93</td><td align=right>3679</td></tr><tr><td align="left"><a href="https://paste.armbian.com/fotificowa">Khadas VIM1</a></td><td align="left">2023-08-19&nbsp;19:15:56</td><td align=right>6.4.11-edge-meson64</td><td align=right>90</td><td align=right>3724</td></tr><tr><td align="left"><a href="https://paste.armbian.com/posituqixa">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-19&nbsp;19:14:32</td><td align=right>6.1.46-current-rockchip64</td><td align=right>694</td><td align=right>1892</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wadivizupe">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-19&nbsp;19:28:39</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>470</td><td align=right>1790</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-19&nbsp;18:57:52</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zikorecake">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-19&nbsp;19:16:01</td><td align=right>6.1.45-current-sunxi</td><td align=right>27</td><td align=right>2564</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nexacugere">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-19&nbsp;19:27:49</td><td align=right>6.4.10-edge-sunxi</td><td align=right>31</td><td align=right>2472</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
