 _(for ThinkPad t480)_

**Step 0**
- Go to Settings > Apps
- Uninstall any Thunderbolt related apps

**Step 1**
- Download the [Drivers Package](https://download.lenovo.com/pccbbs/mobiles/n22ta14w.exe) and [Firmware Package](https://download.lenovo.com/pccbbs/mobiles/n24th13w.exe) executables

**Step 2**
- Install the Driver Package (N22TA14W.exe)
- Clear the `C:\DRIVERS\WIN\THUNDERBOLT` director

**Step 3**
- Execute the Firmware (N24TH13W.exe) but do not INSTALL it, only EXTRACT!

**Step 4**
- Navigate to `C:\DRIVERS\WIN\THUNDERBOLT\xxxxxxxx.xxxxxxxx\non`
- Type this command: **`.\FwUpdateCmd.exe GetCurrentNvmVersion "$(.\FwUpdateCmd.exe EnumControllers)"`**
- It should tell you the thunderbolt firmware version you have

**Step 5**
- Type this command: **`.\FwUpdateCmd.exe FWUpdate "$(.\FwUpdateCmd.exe EnumControllers)" TBT.bin`**
- The command should run and start updating the firmware. Give it some time, it'll tell you when you need to "unplug and completely shut down"

**Step 6**
- Click on the system tray and right click on the Thunderbolt™ Software > about, and it'll show you Thunderbolt Controller.
- In there it should say _"NVM Firmware Version: 23.00"_
- If that's the case you're golden.



[^1]: Sources:
	[https://www.reddit.com/r/thinkpad/comments/1aphtz2/is_there_any_simple_explanation_of_how_to_update/](https://www.reddit.com/r/thinkpad/comments/1aphtz2/is_there_any_simple_explanation_of_how_to_update/)
	[https://pcsupport.lenovo.com/it/en/products/laptops-and-netbooks/thinkpad-t-series-laptops/thinkpad-t480-type-20l5-20l6/solutions/ht508988](https://pcsupport.lenovo.com/it/en/products/laptops-and-netbooks/thinkpad-t-series-laptops/thinkpad-t480-type-20l5-20l6/solutions/ht508988)
	https://pcsupport.lenovo.com/us/en/products/laptops-and-netbooks/thinkpad-t-series-laptops/thinkpad-t480-type-20l5-20l6/downloads/driver-list/component?name=USB%20Device,%20FireWire,%20IEEE%201394,%20Thunderbolt
