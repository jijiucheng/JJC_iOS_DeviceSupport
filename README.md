- [JJC_iOS_DeviceSupport](#JJC_iOS_DeviceSupport)
  - [DeviceSupport Path](#DeviceSupport-Path)
  - [Release Notes](#release-notes)
  - [Others DeviceSupport Link](#Others-DeviceSupport-Link)
  - [Support Version](#Support-Version)



# JJC_iOS_DeviceSupport
This repository is the device support files for Xcode building the iOS App.


### DeviceSupport Path

```
/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport
```

### Release Notes

- [【重点】本项目特殊版本说明](/Release%20Notes.md)
- `RC` 版本是指 `Release Candidate` 正式版本的 `候选版本`，基本上不出意外，正式版本就是该版本。
- [Xcode Release Notes](https://developer.apple.com/documentation/xcode-release-notes)
- [iOS & iPadOS Release Notes](https://developer.apple.com/documentation/ios-ipados-release-notes)
- [Issues - Please DeviceSuport version 14.7? #160](https://github.com/iGhibli/iOS-DeviceSupport/issues/160)
- 
- **`2023.11.15 更新：`**
  - 经测试发现，`Xcode 14.x` 的版本实际上应该无法运行 `iOS 17.x` 系列的版本，必须升级到 `Xcode 15.x` 才可以，且 `macOS` 系统需要升级为 `macOS Sonoma` 才可以运行 `Xcode 15.x`；
  - 另外一点就是，一旦升级到了 `macOS Sonoma` 版本的系统后，`Xcode 14.x` 将无法运行，不再像以前一样可以运行低版本的 `Xcode` 版本，请谨慎升级。
 
### Others DeviceSupport Link

- [Github - iGhibli / iOS-DeviceSupport](https://github.com/iGhibli/iOS-DeviceSupport)
- [Github - filsv / iPhoneOSDeviceSupport](https://github.com/filsv/iPhoneOSDeviceSupport)
- [Gitee - 邱邱邱同学 / iOSDeviceSupport](https://gitee.com/qiu1993/iOSDeviceSupport)
- [Gitee - ios_shen / iOSDeviceSupport](https://gitee.com/ios_shen/iOSDeviceSupport)

### Libarclite

- `Xcode 15` 在某些 `CocoaPods` 中存在构建问题，因为其 `XcodeDefaults` 工具链内容中缺少 `.a` 文件。
- 常见报错信息如下：`SDK does not contain 'libarclite' at the path '/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/arc/libarclite_iphoneos.a'; try increasing the minimum deployment target`
- **解决办法：**
  - 1、将缺失文件拷贝放入 `/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/arc/` 文件夹下；
  - 2、如果没有该文件就手动创建该文件即可；
  - 3、缺少哪种文件就将哪种文件放入该文件夹即可，建议将 `libarclite_iphonesimulator.a` 和 `libarclite_iphoneos.a` 两个文件优先放入其中，毕竟是最常用的。

### Support Version

| Version | Xcode | Release Time | Beta Time |
| :---: | :---: | :------ | :------ |
| 17.5 | Xcode_15.4<br>Xcode_15.3 | ... | iOS17.5_beta（21F5048f）<br>`2024/04/02` |
| 17.4.1<br>17.4 | Xcode_15.3 | Xcode_15.3（15E204a）<br>`2024/03/05`<br><br>iOS17.4.1（21E236）<br>`2024/03/21`<br>iOS17.4（21E219）<br>`2024/03/05` | Xcode_15.3_RC（15E5202a）<br>`2024/02/27`<br>Xcode_15.3_beta3（15E5194e）<br>`2024/02/13`<br>Xcode_15.3_beta2（15E5188j）<br>`2024/02/06`<br>Xcode_15.3_beta（15E5178i）<br>`2024/01/25`<br><br>iOS17.4_RC（21E217）<br>`2024/02/27`<br>iOS17.4_beta4（21E5209b）<br>`2024/02/20`<br>iOS17.4_beta3（21E5200d）<br>`2024/02/13`<br>iOS17.4_beta2（21E5195e）<br>`2024/02/06`<br>iOS17.4_beta_v2（21E5184k）<br>`2024/01/30`<br>iOS17.4_beta（21E5184i）<br>`2024/01/25` |
| 17.3.1<br>17.3 | Xcode_15.3<br>Xcode_15.2 | Xcode_15.2（15C500b）<br>`2024/01/08`<br><br>iOS17.3.1（21D61）<br>`2024/02/08`<br>iOS17.3（21D50）<br>`2024/01/22` | Xcode_15.2_beta（15C5500c）<br>`2023/12/12`<br><br>iOS17.3_RC（21D50）<br>`2024/01/17`<br>iOS17.3_beta3（21D5044a）<br>`2024/01/09`<br>iOS17.3_beta2（21D5036c）<br>`2024/01/03`<br>iOS17.3_beta（21D5026f）<br>`2023/12/12` |
| [17.2.1<br>17.2](/Release%20Notes.md#ios172--ios1721) | Xcode_15.1 | Xcode_15.1（15C65）<br>`2023/12/11`<br><br>iOS17.2.1（21C66）<br>`2023/12/19`<br>iOS17.2（21C62）<br>`2023/12/11` | Xcode_15.1_RC（15C65）<br>`2023/12/05`<br>Xcode_15.1_beta3（15C5059c）<br>`2023/11/14`<br>Xcode_15.1_beta2（15C5042i）<br>`2023/10/26`<br><br>iOS17.2_RC（21C62）<br>`2023/12/05`<br>iOS17.2_beta4（21C5054b）<br>`2023/11/28`<br>iOS17.2_beta3（21C5046c）<br>`2023/11/14`<br>iOS17.2_beta2（21C5040g）<br>`2023/11/09`<br>iOS17.2_beta（21C5029g）<br>`2023/10/26` |
| [17.1.2<br>17.1.1<br>17.1](/Release%20Notes.md#ios171--ios1712) | Xcode_15.1<br>Xcode_15.0.1<br>Xcode_15 | Xcode_15.0.1（15A507）<br>`2023/10/18`<br>Xcode_15（15A240d）<br>`2023/09/18`<br><br>iOS17.1.2（21B101）<br>`2023/11/30`<br>iOS17.1.1（21B91）<br>`2023/11/07`<br>iOS17.1（21B74、21B80）<br>`2023/10/25`<br>iPadOS17.1（21B74）<br>`2023/10/25` | Xcode_15.1_beta2（15C5042i）<br>`2023/10/26`<br>Xcode_15.1_beta（15C5028h）<br>`2023/10/03`<br>Xcode_15.0.1_RC（15A507）<br>`2023/10/11`<br><br>iOS17.1_RC2（21B77）<br>`2023/10/20`<br>iOS17.1_RC（21B74）<br>`2023/10/17`<br>iOS17.1_beta3（21B5066a）<br>`2023/10/10`<br>iOS17.1_beta2（21B5056e）<br>`2023/10/03`<br>iOS17.1_beta（21B5045h）<br>`2023/09/28` |
| [17.0.3<br>17.0.2<br>17.0.1<br>17](/Release%20Notes.md#ios17--ios1703) | Xcode_15.1<br>Xcode_15.0.1<br>Xcode_15 | Xcode_15.0.1（15A507）<br>`2023/10/18`<br>Xcode_15（15A240d）<br>`2023/09/18`<br><br>iOS17.0.3（21A360）<br>`2023/10/03`<br>iOS17.0.2（21A350）<br>`2023/09/22`<br>iOS17.0.1（21A340）<br>`2023/09/21`<br>iOS17（21A329）<br>`2023/09/18` | Xcode_15.1_beta（15C5028h）<br>`2023/10/03`<br>Xcode_15.0.1_RC（15A507）<br>`2023/10/11`<br>Xcode_15_RC（15A240d）<br>`2023/09/12`<br>Xcode_15_beta8（15A5229m）<br>`2023/08/29`<br>Xcode_15_beta7（15A5229h）<br>`2023/08/22`<br>Xcode_15_beta6（15A5219j）<br>`2023/08/08`<br>Xcode_15_beta5（15A5209g）<br>`2023/07/25`<br>Xcode_15_beta4（15A5195m）<br>`2023/07/11`<br>Xcode_15_beta3（15A5195k）<br>`2023/07/05`<br>Xcode_15_beta2（15A5161b）<br>`2023/06/21`<br>Xcode_15_beta（15A5160n）<br>`2023/06/05`<br><br>iOS17_RC（21A329）<br>`2023/09/12`<br>iOS17_beta8（21A5326a）<br>`2023/08/29`<br>iOS17_beta7（21A5319a）<br>`2023/08/22`<br>iOS17_beta6（21A5312c）<br>`2023/08/15`<br>iOS17_beta5（21A5303d）<br>`2023/08/08`<br>iOS17_beta4_v2（21A5291j）<br>`2023/07/31`<br>iOS17_beta4（21A5291h）<br>`2023/07/25`<br>iOS17_beta3_v2（21A5277j）<br>`2023/07/11`<br>iOS17_beta3（21A5277h）<br>`2023/07/05`<br>iOS17_beta2（21A5268h）<br>`2023/06/21`<br>iOS17_beta（21A5248v）<br>`2023/06/05` |
| [16.7.7<br>6.7.6<br>16.7.5<br>16.7.4<br>16.7.3<br>16.7.2<br>16.7.1<br>16.7](/Release%20Notes.md#ios167--ios1675) | Xcode_15.3<br>Xcode_15.2<br>Xcode_15.1<br>Xcode_15.0.1<br>Xcode_15 | Xcode_15.3（15E204a）<br>`2024/03/05`<br>Xcode_15.2（15C500b）<br>`2024/01/08`<br>Xcode_15.1（15C65）<br>`2023/12/11`<br>Xcode_15.0.1（15A507）<br>`2023/10/18`<br>Xcode_15（15A240d）<br>`2023/09/18`<br><br>iOS16.7.7（20H330）<br>`2024/03/21`<br>iOS16.7.6（20H320）<br>`2024/03/05`<br>iOS16.7.5（20H307）<br>`2024/01/22`<br>iOS16.7.4（20H240）<br>`2023/12/20`<br>iOS16.7.3（20H232）<br>`2023/12/11`<br>iOS16.7.2（20H115）<br>`2023/10/25`<br>iOS16.7.1（20H30）<br>`2023/10/10`<br>iOS16.7（20H19）<br>`2023/09/21` | Xcode_15.1_beta（15C5028h）<br>`2023/10/03`<br>Xcode_15.0.1_RC（15A507）<br>`2023/10/11`<br>Xcode_15_RC（15A240d）<br>`2023/09/12`<br><br>iOS16.7.6_RC（20H320）<br>`2024/02/27`<br>iOS16.7.5_RC（20H307）<br>`2024/01/17`<br>iOS16.7.3_RC（20H232）<br>`2023/12/05`<br>iOS16.7.2_RC（20H115）<br>`2023/10/17`<br>iOS16.7_RC（20H18）<br>`2023/09/12` |
| [16.6.1<br>16.6](/Release%20Notes.md#ios166--ios1661) | Xcode_15<br>Xcode_14.3.1<br>Xcode_14.3 | Xcode_15（15A240d）<br>`2023/09/18`<br>Xcode_14.3.1（14E300c）<br>`2023/06/01`<br>Xcode_14.3（14E222b）<br>`2023/03/30`<br><br>iOS16.6.1（20G81）<br>`2023/09/07`<br>iOS16.6（20G75）<br>`2023/07/24` | Xcode_15_RC（15A240d）<br>`2023/09/12`<br>Xcode_15_beta8（15A5229m）<br>`2023/08/29`<br><br>iOS16.6_RC（20G75）<br>`2023/07/18`<br>iOS16.6_beta5（20G5070a）<br>`2023/07/10`<br>iOS16.6_beta4（20G5058d）<br>`2023/06/27`<br>iOS16.6_beta3（20G5047d）<br>`2023/06/15`<br>iOS16.6_beta2（20G5037d）<br>`2023/05/31`<br>iOS16.6_beta（20G5026e）<br>`2023/05/19` |
| [16.5.1<br>16.5](/Release%20Notes.md#ios165--ios1651) | Xcode_15<br>Xcode_14.3 | Xcode_14.3（14E222b）<br>`2023/03/30`<br><br>iOS16.5.1（20F75）<br>`2023/06/21`<br>iOS16.5（20F66）<br>`2023/05/18` | Xcode_15_beta2（15A5161b）<br>`2023/06/21`<br>Xcode_14.3.1_RC（14E300b）<br>`2023/05/17`<br><br>iOS16.5_RC2（20F66）<br>`2023/05/15`<br>iOS16.5_RC（20F65）<br>`2023/05/09`<br>iOS16.5_beta4（20F5059a）<br>`2023/05/02`<br>iOS16.5_beta3（20F5050f）<br>`2023/04/25`<br>iOS16.5_beta2（20F5039e）<br>`2023/04/11`<br>iOS16.5_beta（20F5028e）<br>`2023/03/28` |
| [16.4.1<br>16.4](/Release%20Notes.md#ios164--1641) | Xcode_14.3 | Xcode_14.3（14E222b）<br>`2023/03/30`<br><br>iOS16.4.1（20E252）<br>`2023/04/07`<br>iOS16.4（20E247）<br>`2023/03/27` | Xcode_14.3_RC2（14E222b）<br>`2023/03/27`<br>Xcode_14.3_RC（14E222a）<br>`2023/03/21`<br>Xcode14.3_beta3（14E5215g）<br>`2023/03/15`<br>Xcode14.3_beta2（14E5207e）<br>`2023/02/28`<br>Xcode14.3_beta（14E5197f）<br>`2023/02/16`<br><br>iOS16.4_RC（20E246）<br>`2023/03/21`<br>iOS16.4_beta4（20E5239b）<br>`2023/03/15`<br>iOS16.4_beta3（20E5229e）<br>`2023/03/07`<br>iOS16.4_beta2（20E5223e）<br>`2023/02/28`<br>iOS16.4_beta（20E5212f）<br>`2023/02/16` |
| [16.3.1<br>16.3](/Release%20Notes.md#ios163--ios1631) | Xcode_14.2 | iOS16.3.1（20D67）<br>`2023/02/13`<br>iOS16.3（20D47）<br>`2023/01/23` | iOS16.3_RC（20D47）<br>`2023/01/18`<br>iOS16.3_btea2（20D5035i）<br>`2023/01/10`<br>iOS16.3_btea（20D5024e）<br>`2022/12/14` |
| [16.2](/Release%20Notes.md#ios162) | Xcode_14.2<br>Xcode_14.1 | Xcode_14.2（14C18）<br>`2022/12/13`<br>Xcode_14.1（14B47b）<br>`2022/11/01`<br><br>iOS16.2（20C65）<br>`2022/12/13` | Xcode_14.2_RC（14C18）<br>`2022/12/07`<br>Xcode_14.1_RC2（14B47b）<br>`2022/10/24`<br><br>iOS16.2_RC（20C65）<br>`2022/12/07`<br>iOS16.2_beta4（20C5058d）<br>`2022/12/01`<br>iOS16.2_beta3（20C5049e）<br>`2022/11/15`<br>iOS16.2_beta2（20C5043e）<br>`2022/11/08`<br>iOS16.2_beta（20C5032e）<br>`2022/10/25` |
| [16.1.2<br>16.1.1](/Release%20Notes.md#ios1611--ios1612) | Xcode_14.1 | Xcode_14.1（14B47b）<br>`2022/11/01`<br><br>iOS16.1.2（20B110）<br>`2022/11/30`<br>iOS16.1.1（20B101）<br>`2022/11/09` | ... |
| 16.1 | Xcode_14.1 | Xcode_14.1（14B47b）<br>`2022/11/01`<br><br>iOS16.1（20B82）<br>`2022/10/24` | Xcode_14.1_RC2（14B47b）<br>`2022/10/24`<br>Xcode_14.1_RC（14B47）<br>`2022/10/18`<br>Xcode_14.1_beta3（14B5033e）<br>`2022/09/27`<br>Xcode_14.1_beta2（14B5024i）<br>`2022/09/20`<br>Xcode_14.1_beta（14B5024h）<br>`2022/09/14`<br><br>iOS16.1（20B82）<br>`2022/10/24`<br>iOS16.1_RC（20B79）<br>`2022/10/18`<br>iOS16.1_beta5（20B5072b）<br>`2022/10/11`<br>iOS16.1_beta4（20B5064c）<br>`2022/10/04`<br>iOS16.1_beta3（20B5056e）<br>`2022/09/27`<br>iOS16.1_beta2（20B5050f）<br>`2022/09/20`<br>iOS16.1_beta（20B5045d）<br>`2022/09/14` |
| [16.0.3<br>16.0.2<br>16.0.1](/Release%20Notes.md#ios1601--ios1603) | Xcode_14.0.1 | Xcode_14.0.1（14A400）<br>`2022/09/26`<br><br>iOS16.0.3（20A392）<br>`2022/10/10`<br>iOS16.0.2（20A380）<br>`2022/09/22`<br>iOS16.0.1（20A371）<br>`2022/09/16` | Xcode_14.0.1_RC（14A400）<br>`2022/09/16` |
| 16.0 | Xcode_14.0 | Xcode_14.0（14A309）<br>`2022/09/12`<br><br>iOS16.0（20A362）<br>`2022/09/12` | Xcode_14.0_RC（14A309）<br>`2022/09/07`<br>Xcode_14.0_beta6（14A5294g）<br>`2022/08/23`<br>Xcode_14.0_beta5（14A5294e）<br>`2022/08/08`<br>Xcode_14.0_beta4（14A5284g）<br>`2022/07/27`<br>Xcode_14.0_beta3（14A5270f）<br>`2022/07/06`<br>Xcode_14.0_beta2（14A5229c）<br>`2022/06/22`<br>Xcode_14.0_beta（14A5228q）<br>`2022/06/06` |
| [15.8.2<br>15.8.1<br>15.8](/Release%20Notes.md#ios1581--ios158) | Xcode_15.3<br>Xcode_15.2<br>Xcode_15.1<br>Xcode_15.0.1 | Xcode_15.3（15E204a）<br>`2024/03/05`<br>Xcode_15.2（15C500b）<br>`2024/01/08`<br>Xcode_15.0.1（15A507）<br>`2023/10/18`<br><br>iOS15.8.2（19H384）<br>`2024/03/05`<br>iOS15.8.1（19H380）<br>`2024/01/22`<br>iOS15.8（19H370）<br>`2023/10/25` | Xcode_15.1_beta（15C5028h）<br>`2023/10/03`<br><br>iOS15.8.2_RC（19H384）<br>`2024/02/27`<br>iOS15.8.1_RC（19H380）<br>`2024/01/17` |
| [15.7.9<br>15.7.8<br>15.7.7<br>15.7.6<br>15.7.5<br>15.7.4<br>15.7.3<br>15.7.2<br>15.7.1](/Release%20Notes.md#ios1571--ios1579) | Xcode_15<br>Xcode_14.3<br>Xcode_14.2<br>Xcode_14.1 | Xcode_14.3（14E222b）<br>`2023/03/30`<br>Xcode_14.2（14C18）<br>`2022/12/13`<br>Xcode_14.1（14B47b）<br>`2022/11/01`<br><br>iOS15.7.8（19H364）<br>`2023/07/24`<br>iOS15.7.7（19H357）<br>`2023/06/21`<br>iOS15.7.6（19H349）<br>`2023/05/18`<br>iOS15.7.6（19H349）<br>`2023/05/09`<br>iOS15.7.5（19H332）<br>`2023/04/10`<br>iOS15.7.4（19H321）<br>`2023/03/27`<br>iOS15.7.3（19H307）<br>`2023/01/23`<br>iOS15.7.2（19H218）<br>`2022/12/13`<br>iOS15.7.1（19H17）<br>`2022/10/27` | Xcode_15_beta8（15A5229m）<br>`2023/08/29`<br>Xcode_14.3_RC2（14E222b）<br>`2023/03/27`<br>Xcode_14.3_RC（14E222a）<br>`2023/03/21`<br>Xcode_14.2_RC（14C18）<br>`2022/12/07`<br>Xcode_14.1_RC2（14B47b）<br>`2022/10/24`<br>Xcode_14.1_RC（14B47）<br>`2022/10/18`<br><br>iOS15.7.8_RC（19H364）<br>`2023/07/18`<br>iOS15.7.4_RC（19H321）<br>`2023/03/21`<br>iOS15.7.3_RC（19H307）<br>`2023/01/18`<br>iOS15.7.2_RC（19H218）<br>`2022/12/07`<br>iOS15.7.1_RC（19H115）<br>`2022/10/18` |
| [15.7<br>15.6](/Release%20Notes.md#ios156--ios157) | Xcode_14.0<br>Xcode_13.4.1 | Xcode_14.0（14A309）<br>`2022/09/12`<br>Xcode_13.4.1（13F100）<br>`2022/06/02`<br><br>iOS15.7（19H12）<br>`2022/09/12` | ... |
| 15.5 | Xcode_13.4 | Xcode_13.4（13F17a）<br>`2022/05/16` | Xcode_13.4_RC（13F17a）<br>`2022/05/12` |
| 15.4 | Xcode_13.3.1 | Xcode_13.3.1（13E500A）<br>`2022/04/11` | ... |
| 15.4 | Xcode_13.3 | Xcode_13.3（13E113）<br>`2022/03/14` | Xcode_13.3_RC（13E113）<br>`2022/03/08`<br>Xcode_13.3_beta3（13E5104i）<br>`2022/02/22`<br>Xcode_13.3_beta2（13E5095k）<br>`2022/02/08`<br>Xcode_13.3_beta<br>`2022/01/27` |
| 15.3.x | Xcode_13.2.1 | Xcode_13.2.1（13C100）<br>`2021/12/17` | ... |
| 15.2 | Xcode_13.2 | Xcode_13.2<br>`2021/12/13` | Xcode_13.2_beta2<br>`2021/11/16`<br>Xcode_13.2_beta<br>`2021/10/27` |
| 15.1 | Xcode_13.1 | Xcode_13.1（19B74）<br>`2021/10/26` | ... |
| 15.0 | Xcode_13 | Xcode_13（13A233）<br>`2021/09/21` | Xcode_13_beta5<br>`2021/08/10`<br>Xcode_13_beta4<br>`2021/07/26`<br>Xcode_13_beta3<br>`2021/07/16`<br>Xcode_13_beta2<br>`2021/07/14`<br>Xcode_13_beta<br>`2021/06/07` |
| 14.6 ~ 14.7.x | Xcode_12.5.1 | Xcode_12.5.1（12E507）<br>`2021/06/20` | ... |
| 14.5 | Xcode_12.5 | Xcode_12.5<br>`2021/04/26` | Xcode_12.5_beta3<br>`2021/03/02`<br>Xcode_12.5_beta2<br>`2021/02/16`<br>Xcode_12.5_beta<br>`2021/02/01` |
| 14.4 | Xcode_12.4 | Xcode_12.4<br>`2021/01/27` | ... |
| 14.3 | Xcode_12.3 | Xcode_12.3<br>`2020/12/14` | Xcode_12.3_beta（12C5020F）<br>`2020/11/12`|
| 14.2 | Xcode_12.2 | Xcode_12.2<br>`2020/11/12` | Xcode_12.2_beta3<br>`2020/10/13`<br>Xcode_12.2_beta2<br>`2020/09/29`<br>Xcode_12.2_beta<br>`2020/09/17` |
| 14.1 | Xcode_12.1 | Xcode_12.1（12E507）<br>`2020/10/28` | ... |
| 14.0 | Xcode_12 | Xcode_12<br>`2020/09/17` | Xcode_12_beta6<br>`2020/08/25`<br>Xcode_12_beta5<br>`2020/08/18`<br>Xcode_12_beta4<br>`2020/08/07`<br>Xcode_12_beta3<br>`2020/07/22`<br>Xcode_12_beta2<br>`2020/07/07`<br>Xcode_12_beta<br>`2020/06/22` |
| 13.7 | Xcode_11.7 | Xcode_11.7<br>`2020/09/02` | ... |
| 13.6 | ... | ... | ... |
| 13.5 | ... | ... | ... |
| 13.4 | ... | ... | ... |
| 13.3 | ... | ... | ... |
| 13.2 | ... | ... | ... |
| 13.1 | ... | ... | ... |
| 13.0 | ... | ... | ... |
| 12.4 | ... | ... | ... |
| 12.3 | ... | ... | ... |
| 12.2 | ... | ... | ... |
| 12.1 | ... | ... | ... |
| 12.0 | ... | ... | ... |
| 11.4 | ... | ... | ... |
| 11.3 | ... | ... | ... |
| 11.2 | ... | ... | ... |
| 11.1 | ... | ... | ... |
| 11.0 | ... | ... | ... |
| 10.3 | ... | ... | ... |
| 10.2 | ... | ... | ... |
| 10.1 | ... | ... | ... |
| 10.0 | ... | ... | ... |
| 9.3 | ... | ... | ... |
| 9.2 | ... | ... | ... |
| 9.1 | ... | ... | ... |
| 9.0 | ... | ... | ... |