# NESEmulator-watchOS

Updated to run on Xcode 13.3+ and watchOS 8.x+

NES Emulator on Apple Watch :space_invader: :watch:

[Demo](https://www.youtube.com/watch?v=uhx00fWGjOQ)

![](Documentation/Images/screenshot.png)

![](Documentation/Images/icon.png)

## How to Run

1. Clone this repository (`git clone https://github.com/adityajs12321/NESEmulator-watchOS/`)
2. Execute `carthage update --platform-watchOS` in terminal
3. Add your ROM to the roms folder in the Xcode project through Xcode
4. Navigate to `EmulatorScene.swift` and replace `let rom = Bundle.main.path(forResource: "smb3", ofType: "nes")` with `let rom = Bundle.main.path(forResource: "<insert_your_rom_filename_here>", ofType: "nes")`
5. Under the `NESEmulator Watchkit App` and `NESEmulator Watchkit Extension` target, change the bundle identifier to `com.<insert_any_username>.NESEmulator`. Then, update `Info.plist` under NESEumlator Watchkit App by replacing the value of `WKCompanionAppBundleIdentifier` with the same bundle identifier used earlier and do the same to the .plist file under NESEmulator Watchkit Extension by replacing `WKAppBundleIdentifier`'s value under `NSExtension`>`NSExtensionAttributes` with the aforementioned bundle ID
6. Build and Run

## Requirements

- Xcode 8.2+
- watchOS 3.1+ 
- Carthage 0.18+ (Install carthage from [here](https://github.com/Carthage/Carthage/releases/download/0.38.0/Carthage.pkg))
- Apple Watch Series 3 (Recommended)

## LICENSE

MIT License

Huge thanks to @giginet for this amazing emulator!

This application depends on [FCEUX-watchOS](https://github.com/giginet/FCEUX-watchOS).
It's licensed under [Provenance License and OpenEmu License](https://github.com/giginet/FCEUX-watchOS/blob/master/LICENSE).
